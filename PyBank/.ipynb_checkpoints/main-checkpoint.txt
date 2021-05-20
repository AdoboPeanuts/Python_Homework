{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {},
   "outputs": [],
   "source": [
    "#Import the necessary librarbies for reading csv files\n",
    "import numpy_financial as np\n",
    "import pandas as pd"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Date</th>\n",
       "      <th>Profit/Losses</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Jan-2010</td>\n",
       "      <td>867884</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Feb-2010</td>\n",
       "      <td>984655</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Mar-2010</td>\n",
       "      <td>322013</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Apr-2010</td>\n",
       "      <td>-69417</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>May-2010</td>\n",
       "      <td>310503</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>81</th>\n",
       "      <td>Oct-2016</td>\n",
       "      <td>102685</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>82</th>\n",
       "      <td>Nov-2016</td>\n",
       "      <td>795914</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>83</th>\n",
       "      <td>Dec-2016</td>\n",
       "      <td>60988</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>84</th>\n",
       "      <td>Jan-2017</td>\n",
       "      <td>138230</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>85</th>\n",
       "      <td>Feb-2017</td>\n",
       "      <td>671099</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>86 rows × 2 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "        Date  Profit/Losses\n",
       "0   Jan-2010         867884\n",
       "1   Feb-2010         984655\n",
       "2   Mar-2010         322013\n",
       "3   Apr-2010         -69417\n",
       "4   May-2010         310503\n",
       "..       ...            ...\n",
       "81  Oct-2016         102685\n",
       "82  Nov-2016         795914\n",
       "83  Dec-2016          60988\n",
       "84  Jan-2017         138230\n",
       "85  Feb-2017         671099\n",
       "\n",
       "[86 rows x 2 columns]"
      ]
     },
     "execution_count": 2,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Creating Path File for CSV file \n",
    "# Creating a variable named \"df\" and assigning a path file.\n",
    "\n",
    "df = pd.read_csv(r\"C:/Users/johnm/PyBank/resources/budget_data.csv\")\n",
    "df"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "86"
      ]
     },
     "execution_count": 3,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Created a variable, 'total_months', and assigned\n",
    "\n",
    "total_months = df['Date'].count()\n",
    "\n",
    "total_months"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "38382578"
      ]
     },
     "execution_count": 4,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Created a variable, 'total', and assigned a formula to calculate the sum of 'Profit/Losses'\n",
    "\n",
    "total = df['Profit/Losses'].sum()\n",
    "\n",
    "total\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Date</th>\n",
       "      <th>Profit/Losses</th>\n",
       "      <th>shifted_column</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Jan-2010</td>\n",
       "      <td>867884</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Feb-2010</td>\n",
       "      <td>984655</td>\n",
       "      <td>867884.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Mar-2010</td>\n",
       "      <td>322013</td>\n",
       "      <td>984655.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Apr-2010</td>\n",
       "      <td>-69417</td>\n",
       "      <td>322013.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>May-2010</td>\n",
       "      <td>310503</td>\n",
       "      <td>-69417.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>81</th>\n",
       "      <td>Oct-2016</td>\n",
       "      <td>102685</td>\n",
       "      <td>768450.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>82</th>\n",
       "      <td>Nov-2016</td>\n",
       "      <td>795914</td>\n",
       "      <td>102685.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>83</th>\n",
       "      <td>Dec-2016</td>\n",
       "      <td>60988</td>\n",
       "      <td>795914.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>84</th>\n",
       "      <td>Jan-2017</td>\n",
       "      <td>138230</td>\n",
       "      <td>60988.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>85</th>\n",
       "      <td>Feb-2017</td>\n",
       "      <td>671099</td>\n",
       "      <td>138230.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>86 rows × 3 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "        Date  Profit/Losses  shifted_column\n",
       "0   Jan-2010         867884             NaN\n",
       "1   Feb-2010         984655        867884.0\n",
       "2   Mar-2010         322013        984655.0\n",
       "3   Apr-2010         -69417        322013.0\n",
       "4   May-2010         310503        -69417.0\n",
       "..       ...            ...             ...\n",
       "81  Oct-2016         102685        768450.0\n",
       "82  Nov-2016         795914        102685.0\n",
       "83  Dec-2016          60988        795914.0\n",
       "84  Jan-2017         138230         60988.0\n",
       "85  Feb-2017         671099        138230.0\n",
       "\n",
       "[86 rows x 3 columns]"
      ]
     },
     "execution_count": 5,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Created a column of shifted values.\n",
    "\n",
    "df['shifted_column'] = df['Profit/Losses'].shift(1)\n",
    "df"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Date</th>\n",
       "      <th>Profit/Losses</th>\n",
       "      <th>shifted_column</th>\n",
       "      <th>difference</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Jan-2010</td>\n",
       "      <td>867884</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Feb-2010</td>\n",
       "      <td>984655</td>\n",
       "      <td>867884.0</td>\n",
       "      <td>116771.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Mar-2010</td>\n",
       "      <td>322013</td>\n",
       "      <td>984655.0</td>\n",
       "      <td>-662642.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Apr-2010</td>\n",
       "      <td>-69417</td>\n",
       "      <td>322013.0</td>\n",
       "      <td>-391430.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>May-2010</td>\n",
       "      <td>310503</td>\n",
       "      <td>-69417.0</td>\n",
       "      <td>379920.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>81</th>\n",
       "      <td>Oct-2016</td>\n",
       "      <td>102685</td>\n",
       "      <td>768450.0</td>\n",
       "      <td>-665765.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>82</th>\n",
       "      <td>Nov-2016</td>\n",
       "      <td>795914</td>\n",
       "      <td>102685.0</td>\n",
       "      <td>693229.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>83</th>\n",
       "      <td>Dec-2016</td>\n",
       "      <td>60988</td>\n",
       "      <td>795914.0</td>\n",
       "      <td>-734926.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>84</th>\n",
       "      <td>Jan-2017</td>\n",
       "      <td>138230</td>\n",
       "      <td>60988.0</td>\n",
       "      <td>77242.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>85</th>\n",
       "      <td>Feb-2017</td>\n",
       "      <td>671099</td>\n",
       "      <td>138230.0</td>\n",
       "      <td>532869.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>86 rows × 4 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "        Date  Profit/Losses  shifted_column  difference\n",
       "0   Jan-2010         867884             NaN         NaN\n",
       "1   Feb-2010         984655        867884.0    116771.0\n",
       "2   Mar-2010         322013        984655.0   -662642.0\n",
       "3   Apr-2010         -69417        322013.0   -391430.0\n",
       "4   May-2010         310503        -69417.0    379920.0\n",
       "..       ...            ...             ...         ...\n",
       "81  Oct-2016         102685        768450.0   -665765.0\n",
       "82  Nov-2016         795914        102685.0    693229.0\n",
       "83  Dec-2016          60988        795914.0   -734926.0\n",
       "84  Jan-2017         138230         60988.0     77242.0\n",
       "85  Feb-2017         671099        138230.0    532869.0\n",
       "\n",
       "[86 rows x 4 columns]"
      ]
     },
     "execution_count": 6,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Created a column with the difference between current value 'Profit/Losses' and last line value 'shifted_column'\n",
    "\n",
    "df['difference'] = df['Profit/Losses'] - df['shifted_column']\n",
    "df"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "-2315.1176470588234"
      ]
     },
     "execution_count": 7,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Created a variable, 'average_difference' and assigned value to calculate mean\n",
    "\n",
    "average_difference = df['difference'].mean()\n",
    "\n",
    "average_difference"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "1926159.0"
      ]
     },
     "execution_count": 8,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Created a variable. 'greatest_increase', and assigned a value to calculate maximum difference\n",
    "\n",
    "greatest_increase = df['difference'].max()\n",
    "\n",
    "greatest_increase\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "-2196167.0"
      ]
     },
     "execution_count": 9,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Created a variable, 'greatest_decrease', and assigned a value to calculate minimum difference\n",
    "\n",
    "greatest_decrease = df['difference'].min()\n",
    "\n",
    "greatest_decrease"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Date</th>\n",
       "      <th>Profit/Losses</th>\n",
       "      <th>shifted_column</th>\n",
       "      <th>difference</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>25</th>\n",
       "      <td>Feb-2012</td>\n",
       "      <td>1170593</td>\n",
       "      <td>-755566.0</td>\n",
       "      <td>1926159.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "        Date  Profit/Losses  shifted_column  difference\n",
       "25  Feb-2012        1170593       -755566.0   1926159.0"
      ]
     },
     "execution_count": 10,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Taking the value of 'greatest_increase' and locating it inside df\n",
    "\n",
    "df.loc[df['difference']==greatest_increase]\n",
    "\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Date</th>\n",
       "      <th>Profit/Losses</th>\n",
       "      <th>shifted_column</th>\n",
       "      <th>difference</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>44</th>\n",
       "      <td>Sep-2013</td>\n",
       "      <td>-1196225</td>\n",
       "      <td>999942.0</td>\n",
       "      <td>-2196167.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "        Date  Profit/Losses  shifted_column  difference\n",
       "44  Sep-2013       -1196225        999942.0  -2196167.0"
      ]
     },
     "execution_count": 11,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Taking the value of 'greatest_decrease' and locating it inside df\n",
    "\n",
    "df.loc[df['difference']==greatest_decrease]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Financial Analysis\n",
      "Total Month:  86\n",
      "Total: $ 38382578\n",
      "Average Change: $ -2315.12\n",
      "Greatest Increase in Profits: Feb-2012 $ 1926159.0\n",
      "Greatest Decrease in Profits: Sep-2013 $ -2196167.0\n"
     ]
    }
   ],
   "source": [
    "print(\"Financial Analysis\")\n",
    "print(f'Total Month: ', total_months)\n",
    "print(f'Total: $', total)\n",
    "print(f'Average Change: $', f'{average_difference:.2f}')\n",
    "print(f'Greatest Increase in Profits: Feb-2012 $', greatest_increase)\n",
    "print(f'Greatest Decrease in Profits: Sep-2013 $', greatest_decrease)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.8.8"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 4
}
