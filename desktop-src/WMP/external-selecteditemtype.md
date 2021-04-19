---
title: SelectedItemType
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |SelectedItemType
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- SelectedItemType Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.selectedItemType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9755f66dd00947f295bdd40ea6ab79e69d655d49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977151"
---
# <a name="externalselecteditemtype"></a><span data-ttu-id="e4993-105">SelectedItemType</span><span class="sxs-lookup"><span data-stu-id="e4993-105">External.selectedItemType</span></span>

> [!Note]  
> <span data-ttu-id="e4993-106">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="e4993-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e4993-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="e4993-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e4993-108">**SelectedItemType** 屬性會抓取 Windows Media Player 中目前選取之媒體專案的類型。</span><span class="sxs-lookup"><span data-stu-id="e4993-108">The **selectedItemType** property retrieves the type of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4993-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4993-109">Syntax</span></span>

<span data-ttu-id="e4993-110">selectedItemType () </span><span class="sxs-lookup"><span data-stu-id="e4993-110">window.external.selectedItemType()</span></span>

## <a name="possible-values"></a><span data-ttu-id="e4993-111">可能的值</span><span class="sxs-lookup"><span data-stu-id="e4993-111">Possible Values</span></span>

<span data-ttu-id="e4993-112">這個屬性是唯讀 **字串** ，其中包含其中一個連結 [庫位置常數](library-location-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="e4993-112">This property is a read-only **String** that contains one of the [library location constants](library-location-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4993-113">備註</span><span class="sxs-lookup"><span data-stu-id="e4993-113">Remarks</span></span>

<span data-ttu-id="e4993-114">這個屬性會與 **selectedItemID** 屬性搭配使用。</span><span class="sxs-lookup"><span data-stu-id="e4993-114">This property is used in combination with the **External.selectedItemID** property.</span></span> <span data-ttu-id="e4993-115">例如，如果 **selectedItemType** 等於 CPTrackID，則 **selectedItemID** 是所選播放軌的識別碼。如需 Windows Media Player 如何讓線上商店內容的觀點有詳細的詳細資訊，請參閱 [位置和選取的專案](location-and-selected-item.md)。</span><span class="sxs-lookup"><span data-stu-id="e4993-115">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="e4993-116">Windows Media Player 中的特定視圖會有選取的特定媒體專案。</span><span class="sxs-lookup"><span data-stu-id="e4993-116">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="e4993-117">例如，假設目前的 view 代表專輯。</span><span class="sxs-lookup"><span data-stu-id="e4993-117">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="e4993-118">專輯是曲目的容器，因此 **selectedItemType** 等於 CPTrackID，而 **selectedItemID** 是所選播放軌的識別碼。其他視圖則沒有選取的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="e4993-118">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="e4993-119">例如，如果使用者按一下 [樹狀檢視] 控制項中的線上商店根節點，Windows Media Player 會顯示線上商店所提供的 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="e4993-119">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="e4993-120">播放程式不會在播放程式使用者介面中顯示任何媒體專案的容器。</span><span class="sxs-lookup"><span data-stu-id="e4993-120">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="e4993-121">在此情況下， **selectedItemType** 等於 unknownlocation.xsd，而 **selectedItemID** 等於空字串。</span><span class="sxs-lookup"><span data-stu-id="e4993-121">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4993-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4993-122">Requirements</span></span>



| <span data-ttu-id="e4993-123">需求</span><span class="sxs-lookup"><span data-stu-id="e4993-123">Requirement</span></span> | <span data-ttu-id="e4993-124">值</span><span class="sxs-lookup"><span data-stu-id="e4993-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4993-125">版本</span><span class="sxs-lookup"><span data-stu-id="e4993-125">Version</span></span><br/> | <span data-ttu-id="e4993-126">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="e4993-126">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="e4993-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e4993-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="e4993-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4993-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4993-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4993-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4993-130">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="e4993-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e4993-131">**SelectedItemID**</span><span class="sxs-lookup"><span data-stu-id="e4993-131">**External.selectedItemID**</span></span>](external-selecteditemid.md)
</dt> <dt>

[<span data-ttu-id="e4993-132">**位置和選取的專案**</span><span class="sxs-lookup"><span data-stu-id="e4993-132">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





