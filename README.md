Практична робота №7 Мануйленко Микола

    #include <stdio.h>
    #include <math.h>

    int main() {
    double center1_x, center1_y, radius1, center2_x, center2_y, radius2; 
    double dist;

    scanf("%lf %lf %lf %lf %lf %lf", &center1_x, &center1_y, &radius1, &center2_x, &center2_y, &radius2);

    dist = sqrt((center2_x - center1_x) * (center2_x - center1_x) + (center2_y - center1_y) * (center2_y - center1_y));

    if (dist == 0 && radius1 == radius2) {
        printf("-1\n");
    } else if (dist > radius1 + radius2 || dist < fabs(radius1 - radius2) ) {
        printf("0\n");
    } else if (dist == radius1 + radius2 || dist == fabs(radius1 - radius2)) {
        printf("1\n");
    } else {
        printf("2\n");
    }

    return 0;
    }
