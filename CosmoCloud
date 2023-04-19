list_1 = [
    {"id": "1", "name": "Shrey", "age": 25},
    {"id": "3", "age": 10, "name": "Hello"},
    {"id": "2", "name": "World", "age": 24},
]

list_2 = [
    {"id": "1", "marks": 100},
    {
        "id": "3",
        "marks": 90,
        "roll_no": 11,
        "extra_info": {
            "hello": "world",
        },
    },
]
def comparator(x):
    return int(x["id"])


def merge_lists(list_1, list_2) -> list:
    """
    Complete this function, by merging the information from list_1 and list_2
    to create a new list, which has all the information about each student from
    both lists in one single dict.
    - Both lists are unsorted
    - Both lists can have missing values (for ex list_2 has missing id=2)
    """
    #sorting lists based on id
    list_1=sorted(list_1,key=comparator)  
    list_2=sorted(list_2,key=comparator)
    list_3=[]
    i=0
    j=0
    n=len(list_1)
    m=len(list_2)
    # traverse both lists
    while(i<n and j<m):
        
        if(list_1[i]['id']==list_2[j]['id']):
            # if ids of both elements are matched
            # create a dictionary with both elements.
            temp_dict=dict()
            temp_dict.update(list_1[i])
            temp_dict.update(list_2[j])
            i+=1
            j+=1
            list_3.append(temp_dict) 
        elif(list_1[i]['id']<list_2[j]['id']):
            list_3.append(list_1[i])
            i+=1
        else:
            list_3.append(list_2[j])
            j+=1
    while(i<n):
        list_3.append(list_1[i])
        i+=1
    while(j<m):
        list_3.append(list_2[j])
        j+=1
    return list_3



list_3 = merge_lists(list_1, list_2)
print(list_3)
