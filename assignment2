#include <stdio.h>
#include <stdlib.h>
#include <math.h>

double f(double num);
double fx(double a,double b);
int main(){
    double a, b,c,  tolerance;
    int iter=0;

    printf("Regula Falsi Method for f(x) = x^3 - 2x - 5 \n");
    printf("Enter lower limit a: ");
    scanf("%lf", &a);
    printf("Enter upper limit b: ");
    scanf("%lf", &b);
    printf("Enter tolerance: ");
    scanf("%lf", &tolerance);

        if (f(a) * f(b) >= 0) {
            printf("The Regula Falsi Method cannot be applied. The function does not have root in given interval.\n");
        return 1;
        }

    printf("\nIteration |     a     |     b     |     c     |    f(c)   |  |b-a| \n");
    printf("-------------------------------------------------------------------\n");
    do{
        c=fx(a,b);
        printf("%9d | %8.6f | %8.6f | %8.6f | %8.6f | %8.6f\n",++iter, a, b, c, f(c), fabs(b - a));
        if (fabs(f(c)) < tolerance || fabs(b - a) < tolerance) {
            printf("\nRoot found at x = %f after %d iterations.\n", c, iter);
            return 0;
        }
            if (iter >= 100) {
            printf("\nMethod failed to converge within the maximum number of iterations (100).\n");
            return 1;
        }
        if (f(a) * f(c) < 0)
            b = c;
        else
            a = c;
        }while(1);

    return 0;
    }

    double f(double num){
        return num*num*num-2*num-5;
    }

    double fx(double a,double b){
        double result;
        result =(a*f(b)-b*f(a))/(f(b)-f(a));
        return result ;
    }
