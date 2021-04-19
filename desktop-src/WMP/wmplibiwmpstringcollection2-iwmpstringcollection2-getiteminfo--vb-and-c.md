---
title: IWMPStringCollection2 getItemInfo 方法
description: GetItemInfo 方法會傳回與指定的字串集合專案索引和名稱對應的字串。
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，IWMPStringCollection2 介面
- IWMPStringCollection2 介面 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4741c4a3ba74b03038974d8b66bc42c23830ebb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990971"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a><span data-ttu-id="dff33-106">IWMPStringCollection2：： getItemInfo 方法</span><span class="sxs-lookup"><span data-stu-id="dff33-106">IWMPStringCollection2::getItemInfo method</span></span>

<span data-ttu-id="dff33-107">**GetItemInfo** 方法會傳回與指定的字串集合專案索引和名稱對應的字串。</span><span class="sxs-lookup"><span data-stu-id="dff33-107">The **getItemInfo** method returns the string corresponding to the specified string collection item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="dff33-108">語法</span><span class="sxs-lookup"><span data-stu-id="dff33-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="dff33-109">參數</span><span class="sxs-lookup"><span data-stu-id="dff33-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dff33-110">*lCollectionIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dff33-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dff33-111">指定要從中取得屬性之字串收集項的以零為基底之索引的 **system.object。**</span><span class="sxs-lookup"><span data-stu-id="dff33-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="dff33-112">*bstrItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dff33-112">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dff33-113">做為屬性名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="dff33-113">The **System.String** that is the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dff33-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="dff33-114">Return value</span></span>

<span data-ttu-id="dff33-115">System.string **，這個字串是** 字串收集項目的名稱。</span><span class="sxs-lookup"><span data-stu-id="dff33-115">The **System.String** that is the name of the string collection item.</span></span> <span data-ttu-id="dff33-116">對於其基礎值為 system.string 的 **屬性，它會傳回** 字串 "true" 或 "false"。</span><span class="sxs-lookup"><span data-stu-id="dff33-116">For attributes whose underlying value is **System.Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="dff33-117">備註</span><span class="sxs-lookup"><span data-stu-id="dff33-117">Remarks</span></span>

<span data-ttu-id="dff33-118">若要使用具有複雜值的多個值和屬性來取得屬性，請使用 **getItemInfoByType** 方法。</span><span class="sxs-lookup"><span data-stu-id="dff33-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="dff33-119">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="dff33-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="dff33-120">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="dff33-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dff33-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="dff33-121">Requirements</span></span>



| <span data-ttu-id="dff33-122">需求</span><span class="sxs-lookup"><span data-stu-id="dff33-122">Requirement</span></span> | <span data-ttu-id="dff33-123">值</span><span class="sxs-lookup"><span data-stu-id="dff33-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dff33-124">版本</span><span class="sxs-lookup"><span data-stu-id="dff33-124">Version</span></span><br/>   | <span data-ttu-id="dff33-125">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="dff33-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="dff33-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="dff33-126">Namespace</span></span><br/> | <span data-ttu-id="dff33-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dff33-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dff33-128">組件</span><span class="sxs-lookup"><span data-stu-id="dff33-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dff33-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="dff33-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dff33-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dff33-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff33-131">**IWMPStringCollection2 介面**</span><span class="sxs-lookup"><span data-stu-id="dff33-131">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dff33-132">**IWMPStringCollection2. getItemInfoByType (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="dff33-132">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





