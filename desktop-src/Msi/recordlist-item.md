---
description: Item 屬性是唯讀屬性，會傳回 RecordList 物件集合中的記錄。
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: RecordList 專案屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c7b9332393c4055cb8052b2b759b93781c0fd73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993368"
---
# <a name="recordlistitem-property"></a><span data-ttu-id="78e3d-103">RecordList 專案屬性</span><span class="sxs-lookup"><span data-stu-id="78e3d-103">RecordList.Item property</span></span>

<span data-ttu-id="78e3d-104">**Item** 屬性是唯讀屬性，會傳回 [**RecordList**](recordlist-object.md)物件集合中的記錄。</span><span class="sxs-lookup"><span data-stu-id="78e3d-104">The **Item** property is a read-only property that returns a record in a [**RecordList**](recordlist-object.md) Object collection.</span></span>

<span data-ttu-id="78e3d-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="78e3d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="78e3d-106">語法</span><span class="sxs-lookup"><span data-stu-id="78e3d-106">Syntax</span></span>


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a><span data-ttu-id="78e3d-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="78e3d-107">Property value</span></span>

<span data-ttu-id="78e3d-108">具有字串集合之專案的索引編號。</span><span class="sxs-lookup"><span data-stu-id="78e3d-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="78e3d-109">需要索引。</span><span class="sxs-lookup"><span data-stu-id="78e3d-109">Index is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="78e3d-110">備註</span><span class="sxs-lookup"><span data-stu-id="78e3d-110">Remarks</span></span>

<span data-ttu-id="78e3d-111">用戶端必須先確認 [**RecordList**](recordlist-object.md) 物件存在且不是空的，然後再參考專案屬性。</span><span class="sxs-lookup"><span data-stu-id="78e3d-111">The client must verify that the [**RecordList**](recordlist-object.md) object exists and is not empty before referencing the Item property.</span></span>

## <a name="requirements"></a><span data-ttu-id="78e3d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="78e3d-112">Requirements</span></span>



| <span data-ttu-id="78e3d-113">需求</span><span class="sxs-lookup"><span data-stu-id="78e3d-113">Requirement</span></span> | <span data-ttu-id="78e3d-114">值</span><span class="sxs-lookup"><span data-stu-id="78e3d-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78e3d-115">版本</span><span class="sxs-lookup"><span data-stu-id="78e3d-115">Version</span></span><br/> | <span data-ttu-id="78e3d-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="78e3d-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="78e3d-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="78e3d-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="78e3d-118">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="78e3d-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="78e3d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="78e3d-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="78e3d-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78e3d-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="78e3d-121">IID</span><span class="sxs-lookup"><span data-stu-id="78e3d-121">IID</span></span><br/>     | <span data-ttu-id="78e3d-122">IID \_ IRecordList 定義為000C1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="78e3d-122">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




