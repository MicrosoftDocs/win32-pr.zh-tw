---
title: LibraryLocationID
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |LibraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- LibraryLocationID Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f411ad8575bc7419cf9300d1aab46073ee869c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986170"
---
# <a name="externallibrarylocationid"></a><span data-ttu-id="dc263-105">LibraryLocationID</span><span class="sxs-lookup"><span data-stu-id="dc263-105">External.libraryLocationID</span></span>

> [!Note]  
> <span data-ttu-id="dc263-106">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="dc263-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="dc263-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="dc263-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="dc263-108">**LibraryLocationID** 屬性會抓取目前顯示在播放程式視圖中的特定媒體專案識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc263-108">The **libraryLocationID** property retrieves the identifier of the specific media item that is currently displayed in the Player's view.</span></span>

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a><span data-ttu-id="dc263-109">可能的值</span><span class="sxs-lookup"><span data-stu-id="dc263-109">Possible Values</span></span>

<span data-ttu-id="dc263-110">這個屬性是唯讀 **字串**。</span><span class="sxs-lookup"><span data-stu-id="dc263-110">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc263-111">備註</span><span class="sxs-lookup"><span data-stu-id="dc263-111">Remarks</span></span>

<span data-ttu-id="dc263-112">這個屬性與 [libraryLocationType](external-librarylocationtype.md) 屬性搭配使用。</span><span class="sxs-lookup"><span data-stu-id="dc263-112">This property works in combination with the [External.libraryLocationType](external-librarylocationtype.md) property.</span></span> <span data-ttu-id="dc263-113">例如，假設 **libraryLocationType** 等於 CPAlbumID，而 **libraryLocationID** 等於3。</span><span class="sxs-lookup"><span data-stu-id="dc263-113">For example, suppose **libraryLocationType** is equal to CPAlbumID and **libraryLocationID** is equal to 3.</span></span> <span data-ttu-id="dc263-114">這表示 Windows Media Player 中的目前視圖顯示識別碼為3的專輯。</span><span class="sxs-lookup"><span data-stu-id="dc263-114">That means the current view in Windows Media Player is showing the album that has an ID of 3.</span></span> <span data-ttu-id="dc263-115">如需 Windows Media Player 如何讓線上商店內容的觀點有詳細的詳細資訊，請參閱 [位置和選取的專案](location-and-selected-item.md)。</span><span class="sxs-lookup"><span data-stu-id="dc263-115">For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="dc263-116">Windows Media Player 中的特定視圖會與特定媒體專案相關聯。</span><span class="sxs-lookup"><span data-stu-id="dc263-116">Certain views in Windows Media Player are associated with a particular media item.</span></span> <span data-ttu-id="dc263-117">例如，如果目前的視圖代表個別的專輯，則 **libraryLocationType** 等於 CPAlbumID，而 **libraryLocationID** 是專輯的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc263-117">For example, if the current view represents an individual album, **libraryLocationType** is equal to CPAlbumID, and **libraryLocationID** is the ID of the album.</span></span> <span data-ttu-id="dc263-118">其他的視圖則不會與任何特定媒體專案相關聯。</span><span class="sxs-lookup"><span data-stu-id="dc263-118">Other views are not associated with any particular media item.</span></span> <span data-ttu-id="dc263-119">例如，如果目前的 view 代表所有專輯， **libraryLocationType** 等於 AllCPAlbumIDs，但沒有可指派給 **libraryLocationID** 的有意義的值。</span><span class="sxs-lookup"><span data-stu-id="dc263-119">For example, if the current view represents all albums, **libraryLocationType** is equal to AllCPAlbumIDs, but there is no meaningful value that can be assigned to **libraryLocationID**.</span></span> <span data-ttu-id="dc263-120">在 **libraryLocationID** 屬性沒有任何有意義的值的情況下，它等於空字串。</span><span class="sxs-lookup"><span data-stu-id="dc263-120">In cases where the **libraryLocationID** property has no meaningful value, it is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc263-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc263-121">Requirements</span></span>



| <span data-ttu-id="dc263-122">需求</span><span class="sxs-lookup"><span data-stu-id="dc263-122">Requirement</span></span> | <span data-ttu-id="dc263-123">值</span><span class="sxs-lookup"><span data-stu-id="dc263-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dc263-124">版本</span><span class="sxs-lookup"><span data-stu-id="dc263-124">Version</span></span><br/> | <span data-ttu-id="dc263-125">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="dc263-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="dc263-126">DLL</span><span class="sxs-lookup"><span data-stu-id="dc263-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="dc263-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc263-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc263-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc263-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc263-129">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="dc263-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="dc263-130">**LibraryLocationType**</span><span class="sxs-lookup"><span data-stu-id="dc263-130">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="dc263-131">**位置和選取的專案**</span><span class="sxs-lookup"><span data-stu-id="dc263-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





