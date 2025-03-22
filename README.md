4. 查询衬衣（Read）
我们可以定义一个函数来显示所有衬衣信息，或者根据特定ID查询单个衬衣信息。

python
def list_shirts():
    if not shirts:
        print("No shirts available.")
    else:
        for shirt in shirts:
            print(shirt)
 
def find_shirt(shirt_id):
    for shirt in shirts:
        if shirt['id'] == shirt_id:
            return shirt
    print(f"Shirt with ID {shirt_id} not found.")
    return None
5. 更新衬衣（Update）
定义一个函数来更新库存中的衬衣信息。

python
def update_shirt(shirt_id, new_data):
    shirt = find_shirt(shirt_id)
    if shirt:
        shirt.update(new_data)
        print(f"Shirt {shirt_id} updated successfully.")
    else:
        print(f"Shirt with ID {shirt_id} not found.")
6. 删除衬衣（Delete）
定义一个函数来从库存中删除特定ID的衬衣。

python
def delete_shirt(shirt_id):
    global shirts
    shirts = [shirt for shirt in shirts if shirt['id'] != shirt_id]
    print(f"Shirt {shirt_id} deleted successfully.")
