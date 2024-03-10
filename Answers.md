Question1->   many to one relationship
Question2->To ensure that each product in the "Product" table has a valid category assigned to it, you can establish a foreign key relationship between the "Product" table and the "product_category" table. This is typically done by adding a foreign key constraint on the "category_id" column in the "Product" table, referencing the "id" column in the "product_category" table.

ALTER TABLE product
ADD CONSTRAINT fk_product_category
FOREIGN KEY (category_id)
REFERENCES product_category(id);
