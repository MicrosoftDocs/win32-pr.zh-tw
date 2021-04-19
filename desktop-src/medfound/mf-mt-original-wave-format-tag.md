---
description: 包含音訊資料流程的原始 WAVE 格式標記。
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: 'MF_MT_ORIGINAL_WAVE_FORMAT_TAG 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba89171f9ae2bf3ab99df05bd3ae64b7d52be6d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976574"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a><span data-ttu-id="a6b02-103">MF \_ MT \_ 原始 \_ WAVE \_ 格式 \_ 標記屬性</span><span class="sxs-lookup"><span data-stu-id="a6b02-103">MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute</span></span>

<span data-ttu-id="a6b02-104">包含音訊資料流程的原始 WAVE 格式標記。</span><span class="sxs-lookup"><span data-stu-id="a6b02-104">Contains the original WAVE format tag for an audio stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="a6b02-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a6b02-105">Data type</span></span>

<span data-ttu-id="a6b02-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a6b02-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a6b02-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="a6b02-107">Get/set</span></span>

<span data-ttu-id="a6b02-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="a6b02-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a6b02-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="a6b02-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a6b02-110">適用於</span><span class="sxs-lookup"><span data-stu-id="a6b02-110">Applies to</span></span>

[<span data-ttu-id="a6b02-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a6b02-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="a6b02-112">備註</span><span class="sxs-lookup"><span data-stu-id="a6b02-112">Remarks</span></span>

<span data-ttu-id="a6b02-113">根據來源檔案，AVI 媒體來源可能會在其所提供的媒體類型上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="a6b02-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="a6b02-114">AVI 檔案包含檔案中每個資料流程的資料流程標頭。</span><span class="sxs-lookup"><span data-stu-id="a6b02-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="a6b02-115">AVI 媒體來源會將資料流程標頭轉譯為媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a6b02-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="a6b02-116">針對音訊串流，資料流程標頭包含可識別音訊格式的格式標記。</span><span class="sxs-lookup"><span data-stu-id="a6b02-116">For audio streams, the stream header contains a format tag that identifies the audio format.</span></span> <span data-ttu-id="a6b02-117"> (格式標籤包含在 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構的 **wFormatTag** 成員中 ) 。在大部分情況下，AVI 媒體來源會將格式標記直接轉換成子類型 Guid，如「[**音訊子類型 guid**](audio-subtype-guids.md)」主題所述。</span><span class="sxs-lookup"><span data-stu-id="a6b02-117">(The format tag is contained in the **wFormatTag** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.) In most cases, the AVI media source converts the format tag directly to a subtype GUID, as described in the topic [**Audio Subtype GUIDs**](audio-subtype-guids.md).</span></span> <span data-ttu-id="a6b02-118">不過，在某些情況下，它會將原始格式標記對應至另一個相等的格式標記。</span><span class="sxs-lookup"><span data-stu-id="a6b02-118">In some cases, however, it maps the original format tag to another format tag that is equivalent.</span></span> <span data-ttu-id="a6b02-119">如果是的話，媒體來源會使用 MF \_ MT \_ 原始 \_ WAVE \_ 格式 \_ 標記屬性，將原始格式標記儲存在媒體類型中。</span><span class="sxs-lookup"><span data-stu-id="a6b02-119">If so, the media source stores the original format tag in the media type, using the MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute.</span></span>

<span data-ttu-id="a6b02-120">格式對應會儲存在登錄中的下列機碼底下：</span><span class="sxs-lookup"><span data-stu-id="a6b02-120">The format mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="a6b02-121">**HKEY \_類別 \_ 根目錄** \\ **MediaFoundation** \\ **MapAudioFormatTag**</span><span class="sxs-lookup"><span data-stu-id="a6b02-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapAudioFormatTag**</span></span>

<span data-ttu-id="a6b02-122">每個專案都是 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="a6b02-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="a6b02-123">專案的名稱是格式標記的十進位標記法。</span><span class="sxs-lookup"><span data-stu-id="a6b02-123">The name of the entry is the decimal representation of the format tag.</span></span> <span data-ttu-id="a6b02-124">專案的值是相等的格式標記。</span><span class="sxs-lookup"><span data-stu-id="a6b02-124">The value of the entry is the equivalent format tag.</span></span>

<span data-ttu-id="a6b02-125">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="a6b02-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6b02-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6b02-126">Requirements</span></span>



| <span data-ttu-id="a6b02-127">需求</span><span class="sxs-lookup"><span data-stu-id="a6b02-127">Requirement</span></span> | <span data-ttu-id="a6b02-128">值</span><span class="sxs-lookup"><span data-stu-id="a6b02-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b02-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6b02-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a6b02-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6b02-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a6b02-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6b02-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a6b02-132">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6b02-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a6b02-133">標頭</span><span class="sxs-lookup"><span data-stu-id="a6b02-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6b02-134"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a6b02-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6b02-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6b02-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6b02-136">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a6b02-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a6b02-137">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="a6b02-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
