# simple-algorithms
To realize some simple fundamental algorithms using C/C++

/*  Bubble Dort Algorithm */
/*  冒泡排序法的基本思想：（以升序为例）含有n个元素的数组原则上要进行n-1次排序。对于每一躺的排序，从第一个数开始，依次比较前一个数与后一个数的大小。如果前一个数比后一个数大，则进行交换。这样一轮过后，最大的数将会出现称为最末位的数组元素。第二轮则去掉最后一个数，对前n-1个数再按照上面的步骤找出最大数，该数将称为倒数第二的数组元素......n-1轮过后，就完成了排序。
//若要以降序顺序排列，则只需将 if(array[j]>array[j+1])语句中的大于号改为小于号即可。*/
# include <stdio.h>
int main()
{
    int tem,i,j,a[10];
    printf("plz enter 10 integers:");
    for (i=0;i<10;i++)
      scanf("%d",&a[i]);
    for(j=0;j<9;j++)
    {
    	for(i=0;i<9-j;i++)
    	if(a[i]>a[i+1])
    	{
    		tem=a[i];
    		a[i]=a[i+1];
    		a[i+1]=tem;
    	}
    }
     for (i=0;i<10;i++)
     printf("%d ",a[i]);
}
