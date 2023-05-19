# Project
The task given by Nimap solutions is completed
The sql querry used is 
***CREATE TABLE Categories (
    CategoryId INT PRIMARY KEY,
    CategoryName NVARCHAR(100) NOT NULL
)

***CREATE TABLE Products (
    ProductId INT PRIMARY KEY,
    ProductName NVARCHAR(100) NOT NULL,
    CategoryId INT FOREIGN KEY REFERENCES Categories(CategoryId)
)
Both the Ids are auto incremented
The logic used for viewing 10 products is 
# public ActionResult Index(int? page)
    {
        int pageSize = 10;
        int pageNumber = page ?? 1;
        List<Product> products = db.Products.OrderBy(p => p.ProductId)
                                            .Skip((pageNumber - 1) * pageSize)
                                            .Take(pageSize)
    }
    The Screenshots are added below for more info
![Screenshot (37)](https://github.com/zeusssx/Project/assets/76738182/ddef7867-127d-4fb8-9005-7982a5b69dbb)
![Screenshot (38)](https://github.com/zeusssx/Project/assets/76738182/3e298e2a-c4c6-4c9b-97b6-729f151d5e22)
![Screenshot (39)](https://github.com/zeusssx/Project/assets/76738182/311519ce-bead-4be2-892a-a34b6af354b0)
![Screenshot (40)](https://github.com/zeusssx/Project/assets/76738182/5e0232e4-e943-4209-b450-c42e67e04740)
![Screenshot (41)](https://github.com/zeusssx/Project/assets/76738182/064dfd94-54b4-45fe-bfb6-401c3d6ad4fd)
![Screenshot (42)](https://github.com/zeusssx/Project/assets/76738182/6dbc2ead-dce3-4da0-a444-a5c6f34ded42)
![Screenshot (43)](https://github.com/zeusssx/Project/assets/76738182/655b9002-a5e2-4419-9d7c-73d4f7256ea5)
