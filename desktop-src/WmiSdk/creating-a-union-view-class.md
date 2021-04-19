---
description: Union view 類別是來源類別實例的邏輯聯集。 Union view 類別包含來源類別的所有實例，除非您在來源查詢中包含 WHERE 子句，以限制實例。
ms.assetid: 54a9804d-644d-4ab6-a3d5-c9c4f7761967
ms.tgt_platform: multiple
title: 建立聯集視圖類別
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ff9327645828c3db78a82811831f058cc27f202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985086"
---
# <a name="creating-a-union-view-class"></a><span data-ttu-id="8b044-104">建立聯集視圖類別</span><span class="sxs-lookup"><span data-stu-id="8b044-104">Creating a Union View Class</span></span>

<span data-ttu-id="8b044-105">Union view 類別是來源類別實例的邏輯聯集。</span><span class="sxs-lookup"><span data-stu-id="8b044-105">A union view class is a logical union of source class instances.</span></span> <span data-ttu-id="8b044-106">Union view 類別包含來源類別的所有實例，除非您在來源查詢中包含 WHERE 子句，以限制實例。</span><span class="sxs-lookup"><span data-stu-id="8b044-106">A union view class includes all the instances of the source classes unless you limit the instances by including a WHERE clause on the source query.</span></span>

<span data-ttu-id="8b044-107">當您想要查看位於不同命名空間或不同電腦上的類似或相同類別的實例時，聯集視圖類別相當有用。</span><span class="sxs-lookup"><span data-stu-id="8b044-107">Union view classes are useful when you want to see instances of similar or identical classes that are located in different namespaces or on different computers.</span></span> <span data-ttu-id="8b044-108">例如，您可以建立包含要監視之不同磁片磁碟機實例的聯集類別。</span><span class="sxs-lookup"><span data-stu-id="8b044-108">For example, you can create a union class that contains instances of different disk drives to monitor.</span></span>

<span data-ttu-id="8b044-109">您也可以將等位視圖類別的屬性作為所有來源類別實例中不存在的屬性作為基礎。</span><span class="sxs-lookup"><span data-stu-id="8b044-109">You can also base the properties of a union view class on properties not present in all of the source class instances.</span></span> <span data-ttu-id="8b044-110">如果來源類別實例沒有相同的屬性，則 union 類別實例的屬性值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8b044-110">If the source class instances do not have the same property, the properties of union class instances have a value of **NULL**.</span></span> <span data-ttu-id="8b044-111">例如，如果某個硬碟機有 **溫度** 屬性，但另一個硬碟沒有，您仍然可以建立兩者之間的聯集。</span><span class="sxs-lookup"><span data-stu-id="8b044-111">For example, if one hard disk drive has a **temperature** property but another does not, you can still create a union between the two.</span></span>

<span data-ttu-id="8b044-112">下列程式描述如何建立聯集視圖類別。</span><span class="sxs-lookup"><span data-stu-id="8b044-112">The following procedure describes how to create a union view class.</span></span>

<span data-ttu-id="8b044-113">**若要建立聯集視圖類別**</span><span class="sxs-lookup"><span data-stu-id="8b044-113">**To create a union view class**</span></span>

