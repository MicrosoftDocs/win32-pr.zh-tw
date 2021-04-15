---
title: MetadataPicture 物件
description: MetadataPicture 物件會提供一種方式來取出 WM/圖片中繼資料屬性的值。 這個屬性會對應至包含在數位媒體檔案中的專輯封面，而不是透過網際網路下載的專輯封面。
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- MetadataPicture 物件 Windows Media Player
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 892b162ba05ab43740565c849b00bc4e3c52aad6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463553"
---
# <a name="metadatapicture-object"></a><span data-ttu-id="6efa5-105">MetadataPicture 物件</span><span class="sxs-lookup"><span data-stu-id="6efa5-105">MetadataPicture Object</span></span>

<span data-ttu-id="6efa5-106">**MetadataPicture** 物件會提供一種方式來取出 [**WM/圖片**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)中繼資料屬性的值。</span><span class="sxs-lookup"><span data-stu-id="6efa5-106">The **MetadataPicture** object provides a way to retrieve the values of the [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) metadata attribute.</span></span> <span data-ttu-id="6efa5-107">這個屬性會對應至包含在數位媒體檔案中的專輯封面，而不是透過網際網路下載的專輯封面。</span><span class="sxs-lookup"><span data-stu-id="6efa5-107">This attribute corresponds to album art contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="6efa5-108">**MetadataPicture** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="6efa5-108">The **MetadataPicture** object supports the following properties.</span></span>



| <span data-ttu-id="6efa5-109">屬性</span><span class="sxs-lookup"><span data-stu-id="6efa5-109">Property</span></span>                                           | <span data-ttu-id="6efa5-110">描述</span><span class="sxs-lookup"><span data-stu-id="6efa5-110">Description</span></span>                                       |
|----------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="6efa5-111">**描述**</span><span class="sxs-lookup"><span data-stu-id="6efa5-111">**description**</span></span>](metadatapicture-description.md) | <span data-ttu-id="6efa5-112">捕獲中繼資料影像的描述。</span><span class="sxs-lookup"><span data-stu-id="6efa5-112">Retrieves a description of the metadata image.</span></span>    |
| [<span data-ttu-id="6efa5-113">**mimeType**</span><span class="sxs-lookup"><span data-stu-id="6efa5-113">**mimeType**</span></span>](metadatapicture-mimetype.md)       | <span data-ttu-id="6efa5-114">捕獲中繼資料影像的 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="6efa5-114">Retrieves the MIME type of the metadata image.</span></span>    |
| [<span data-ttu-id="6efa5-115">**pictureType**</span><span class="sxs-lookup"><span data-stu-id="6efa5-115">**pictureType**</span></span>](metadatapicture-picturetype.md) | <span data-ttu-id="6efa5-116">捕獲中繼資料影像的圖片類型。</span><span class="sxs-lookup"><span data-stu-id="6efa5-116">Retrieves the picture type of the metadata image.</span></span> |
| [<span data-ttu-id="6efa5-117">**URL**</span><span class="sxs-lookup"><span data-stu-id="6efa5-117">**URL**</span></span>](metadatapicture-url.md)                 | <span data-ttu-id="6efa5-118">僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="6efa5-118">Internal use only.</span></span>                                |



 

<span data-ttu-id="6efa5-119">**MetadataPicture** 物件是透過下列方法來存取。</span><span class="sxs-lookup"><span data-stu-id="6efa5-119">The **MetadataPicture** object is accessed through the following method.</span></span>



| <span data-ttu-id="6efa5-120">Object</span><span class="sxs-lookup"><span data-stu-id="6efa5-120">Object</span></span>                        | <span data-ttu-id="6efa5-121">方法</span><span class="sxs-lookup"><span data-stu-id="6efa5-121">Method</span></span>                                               |
|-------------------------------|------------------------------------------------------|
| [<span data-ttu-id="6efa5-122">**媒體**</span><span class="sxs-lookup"><span data-stu-id="6efa5-122">**Media**</span></span>](media-object.md) | [<span data-ttu-id="6efa5-123">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="6efa5-123">**getItemInfoByType**</span></span>](media-getiteminfobytype.md) |



 

<span data-ttu-id="6efa5-124">為了方便說明， `player.currentMedia.getItemInfoByType(name, language, index)` 在參考語法區段中使用。</span><span class="sxs-lookup"><span data-stu-id="6efa5-124">For purposes of illustration, `player.currentMedia.getItemInfoByType(name, language, index)` is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="6efa5-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6efa5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6efa5-126">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="6efa5-126">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 