---
description: 包含影片媒體類型的元件專案。 使用這個屬性來調色盤影片格式，例如 RGB 8。
ms.assetid: 3efc124b-073e-4c48-9550-c100e29f2d6f
title: 'MF_MT_PALETTE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dcfc596ae463cf642cc462da1c73dc641356d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969321"
---
# <a name="mf_mt_palette-attribute"></a><span data-ttu-id="e12f6-104">MF \_ MT \_ 調色板屬性</span><span class="sxs-lookup"><span data-stu-id="e12f6-104">MF\_MT\_PALETTE attribute</span></span>

<span data-ttu-id="e12f6-105">包含影片媒體類型的元件專案。</span><span class="sxs-lookup"><span data-stu-id="e12f6-105">Contains the palette entries for a video media type.</span></span> <span data-ttu-id="e12f6-106">使用這個屬性來調色盤影片格式，例如 RGB 8。</span><span class="sxs-lookup"><span data-stu-id="e12f6-106">Use this attribute for palettized video formats, such as RGB 8.</span></span>

## <a name="data-type"></a><span data-ttu-id="e12f6-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="e12f6-107">Data type</span></span>

<span data-ttu-id="e12f6-108">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="e12f6-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="e12f6-109">備註</span><span class="sxs-lookup"><span data-stu-id="e12f6-109">Remarks</span></span>

<span data-ttu-id="e12f6-110">屬性資料是 [**MFPaletteEntry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) 聯集的陣列。</span><span class="sxs-lookup"><span data-stu-id="e12f6-110">The attribute data is an array of [**MFPaletteEntry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) unions.</span></span>

<span data-ttu-id="e12f6-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="e12f6-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e12f6-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e12f6-112">Requirements</span></span>



| <span data-ttu-id="e12f6-113">需求</span><span class="sxs-lookup"><span data-stu-id="e12f6-113">Requirement</span></span> | <span data-ttu-id="e12f6-114">值</span><span class="sxs-lookup"><span data-stu-id="e12f6-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e12f6-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e12f6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e12f6-116">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e12f6-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e12f6-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e12f6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e12f6-118">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e12f6-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e12f6-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e12f6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e12f6-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e12f6-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e12f6-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e12f6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e12f6-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e12f6-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e12f6-123">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="e12f6-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="e12f6-124">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="e12f6-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="e12f6-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="e12f6-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="e12f6-126">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="e12f6-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




