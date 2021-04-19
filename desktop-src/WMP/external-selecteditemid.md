---
title: SelectedItemID
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |SelectedItemID
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- SelectedItemID Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.selectedItemID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768387c9e20082ef47cb0f502a2c4572bf462f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976552"
---
# <a name="externalselecteditemid"></a><span data-ttu-id="f0f34-105">SelectedItemID</span><span class="sxs-lookup"><span data-stu-id="f0f34-105">External.selectedItemID</span></span>

> [!Note]  
> <span data-ttu-id="f0f34-106">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="f0f34-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f0f34-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="f0f34-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f0f34-108">**SelectedItemID** 屬性會抓取 Windows Media Player 中目前選取之媒體專案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0f34-108">The **selectedItemID** property retrieves the identifier of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0f34-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0f34-109">Syntax</span></span>

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a><span data-ttu-id="f0f34-110">可能的值</span><span class="sxs-lookup"><span data-stu-id="f0f34-110">Possible Values</span></span>

<span data-ttu-id="f0f34-111">這個屬性是唯讀 **字串**。</span><span class="sxs-lookup"><span data-stu-id="f0f34-111">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0f34-112">備註</span><span class="sxs-lookup"><span data-stu-id="f0f34-112">Remarks</span></span>

<span data-ttu-id="f0f34-113">這個屬性會與 [selectedItemType](external-selecteditemtype.md) 屬性搭配使用。</span><span class="sxs-lookup"><span data-stu-id="f0f34-113">This property is used in combination with the [External.selectedItemType](external-selecteditemtype.md) property.</span></span> <span data-ttu-id="f0f34-114">例如，如果 **selectedItemType** 等於 CPTrackID，則 **selectedItemID** 是所選播放軌的識別碼。如需 Windows Media Player 如何讓線上商店內容的觀點有詳細的詳細資訊，請參閱 [位置和選取的專案](location-and-selected-item.md)。</span><span class="sxs-lookup"><span data-stu-id="f0f34-114">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="f0f34-115">Windows Media Player 中的特定視圖會有選取的特定媒體專案。</span><span class="sxs-lookup"><span data-stu-id="f0f34-115">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="f0f34-116">例如，假設目前的 view 代表專輯。</span><span class="sxs-lookup"><span data-stu-id="f0f34-116">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="f0f34-117">專輯是曲目的容器，因此 **selectedItemType** 等於 CPTrackID，而 **selectedItemID** 是所選播放軌的識別碼。其他視圖則沒有選取的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="f0f34-117">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="f0f34-118">例如，如果使用者按一下 [樹狀檢視] 控制項中的線上商店根節點，Windows Media Player 會顯示線上商店所提供的 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="f0f34-118">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="f0f34-119">播放程式不會在播放程式使用者介面中顯示任何媒體專案的容器。</span><span class="sxs-lookup"><span data-stu-id="f0f34-119">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="f0f34-120">在此情況下， **selectedItemType** 等於 unknownlocation.xsd，而 **selectedItemID** 等於空字串。</span><span class="sxs-lookup"><span data-stu-id="f0f34-120">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0f34-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0f34-121">Requirements</span></span>



| <span data-ttu-id="f0f34-122">需求</span><span class="sxs-lookup"><span data-stu-id="f0f34-122">Requirement</span></span> | <span data-ttu-id="f0f34-123">值</span><span class="sxs-lookup"><span data-stu-id="f0f34-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0f34-124">版本</span><span class="sxs-lookup"><span data-stu-id="f0f34-124">Version</span></span><br/> | <span data-ttu-id="f0f34-125">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="f0f34-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="f0f34-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f0f34-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="f0f34-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0f34-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0f34-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0f34-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0f34-129">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="f0f34-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f0f34-130">**SelectedItemType**</span><span class="sxs-lookup"><span data-stu-id="f0f34-130">**External.selectedItemType**</span></span>](external-selecteditemtype.md)
</dt> <dt>

[<span data-ttu-id="f0f34-131">**位置和選取的專案**</span><span class="sxs-lookup"><span data-stu-id="f0f34-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





