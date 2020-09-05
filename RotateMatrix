#include<stdio.h>
#include<stdlib.h>
#include<malloc.h>
#include<time.h>


void
nl (void)
{				//function to print new line
  printf ("\n");
}

int **
allocate (_size)
{				//allocating matrix in malloc
  int **matrix = (int *) malloc (sizeof (int) * _size);
  for (int i = 0; i < _size; i++)
    {
      matrix[i] = (int *) malloc (sizeof (int) * _size);
    }
  return matrix;
}

void
scanMatrix (_matrix, _size)	//function
     int **_matrix;
{

  int upper_limit, lower_limit, n, i;
  srand (time (0));
  for (int i = 0; i < _size; i++)
    {
      for (int j = 0; j < _size; j++)
	{
	  _matrix[i][j] =
	    (rand () % (upper_limit - lower_limit)) + lower_limit;
	}
    }
}

void
printMatrix (_matrix, _size)	//function to printMatrix
     int **_matrix;
{
  for (int i = 0; i < _size; i++)
    {
      for (int j = 0; j < _size; j++)
	{
	  printf ("%d ", _matrix[i][j]);
	}
      nl ();
    }
}

void
swap (num1, num2)		//constructing the final matrix
     int *num1;
     int *num2;
{
  *num1 = *num1 + *num2;
  *num2 = *num1 - *num2;
  *num1 = *num1 - *num2;
}

void
rotateMatrix (_matrix, _size)	//rotateMatrix
     int **_matrix;
{
  for (int i = 0; i < _size; i++)
    {
      for (int j = i + 1; j < _size; j++)
	{
	  swap (&_matrix[i][j], &_matrix[j][i]);
	}
    }
  for (int i = 0; i < _size; i++)
    {
      for (int j = 0; j < _size / 2; j++)
	{
	  swap (&_matrix[i][j], &_matrix[i][_size - 1 - j]);
	}
    }
}

main (argc, argv)		//Driver code
     const char **argv;
{
  int size = 0;
  printf ("Enter the size of the square matrix: ");
  scanf ("%d", &size);
  int **matrix = allocate (size);
  scanMatrix (matrix, size);
  printMatrix (matrix, size);
  nl ();
  rotateMatrix (matrix, size);
  nl ();
  printMatrix (matrix, size);
  return 0;
}