1.  <span data-ttu-id="8b044-114">使用聯 [**集**](qualifiers-specific-to-the-view-provider.md) 字串辨識符號來開始您的類別定義。</span><span class="sxs-lookup"><span data-stu-id="8b044-114">Begin your class definition with the [**Union**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="8b044-115">[**JoinOn**](qualifiers-specific-to-the-view-provider.md)、 **Association** 和 **Union** 限定詞都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="8b044-115">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="8b044-116">建立查詢，以使用 [**ViewSources**](viewsources-qualifier.md) 限定詞來定義 view 類別中所使用的來源類別。</span><span class="sxs-lookup"><span data-stu-id="8b044-116">Create the queries that define source classes used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="8b044-117">使用 [**ViewSpaces**](viewspaces-qualifier.md) 限定詞來定義來源類別所在之命名空間的名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="8b044-117">Define the names and location of the namespaces in which the source classes are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="8b044-118">使用 [**PropertySources**](propertysources-qualifier.md) 限定詞，定義對應至來源類別中屬性的屬性。</span><span class="sxs-lookup"><span data-stu-id="8b044-118">Define the properties that map to the properties in the source classes with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="8b044-119">如有必要，您可以使用 [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) 限定詞，將任何屬性標記為屬於來源類別。</span><span class="sxs-lookup"><span data-stu-id="8b044-119">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="8b044-120">定義您的等位視圖類別之來源類別的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="8b044-120">Define the key properties of the source classes of your union view class.</span></span>

    <span data-ttu-id="8b044-121">每個來源類別都必須有與 [**CIMType**](swbemproperty-cimtype.md)相符的相同索引鍵屬性數目。</span><span class="sxs-lookup"><span data-stu-id="8b044-121">Each source class must have the same number of key properties matched by [**CIMType**](swbemproperty-cimtype.md).</span></span> <span data-ttu-id="8b044-122">此外，您的等位視圖類別的索引鍵必須可唯一識別所有來源實例。</span><span class="sxs-lookup"><span data-stu-id="8b044-122">Also, the keys of your union view class must uniquely identify all source instances.</span></span> <span data-ttu-id="8b044-123">在某些情況下，您可能需要指定系統屬性，以確保實例是唯一的。</span><span class="sxs-lookup"><span data-stu-id="8b044-123">In some cases, you might need to specify system properties to ensure that instances are unique.</span></span> <span data-ttu-id="8b044-124">例如，如果您在兩個不同的命名空間中，從兩個相同類別的聯集建立一個視圖，您可以在 view 類別中包含 [**\_ \_ Namespace**](--namespace.md)屬性做為索引鍵，以區分這兩個實例。</span><span class="sxs-lookup"><span data-stu-id="8b044-124">For example, if you create a view from the union of two identical classes in two different namespaces, you could include the [**\_\_Namespace**](--namespace.md) property as a key in the view class to differentiate between the two instances.</span></span> <span data-ttu-id="8b044-125">如果您在相同的命名空間中使用兩個類似的類別來建立視圖，則可以使用 **\_ \_ 類別** 屬性來區分兩者。</span><span class="sxs-lookup"><span data-stu-id="8b044-125">If you use two similar classes from the same namespace to create a view, you could use the **\_\_Class** property to distinguish between the two.</span></span> <span data-ttu-id="8b044-126">重新命名視圖中的任何系統屬性，讓您可以避免與 view 類別的系統屬性發生衝突。</span><span class="sxs-lookup"><span data-stu-id="8b044-126">Rename any system properties in the view so you can avoid a conflict with the system properties of the view class.</span></span>

6.  <span data-ttu-id="8b044-127">使用 [**MethodSource**](qualifiers-specific-to-the-view-provider.md) 限定詞定義任何您想要的方法。</span><span class="sxs-lookup"><span data-stu-id="8b044-127">Define any methods you want using the [**MethodSource**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

    <span data-ttu-id="8b044-128">不同于其他視圖類別，您可以建立方法來修改聯集視圖。</span><span class="sxs-lookup"><span data-stu-id="8b044-128">Unlike other view classes, you can create methods to modify a union view.</span></span>

<span data-ttu-id="8b044-129">下列程式碼範例描述聯集視圖類別。</span><span class="sxs-lookup"><span data-stu-id="8b044-129">The following code example describes a union view class.</span></span>

``` syntax
[Union, ViewSources{"SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM LocalDisk", 
    "SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM RemoteDisk"}, 
    ViewSpaces{"\\\\.\\Root\\LocalNamespace","\\\\.\\Root\\RemoteNamespace"}, 
    dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class UnionOfDrives

{
    [PropertySources{"Description", "Description"}] string des;
    [PropertySources{"DeviceID", "DeviceID"}, key] String did;
    [PropertySources{"__Namespace", "__Namespace"}, key] String KEYID;
    [PropertySources{"FileSystem", "FileSystem"}] String fsystem ;
    [PropertySources{"FreeSpace", "FreeSpace"}] uint64 fspace;
    [PropertySources{"VolumeName", "VolumeName"}] String vname;
};
```

 

 



