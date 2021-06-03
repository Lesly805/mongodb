import pymongo
import os
import sys
import pprint

def main():
    connection_string = os.environ["MONGO_CONNECTION_STRING"]
    db_name = os.environ["MONGO_DBNAME"]

    client = pymongo.MongoClient(connection_string)
    db = client[db_name]
    collection = db['DSWclassdb']

#2. insert additional document using insert_one()
    collection_id = collection.insert_one(collection).inserted_id
    collection_id


    collection.count_documents({}) #3 print the number of documents in the collection


    pprint.pprint(collection.find_one())#4. print the first document in the collection


    for post in collection.find():
        pprint.pprint(post)#5. print all documents in the collection

    for post in collection.find({"name": "Daisy"}):
        pprint.pprint(post)##6. print all documents with a particular value for some attribute

if __name__=="__main__":
    main()
