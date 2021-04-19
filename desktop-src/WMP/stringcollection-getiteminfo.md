---
title: StringCollection. getItemInfo 方法
description: GetItemInfo 方法會抓取對應于指定之 StringCollection 專案索引和名稱的字串。
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，StringCollection 類別
- StringCollection 類別 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- StringCollection.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9552dcebbc7d565ebc797c62ac3bc00ee109fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995332"
---
# <a name="stringcollectiongetiteminfo-method"></a><span data-ttu-id="05a93-106">StringCollection. getItemInfo 方法</span><span class="sxs-lookup"><span data-stu-id="05a93-106">StringCollection.getItemInfo method</span></span>

<span data-ttu-id="05a93-107">**GetItemInfo** 方法會抓取對應于指定之 **StringCollection** 專案索引和名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="05a93-107">The **getItemInfo** method retrieves the string corresponding to the specified **StringCollection** item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="05a93-108">語法</span><span class="sxs-lookup"><span data-stu-id="05a93-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="05a93-109">參數</span><span class="sxs-lookup"><span data-stu-id="05a93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05a93-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05a93-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05a93-111">**Number** (**long**) 指定要從中取得屬性之 **StringCollection** 專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="05a93-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="05a93-112">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05a93-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05a93-113">包含屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="05a93-113">**String** containing the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05a93-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="05a93-114">Return value</span></span>

<span data-ttu-id="05a93-115">這個方法會傳回 **字串** ，表示指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="05a93-115">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="05a93-116">針對其基礎值為 **布林** 值的屬性，它會傳回字串 "true" 或 "false"。</span><span class="sxs-lookup"><span data-stu-id="05a93-116">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="05a93-117">備註</span><span class="sxs-lookup"><span data-stu-id="05a93-117">Remarks</span></span>

<span data-ttu-id="05a93-118">若要使用具有複雜值的多個值和屬性來取得屬性，請使用 **getItemInfoByType** 方法。</span><span class="sxs-lookup"><span data-stu-id="05a93-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="05a93-119">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="05a93-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="05a93-120">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="05a93-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05a93-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="05a93-121">Requirements</span></span>



| <span data-ttu-id="05a93-122">需求</span><span class="sxs-lookup"><span data-stu-id="05a93-122">Requirement</span></span> | <span data-ttu-id="05a93-123">值</span><span class="sxs-lookup"><span data-stu-id="05a93-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05a93-124">版本</span><span class="sxs-lookup"><span data-stu-id="05a93-124">Version</span></span><br/> | <span data-ttu-id="05a93-125">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="05a93-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="05a93-126">DLL</span><span class="sxs-lookup"><span data-stu-id="05a93-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="05a93-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05a93-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05a93-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05a93-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a93-129">**StringCollection. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="05a93-129">**StringCollection.getItemInfoByType**</span></span>](stringcollection-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="05a93-130">**StringCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="05a93-130">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





