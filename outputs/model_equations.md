
# Task 3: Dummy Variable Approach

## Why Dummy Variables are Created

The dataset contains categorical variables such as region,store_type,and month. Since linear regression requires numerical input variables, categorical variables cannot be used directly in the regression model.

Dummy variables were therefore created to convert categorical values into binary (0/1) variables while preserving their categorical meaning.

---

## Region Dummy Variables

The region variable contains four categories:

- East
- West
- North
- South

To avoid the dummy variable trap (perfect multicollinearity), one category must be used as the reference category.

Reference Category: East

The following dummy variables are created:

- Region_West
- Region_North
- Region_South

Encoding:

| Region | Region_West | Region_North | Region_South |
|--------|------------:|-------------:|-------------:|
| East (Reference) | 0 | 0 | 0 |
| West | 1 | 0 | 0 |
| North | 0 | 1 | 0 |
| South | 0 | 0 | 1 |

---

## Store Type Dummy Variables

The store_type variable contains four categories:

- Residential
- Airport
- High Street
- Mall

Reference Category: Residential

The following dummy variables are created:

- Store_Airport
- Store_HighStreet
- Store_Mall

Encoding:

| Store Type | Store_Airport | Store_HighStreet | Store_Mall |
|------------|--------------:|-----------------:|-----------:|
| Residential (Reference) | 0 | 0 | 0 |
| Airport | 1 | 0 | 0 |
| High Street | 0 | 1 | 0 |
| Mall | 0 | 0 | 1 |

---

## Month Variable

The month column is retained in its original YYYY-MM format.

Although month is a categorical variable, dummy variables are not created because the assignment requires dummy variables for at least one categorical variable , and the selected regression model does not include month as an explanatory variable.

---

## Why One Category is Omitted

One category from each categorical variable is intentionally excluded and used as the reference category.

This prevents perfect multicollinearity (also known as the dummy variable trap) and allows the regression coefficients to be interpreted relative to the reference category.

- Region Reference Category: East
- Store Type Reference Category: Residential

The coefficients of the dummy variables therefore represent the expected difference compared with the corresponding reference category while holding all other variables constant.

