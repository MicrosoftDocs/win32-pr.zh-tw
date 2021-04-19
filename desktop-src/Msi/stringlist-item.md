---
description: Item 屬性是唯讀屬性，會傳回 StringList 物件集合中的字串。
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: StringList 專案屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984790"
---
# <a name="stringlistitem-property"></a><span data-ttu-id="a21cd-103">StringList 專案屬性</span><span class="sxs-lookup"><span data-stu-id="a21cd-103">StringList.Item property</span></span>

<span data-ttu-id="a21cd-104">**Item** 屬性是唯讀屬性，會傳回 [**StringList 物件**](stringlist-object.md)集合中的字串。</span><span class="sxs-lookup"><span data-stu-id="a21cd-104">The **Item** property is a read-only property that returns a string in the [**StringList Object**](stringlist-object.md) collection.</span></span>

<span data-ttu-id="a21cd-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="a21cd-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a21cd-106">語法</span><span class="sxs-lookup"><span data-stu-id="a21cd-106">Syntax</span></span>


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a><span data-ttu-id="a21cd-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="a21cd-107">Property value</span></span>

<span data-ttu-id="a21cd-108">具有字串集合之專案的索引編號。</span><span class="sxs-lookup"><span data-stu-id="a21cd-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="a21cd-109">此為必要參數。</span><span class="sxs-lookup"><span data-stu-id="a21cd-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="a21cd-110">備註</span><span class="sxs-lookup"><span data-stu-id="a21cd-110">Remarks</span></span>

<span data-ttu-id="a21cd-111">用戶端必須先確認 [**StringList 物件**](stringlist-object.md) 存在且不是空的，然後再參考 **專案** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a21cd-111">The client must verify that the [**StringList Object**](stringlist-object.md) exists and is not empty before referencing the **Item** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a21cd-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a21cd-112">Requirements</span></span>



| <span data-ttu-id="a21cd-113">需求</span><span class="sxs-lookup"><span data-stu-id="a21cd-113">Requirement</span></span> | <span data-ttu-id="a21cd-114">值</span><span class="sxs-lookup"><span data-stu-id="a21cd-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a21cd-115">版本</span><span class="sxs-lookup"><span data-stu-id="a21cd-115">Version</span></span><br/> | <span data-ttu-id="a21cd-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="a21cd-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a21cd-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="a21cd-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a21cd-118">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="a21cd-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a21cd-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a21cd-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="a21cd-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a21cd-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a21cd-121">IID</span><span class="sxs-lookup"><span data-stu-id="a21cd-121">IID</span></span><br/>     | <span data-ttu-id="a21cd-122">IID \_ IStringList 定義為000C1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a21cd-122">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




