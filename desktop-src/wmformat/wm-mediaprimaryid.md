---
title: WM/MediaClassPrimaryID
description: WM/MediaClassPrimaryID 屬性包含主要媒體類別的 GUID。
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- WM/MediaClassPrimaryID windows Media 格式
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f84d987d57b1d825fac54e6a7de41b0154952e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841463"
---
# <a name="wmmediaclassprimaryid"></a><span data-ttu-id="675a7-104">WM/MediaClassPrimaryID</span><span class="sxs-lookup"><span data-stu-id="675a7-104">WM/MediaClassPrimaryID</span></span>

<span data-ttu-id="675a7-105">**WM/MediaClassPrimaryID** 屬性包含主要媒體類別的 GUID。</span><span class="sxs-lookup"><span data-stu-id="675a7-105">The **WM/MediaClassPrimaryID** attribute contains the GUID of the primary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="675a7-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="675a7-106">Global Constant</span></span>

<span data-ttu-id="675a7-107">g \_ wszWMMediaClassPrimaryID</span><span class="sxs-lookup"><span data-stu-id="675a7-107">g\_wszWMMediaClassPrimaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="675a7-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="675a7-108">Data Type</span></span>

<span data-ttu-id="675a7-109">**WMT \_ 類型 \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="675a7-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="675a7-110">備註</span><span class="sxs-lookup"><span data-stu-id="675a7-110">Remarks</span></span>

<span data-ttu-id="675a7-111">這個屬性應該設定為下表中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="675a7-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="675a7-112">主要類別 GUID</span><span class="sxs-lookup"><span data-stu-id="675a7-112">Primary class GUID</span></span>                     | <span data-ttu-id="675a7-113">Description</span><span class="sxs-lookup"><span data-stu-id="675a7-113">Description</span></span>                                                  |
|----------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="675a7-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span><span class="sxs-lookup"><span data-stu-id="675a7-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span></span> | <span data-ttu-id="675a7-115">用於音樂檔案。</span><span class="sxs-lookup"><span data-stu-id="675a7-115">Use for music files.</span></span> <span data-ttu-id="675a7-116">請勿用於非音樂的音訊。</span><span class="sxs-lookup"><span data-stu-id="675a7-116">Do not use for audio that is not music.</span></span> |
| <span data-ttu-id="675a7-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span><span class="sxs-lookup"><span data-stu-id="675a7-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span></span> | <span data-ttu-id="675a7-118">使用於影片檔案。</span><span class="sxs-lookup"><span data-stu-id="675a7-118">Use for video files.</span></span>                                         |
| <span data-ttu-id="675a7-119">"01CD0F29-DA4E-4157-897B-6275D50C4F11"</span><span class="sxs-lookup"><span data-stu-id="675a7-119">"01CD0F29-DA4E-4157-897B-6275D50C4F11"</span></span> | <span data-ttu-id="675a7-120">用於非音樂的音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="675a7-120">Use for audio files that are not music.</span></span>                      |
| <span data-ttu-id="675a7-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span><span class="sxs-lookup"><span data-stu-id="675a7-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span></span> | <span data-ttu-id="675a7-122">針對非音訊或影片的檔案使用。</span><span class="sxs-lookup"><span data-stu-id="675a7-122">Use for files that are neither audio or video.</span></span>               |



 

<span data-ttu-id="675a7-123">當您指定主要類別識別碼時，您也應該設定次要類別識別碼，以明確說明檔案中的內容類型。</span><span class="sxs-lookup"><span data-stu-id="675a7-123">When you specify a primary class identifier, you should also set a secondary class identifier to clarify the type of content in the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="675a7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="675a7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="675a7-125">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="675a7-125">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="675a7-126">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="675a7-126">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
</dt> </dl>

 

 




