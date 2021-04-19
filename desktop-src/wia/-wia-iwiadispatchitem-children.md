---
description: Item 物件的子屬性會抓取專案物件的集合。 這個集合中的專案代表在階層樹狀結構中，屬於此專案之直接子系的專案。 唯讀。
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: 專案。子系屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 144b60f1c8e9b500d49b53dfe290565c23023220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996605"
---
# <a name="itemchildren-property"></a><span data-ttu-id="b8cdc-105">專案。子系屬性</span><span class="sxs-lookup"><span data-stu-id="b8cdc-105">Item.Children property</span></span>

<span data-ttu-id="b8cdc-106">[**Item**](-wia-item.md)物件的 **子** 屬性會抓取 **專案** 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="b8cdc-106">The **Children** property of the [**Item**](-wia-item.md) object retrieves a collection of **Item** objects.</span></span> <span data-ttu-id="b8cdc-107">這個集合中的專案代表在階層樹狀結構中，屬於此專案之直接子系的專案。</span><span class="sxs-lookup"><span data-stu-id="b8cdc-107">The items in this collection represent items that are direct children of this item in the hierarchical tree.</span></span> <span data-ttu-id="b8cdc-108">唯讀。</span><span class="sxs-lookup"><span data-stu-id="b8cdc-108">Read-only.</span></span>

<span data-ttu-id="b8cdc-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b8cdc-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8cdc-110">語法</span><span class="sxs-lookup"><span data-stu-id="b8cdc-110">Syntax</span></span>


```JScript
propVal = Item.Children
```



## <a name="property-value"></a><span data-ttu-id="b8cdc-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="b8cdc-111">Property value</span></span>

<span data-ttu-id="b8cdc-112">接收物件的變數。</span><span class="sxs-lookup"><span data-stu-id="b8cdc-112">Variable that receives the objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8cdc-113">備註</span><span class="sxs-lookup"><span data-stu-id="b8cdc-113">Remarks</span></span>

<span data-ttu-id="b8cdc-114">使用這個屬性可流覽代表裝置的 [**專案**](-wia-item.md) 物件階層樹狀結構、資料夾和位於裝置上的檔案。</span><span class="sxs-lookup"><span data-stu-id="b8cdc-114">Use this property to navigate the hierarchical tree of [**Item**](-wia-item.md) objects that represent a device, the folders and the files that reside on the device.</span></span>

<span data-ttu-id="b8cdc-115">[ **子** 系] 屬性是 [**專案**](-wia-item.md) 物件的集合，只來自樹狀結構中這個 **專案** 物件下的層級。</span><span class="sxs-lookup"><span data-stu-id="b8cdc-115">The **Children** property is a collection of [**Item**](-wia-item.md) objects only from the level directly beneath this **Item** object in the tree.</span></span> <span data-ttu-id="b8cdc-116">若要在樹狀結構中向下導覽層級，請以遞迴方式使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="b8cdc-116">To navigate further levels down the tree, use this property recursively.</span></span>

<span data-ttu-id="b8cdc-117">如果專案不能或沒有任何子專案，這個屬性會傳回空集合。</span><span class="sxs-lookup"><span data-stu-id="b8cdc-117">If the item cannot or does not have any child items, this property returns an empty collection.</span></span>

> [!Note]  
> <span data-ttu-id="b8cdc-118">這個集合是以0為基礎。</span><span class="sxs-lookup"><span data-stu-id="b8cdc-118">This collection is 0-based.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b8cdc-119">範例</span><span class="sxs-lookup"><span data-stu-id="b8cdc-119">Examples</span></span>

<span data-ttu-id="b8cdc-120">下列範例示範如何使用 [ **子** 系] 屬性來抓取和列舉裝置的子專案集合。</span><span class="sxs-lookup"><span data-stu-id="b8cdc-120">The following example demonstrates the use of the **Children** property to retrieve and enumerate a collection of the child items of a device.</span></span> <span data-ttu-id="b8cdc-121">如果裝置是數位相機，則集合通常會包含資料夾和影像專案。</span><span class="sxs-lookup"><span data-stu-id="b8cdc-121">If the device is a digital camera, the collection typically contains folder and image items.</span></span> <span data-ttu-id="b8cdc-122">如果裝置是掃描器，則集合通常會包含代表掃描張床的專案。</span><span class="sxs-lookup"><span data-stu-id="b8cdc-122">If the device is a scanner, the collection typically contains items that represent scanning beds.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="b8cdc-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8cdc-123">Requirements</span></span>



| <span data-ttu-id="b8cdc-124">需求</span><span class="sxs-lookup"><span data-stu-id="b8cdc-124">Requirement</span></span> | <span data-ttu-id="b8cdc-125">值</span><span class="sxs-lookup"><span data-stu-id="b8cdc-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8cdc-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8cdc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b8cdc-127">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8cdc-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8cdc-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8cdc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b8cdc-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8cdc-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b8cdc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b8cdc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8cdc-131"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="b8cdc-131"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




