---
title: 'IWMPMetadataPicture (VB 和 C ) 介面 (h.264. h) '
description: 提供屬性，以取得以 WM/Picturemetadata 屬性工作表示之數位媒體檔案中包含之影像的相關資訊。
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- IWMPMetadataPicture (VB 和 C ) 介面 Windows Media Player
- IWMPMetadataPicture (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b462c431a136745974dcde5716c3bd81226f15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995029"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a><span data-ttu-id="8bc34-105">IWMPMetadataPicture (VB 和 c # ) 介面</span><span class="sxs-lookup"><span data-stu-id="8bc34-105">IWMPMetadataPicture (VB and C#) interface</span></span>

<span data-ttu-id="8bc34-106">提供屬性，以取得以 [**WM/圖片**](/windows/desktop/wmformat/wmpicture)中繼資料屬性工作表示之數位媒體檔案中包含之影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8bc34-106">Provides properties for getting information about the image contained in a digital media file that is represented by a [**WM/Picture**](/windows/desktop/wmformat/wmpicture)metadata attribute.</span></span> <span data-ttu-id="8bc34-107">這個屬性會對應至數位媒體檔案中包含的專輯封面影像，而不是透過網際網路下載的專輯封面。</span><span class="sxs-lookup"><span data-stu-id="8bc34-107">This attribute corresponds to album art images contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="8bc34-108">**IWMPMetadataPicture** 介面會公開下列屬性。</span><span class="sxs-lookup"><span data-stu-id="8bc34-108">The **IWMPMetadataPicture** interface exposes the following properties.</span></span>



| <span data-ttu-id="8bc34-109">屬性</span><span class="sxs-lookup"><span data-stu-id="8bc34-109">Property</span></span>                                                                                   | <span data-ttu-id="8bc34-110">描述</span><span class="sxs-lookup"><span data-stu-id="8bc34-110">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="8bc34-111">**描述**</span><span class="sxs-lookup"><span data-stu-id="8bc34-111">**Description**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | <span data-ttu-id="8bc34-112">取得中繼資料屬性所代表之影像的描述。</span><span class="sxs-lookup"><span data-stu-id="8bc34-112">Gets the description of the image represented by the metadata attribute.</span></span>  |
| [<span data-ttu-id="8bc34-113">**mimeType**</span><span class="sxs-lookup"><span data-stu-id="8bc34-113">**mimeType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | <span data-ttu-id="8bc34-114">取得中繼資料屬性所代表之影像的 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="8bc34-114">Gets the MIME type of the image represented by the metadata attribute.</span></span>    |
| [<span data-ttu-id="8bc34-115">**pictureType**</span><span class="sxs-lookup"><span data-stu-id="8bc34-115">**pictureType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | <span data-ttu-id="8bc34-116">取得中繼資料屬性所代表之影像的圖片類型。</span><span class="sxs-lookup"><span data-stu-id="8bc34-116">Gets the picture type of the image represented by the metadata attribute.</span></span> |
| [<span data-ttu-id="8bc34-117">**URL**</span><span class="sxs-lookup"><span data-stu-id="8bc34-117">**URL**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | <span data-ttu-id="8bc34-118">僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="8bc34-118">Internal use only.</span></span>                                                        |



 

<span data-ttu-id="8bc34-119">取得 **IWMPMetadataPicture** 介面，方法是將屬性名稱 [**WM/圖片**](/windows/desktop/wmformat/wmpicture) 傳入下列方法，並轉換傳回的物件。</span><span class="sxs-lookup"><span data-stu-id="8bc34-119">Get an **IWMPMetadataPicture** interface by passing in the attribute name [**WM/Picture**](/windows/desktop/wmformat/wmpicture) to the following method and casting the object that is returned.</span></span>



| <span data-ttu-id="8bc34-120">介面</span><span class="sxs-lookup"><span data-stu-id="8bc34-120">Interface</span></span>                                  | <span data-ttu-id="8bc34-121">屬性</span><span class="sxs-lookup"><span data-stu-id="8bc34-121">Property</span></span>                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bc34-122">**IWMPMedia3**</span><span class="sxs-lookup"><span data-stu-id="8bc34-122">**IWMPMedia3**</span></span>](iwmpmedia3--vb-and-c.md) | [<span data-ttu-id="8bc34-123">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="8bc34-123">**getItemInfoByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a><span data-ttu-id="8bc34-124">成員</span><span class="sxs-lookup"><span data-stu-id="8bc34-124">Members</span></span>

<span data-ttu-id="8bc34-125">**IWMPMetadataPicture (VB 和 c # )** 介面不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="8bc34-125">The **IWMPMetadataPicture (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bc34-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bc34-126">Requirements</span></span>



| <span data-ttu-id="8bc34-127">需求</span><span class="sxs-lookup"><span data-stu-id="8bc34-127">Requirement</span></span> | <span data-ttu-id="8bc34-128">值</span><span class="sxs-lookup"><span data-stu-id="8bc34-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8bc34-129">標頭</span><span class="sxs-lookup"><span data-stu-id="8bc34-129">Header</span></span><br/> | <dl> <span data-ttu-id="8bc34-130"><dt>Wmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="8bc34-130"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bc34-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bc34-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bc34-132">**適用于 Visual Basic .NET 和 C 的介面#**</span><span class="sxs-lookup"><span data-stu-id="8bc34-132">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

