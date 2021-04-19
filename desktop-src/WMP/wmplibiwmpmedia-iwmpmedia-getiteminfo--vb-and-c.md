---
title: IWMPMedia getItemInfo 方法
description: GetItemInfo 方法會針對媒體專案傳回指定之屬性的值。
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523e57e68d13df55395cd4deca6e09904723bbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984424"
---
# <a name="iwmpmediagetiteminfo-method"></a><span data-ttu-id="1d424-106">IWMPMedia：： getItemInfo 方法</span><span class="sxs-lookup"><span data-stu-id="1d424-106">IWMPMedia::getItemInfo method</span></span>

<span data-ttu-id="1d424-107">**GetItemInfo** 方法會針對媒體專案傳回指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1d424-107">The **getItemInfo** method returns the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d424-108">語法</span><span class="sxs-lookup"><span data-stu-id="1d424-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="1d424-109">參數</span><span class="sxs-lookup"><span data-stu-id="1d424-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d424-110">*bstrItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1d424-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d424-111">**System.string** ，它是屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d424-111">A **System.String** that is the name of the attribute.</span></span> <span data-ttu-id="1d424-112">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="1d424-112">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d424-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d424-113">Return value</span></span>

<span data-ttu-id="1d424-114">**System.string** ，這是指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1d424-114">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d424-115">備註</span><span class="sxs-lookup"><span data-stu-id="1d424-115">Remarks</span></span>

<span data-ttu-id="1d424-116">這個方法會傳回個別媒體專案的中繼資料，或屬於播放清單一部分的媒體專案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1d424-116">This method returns the metadata for an individual media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="1d424-117">**AttributeCount** 屬性會取得指定媒體專案可用的屬性名稱數目。</span><span class="sxs-lookup"><span data-stu-id="1d424-117">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="1d424-118">然後，您可以搭配 **getAttributeName** 方法使用索引編號來判斷每個可用屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d424-118">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="1d424-119">可以將個別的屬性名稱傳遞給 **getItemInfo**。</span><span class="sxs-lookup"><span data-stu-id="1d424-119">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="1d424-120">若要使用具有複雜值的多個值和屬性來取得屬性，請使用 **getItemInfoByType** 方法。</span><span class="sxs-lookup"><span data-stu-id="1d424-120">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="1d424-121">如果媒體專案來自呼叫 [IWMPLibrary mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)所抓取的程式庫，可用屬性的集合就會與可透過呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)所抓取的本機程式庫查詢的不同。</span><span class="sxs-lookup"><span data-stu-id="1d424-121">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="1d424-122">例如，使用 **IWMPLibrary** 抓取的本機程式庫中所提供的屬性，將會是使用 **IWMPCore** 抓取之本機程式庫中可用屬性的子集。</span><span class="sxs-lookup"><span data-stu-id="1d424-122">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **IWMPCore**.</span></span> <span data-ttu-id="1d424-123">其他來源 (遠端程式庫、可攜式裝置或 Cd) 的可用屬性集是由其他來源所定義。</span><span class="sxs-lookup"><span data-stu-id="1d424-123">The set of attributes available from other sources (remote libraries, portable devices, or CDs) is defined by the other sources.</span></span>

<span data-ttu-id="1d424-124">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="1d424-124">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="1d424-125">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="1d424-125">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d424-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d424-126">Requirements</span></span>



| <span data-ttu-id="1d424-127">需求</span><span class="sxs-lookup"><span data-stu-id="1d424-127">Requirement</span></span> | <span data-ttu-id="1d424-128">值</span><span class="sxs-lookup"><span data-stu-id="1d424-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d424-129">版本</span><span class="sxs-lookup"><span data-stu-id="1d424-129">Version</span></span><br/>   | <span data-ttu-id="1d424-130">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="1d424-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1d424-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="1d424-131">Namespace</span></span><br/> | <span data-ttu-id="1d424-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1d424-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1d424-133">組件</span><span class="sxs-lookup"><span data-stu-id="1d424-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1d424-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="1d424-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d424-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d424-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d424-136">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="1d424-136">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="1d424-137">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1d424-137">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1d424-138">**IWMPMedia. attributeCount (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1d424-138">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1d424-139">**IWMPMedia. getAttributeName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1d424-139">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1d424-140">**IWMPMedia. setItemInfo (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1d424-140">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1d424-141">**IWMPMedia3. getItemInfoByType (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1d424-141">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





