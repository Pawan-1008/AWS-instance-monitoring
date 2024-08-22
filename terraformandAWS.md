
# Launching an instance using Terraform

![image](https://github.com/user-attachments/assets/b51b5449-f573-4f43-adbc-abf0d8d491b3)

## creating an IAM role to launching an instance.

![image](https://github.com/user-attachments/assets/fad0bbc4-0671-4499-be92-ea91f1383e88)
![image](https://github.com/user-attachments/assets/a6556b27-0a7d-4af0-8674-2c57ae90fbba)



## Launching an instance using Terraform:

---------------------------------------------------

provider "aws" {
  region  = "us-east-1"
}

resource "aws_instance" "app_server" {
  ami           = "ami-830c94e3"
  instance_type = "t2.micro"

  tags = {
    Name = "ExampleAppServerInstance"
  }
}

----------------------------------------------------

## Init, plan & apply the file

- terraform init
- terraform plan
- terraform apply

![image](https://github.com/user-attachments/assets/f927bb75-3fb9-4f2a-94b6-af4cef0c2a5a)

![image](https://github.com/user-attachments/assets/b9c190d2-c3c3-4a79-8cde-1870a2770b89)

![image](https://github.com/user-attachments/assets/ae403ab9-b224-4869-a6cf-ba6c9760578c)


-----------------------------------------------------------------------------------------


![image](https://github.com/user-attachments/assets/e5f011f9-d583-483d-a166-fb2feb0369a8)



![image](https://github.com/user-attachments/assets/c2d295c5-32c9-4eaf-905f-ab6f41ac04b7)


