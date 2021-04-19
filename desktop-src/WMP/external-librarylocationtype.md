---
title: LibraryLocationType
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |LibraryLocationType
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- LibraryLocationType Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c2f14940a2ad41bed24493396e2bacfba2f0a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977591"
---
# <a name="externallibrarylocationtype"></a><span data-ttu-id="b975d-105">LibraryLocationType</span><span class="sxs-lookup"><span data-stu-id="b975d-105">External.libraryLocationType</span></span>

> [!Note]  
> <span data-ttu-id="b975d-106">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="b975d-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b975d-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="b975d-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b975d-108">**LibraryLocationType** 屬性會抓取連結 [庫位置常數](library-location-constants.md)，指出 Windows Media Player 中目前視圖的型別。</span><span class="sxs-lookup"><span data-stu-id="b975d-108">The **libraryLocationType** property retrieves a [library location constant](library-location-constants.md) that indicates the type of the current view in Windows Media Player.</span></span>

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a><span data-ttu-id="b975d-109">可能的值</span><span class="sxs-lookup"><span data-stu-id="b975d-109">Possible Values</span></span>

<span data-ttu-id="b975d-110">這個屬性是唯讀 **字串** ，其中包含其中一個程式庫位置常數。</span><span class="sxs-lookup"><span data-stu-id="b975d-110">This property is a read-only **String** that contains one of the library location constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="b975d-111">備註</span><span class="sxs-lookup"><span data-stu-id="b975d-111">Remarks</span></span>

<span data-ttu-id="b975d-112">這個屬性與 [libraryLocationID](external-librarylocationid.md) 屬性搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b975d-112">This property works in combination with the [External.libraryLocationID](external-librarylocationid.md) property.</span></span> <span data-ttu-id="b975d-113">例如，假設 **libraryLocationType** 等於 CPAlbumID，而 **libraryLocationID** 等於3。</span><span class="sxs-lookup"><span data-stu-id="b975d-113">For example, suppose **libraryLocationType** is equal to CPAlbumID and **libraryLocationID** is equal to 3.</span></span> <span data-ttu-id="b975d-114">這表示 Windows Media Player 中的目前視圖顯示識別碼為3的專輯。</span><span class="sxs-lookup"><span data-stu-id="b975d-114">That means the current view in Windows Media Player is showing the album that has an ID of 3.</span></span> <span data-ttu-id="b975d-115">如需 Windows Media Player 如何讓線上商店內容的觀點有詳細的詳細資訊，請參閱 [位置和選取的專案](location-and-selected-item.md)。</span><span class="sxs-lookup"><span data-stu-id="b975d-115">For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b975d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b975d-116">Requirements</span></span>



| <span data-ttu-id="b975d-117">需求</span><span class="sxs-lookup"><span data-stu-id="b975d-117">Requirement</span></span> | <span data-ttu-id="b975d-118">值</span><span class="sxs-lookup"><span data-stu-id="b975d-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b975d-119">版本</span><span class="sxs-lookup"><span data-stu-id="b975d-119">Version</span></span><br/> | <span data-ttu-id="b975d-120">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="b975d-120">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="b975d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b975d-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="b975d-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b975d-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b975d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b975d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b975d-124">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="b975d-124">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="b975d-125">**LibraryLocationID**</span><span class="sxs-lookup"><span data-stu-id="b975d-125">**External.libraryLocationID**</span></span>](external-librarylocationid.md)
</dt> <dt>

[<span data-ttu-id="b975d-126">**位置和選取的專案**</span><span class="sxs-lookup"><span data-stu-id="b975d-126">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





