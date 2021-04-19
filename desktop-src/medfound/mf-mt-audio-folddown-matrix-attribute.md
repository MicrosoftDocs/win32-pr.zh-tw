---
description: 指定音訊解碼器如何將多頻道音訊轉換成身歷聲輸出。 此程式也稱為折迭。
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: 'MF_MT_AUDIO_FOLDDOWN_MATRIX 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bb8aa00835ab31f6c05eaa9a1d0e5d9d126b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977222"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a><span data-ttu-id="a83d4-104">MF \_ MT \_ 音訊 \_ FOLDDOWN \_ 矩陣屬性</span><span class="sxs-lookup"><span data-stu-id="a83d4-104">MF\_MT\_AUDIO\_FOLDDOWN\_MATRIX attribute</span></span>

<span data-ttu-id="a83d4-105">指定音訊解碼器如何將多頻道音訊轉換成身歷聲輸出。</span><span class="sxs-lookup"><span data-stu-id="a83d4-105">Specifies how an audio decoder should transform multichannel audio to stereo output.</span></span> <span data-ttu-id="a83d4-106">此程式也稱為 *折* 迭。</span><span class="sxs-lookup"><span data-stu-id="a83d4-106">This process is also called *fold-down*.</span></span>

## <a name="data-type"></a><span data-ttu-id="a83d4-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="a83d4-107">Data type</span></span>

<span data-ttu-id="a83d4-108">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="a83d4-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="a83d4-109">備註</span><span class="sxs-lookup"><span data-stu-id="a83d4-109">Remarks</span></span>

<span data-ttu-id="a83d4-110">這個屬性會套用到音訊媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a83d4-110">This attribute applies to audio media types.</span></span>

<span data-ttu-id="a83d4-111">這個屬性的值是 [**MFFOLDDOWN \_ 矩陣**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) 結構。</span><span class="sxs-lookup"><span data-stu-id="a83d4-111">The value of this attribute is an [**MFFOLDDOWN\_MATRIX**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) structure.</span></span>

<span data-ttu-id="a83d4-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="a83d4-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a83d4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a83d4-113">Requirements</span></span>



| <span data-ttu-id="a83d4-114">需求</span><span class="sxs-lookup"><span data-stu-id="a83d4-114">Requirement</span></span> | <span data-ttu-id="a83d4-115">值</span><span class="sxs-lookup"><span data-stu-id="a83d4-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a83d4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a83d4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a83d4-117">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a83d4-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a83d4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a83d4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a83d4-119">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a83d4-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a83d4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="a83d4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a83d4-121"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a83d4-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a83d4-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a83d4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a83d4-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a83d4-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a83d4-124">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="a83d4-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="a83d4-125">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="a83d4-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="a83d4-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a83d4-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a83d4-127">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="a83d4-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




