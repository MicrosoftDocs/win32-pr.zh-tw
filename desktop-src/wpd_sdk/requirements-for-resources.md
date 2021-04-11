---
description: 資源的需求
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: 資源的需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5702555704137f4280e527f0fc26f176435238ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193933"
---
# <a name="requirements-for-resources"></a><span data-ttu-id="3156e-103">資源的需求</span><span class="sxs-lookup"><span data-stu-id="3156e-103">Requirements for Resources</span></span>

<span data-ttu-id="3156e-104">Windows 可攜式裝置會將下列資源類別定義為 **PROPERTYKEY** 值。</span><span class="sxs-lookup"><span data-stu-id="3156e-104">Windows Portable Devices defines the following resource categories as **PROPERTYKEY** values.</span></span> <span data-ttu-id="3156e-105">這些值是用來描述物件中的個別資源。</span><span class="sxs-lookup"><span data-stu-id="3156e-105">These values are used to describe individual resources in an object.</span></span> <span data-ttu-id="3156e-106">屬性索引鍵的 *pid* 成員可以不同，以描述相同類型之相同類型的不同資源，但 **WPD \_ 資源 \_ 預設** 除外，但只能描述一項資源。</span><span class="sxs-lookup"><span data-stu-id="3156e-106">The *pid* member of the property key can be different to describe different resources of the same type for all types except **WPD\_RESOURCE\_DEFAULT**, which can only describe one resource.</span></span> <span data-ttu-id="3156e-107">每個資源類型的連結描述頁面會列出該資源所支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="3156e-107">The linked description page for each resource type lists the attributes supported by that resource.</span></span>



| <span data-ttu-id="3156e-108">資源 PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="3156e-108">Resource PROPERTYKEY</span></span>                                                | <span data-ttu-id="3156e-109">Description</span><span class="sxs-lookup"><span data-stu-id="3156e-109">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3156e-110">**WPD \_ 資源 \_ 預設**</span><span class="sxs-lookup"><span data-stu-id="3156e-110">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md)              | <span data-ttu-id="3156e-111">指定物件後方的整個檔案。</span><span class="sxs-lookup"><span data-stu-id="3156e-111">Specifies the whole file behind the object.</span></span> <span data-ttu-id="3156e-112">這是具有資源之任何物件的唯一必要資源。</span><span class="sxs-lookup"><span data-stu-id="3156e-112">This is the only required resource for any object with a resource.</span></span> |
| [<span data-ttu-id="3156e-113">**WPD \_ 資源 \_ 專輯 \_ 封面**</span><span class="sxs-lookup"><span data-stu-id="3156e-113">**WPD\_RESOURCE\_ALBUM\_ART**</span></span>](wpd-resource-album-art.md)         | <span data-ttu-id="3156e-114">指定代表物件之專輯作品的影像。</span><span class="sxs-lookup"><span data-stu-id="3156e-114">Specifies an image that represents the album artwork for the object.</span></span>                                           |
| [<span data-ttu-id="3156e-115">**WPD \_ 資源 \_ 音訊 \_ 剪輯**</span><span class="sxs-lookup"><span data-stu-id="3156e-115">**WPD\_RESOURCE\_AUDIO\_CLIP**</span></span>](wpd-resource-audio-clip.md)       | <span data-ttu-id="3156e-116">指定物件的音訊剪輯。</span><span class="sxs-lookup"><span data-stu-id="3156e-116">Specifies an audio clip for the object.</span></span>                                                                        |
| [<span data-ttu-id="3156e-117">**WPD \_ 資源 \_ 連絡人 \_ 相片**</span><span class="sxs-lookup"><span data-stu-id="3156e-117">**WPD\_RESOURCE\_CONTACT\_PHOTO**</span></span>](wpd-resource-contact-photo.md) | <span data-ttu-id="3156e-118">指定代表 contact 物件中所參考之個別相片的影像。</span><span class="sxs-lookup"><span data-stu-id="3156e-118">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>                |
| [<span data-ttu-id="3156e-119">**WPD \_ 資源 \_ 泛型**</span><span class="sxs-lookup"><span data-stu-id="3156e-119">**WPD\_RESOURCE\_GENERIC**</span></span>](wpd-resource-generic.md)              | <span data-ttu-id="3156e-120">未定義資料類型的一般資源。</span><span class="sxs-lookup"><span data-stu-id="3156e-120">A generic resource of undefined data type.</span></span> <span data-ttu-id="3156e-121">這應該被視為位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="3156e-121">This should be treated as a byte array.</span></span>                             |
| [<span data-ttu-id="3156e-122">**WPD \_ 資源 \_ 圖示**</span><span class="sxs-lookup"><span data-stu-id="3156e-122">**WPD\_RESOURCE\_ICON**</span></span>](wpd-resource-icon.md)                    | <span data-ttu-id="3156e-123">圖示。</span><span class="sxs-lookup"><span data-stu-id="3156e-123">An icon.</span></span>                                                                                                       |
| [<span data-ttu-id="3156e-124">**WPD \_ 資源 \_ 縮圖**</span><span class="sxs-lookup"><span data-stu-id="3156e-124">**WPD\_RESOURCE\_THUMBNAIL**</span></span>](wpd-resource-thumbnail.md)          | <span data-ttu-id="3156e-125">縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="3156e-125">A thumbnail image.</span></span>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="3156e-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="3156e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3156e-127">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="3156e-127">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



