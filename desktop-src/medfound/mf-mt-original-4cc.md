---
description: 包含影片資料流程的原始編解碼器 FOURCC。
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: 'MF_MT_ORIGINAL_4CC 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944908"
---
# <a name="mf_mt_original_4cc-attribute"></a><span data-ttu-id="e3c37-103">MF \_ MT \_ 原始 \_ 4CC 屬性</span><span class="sxs-lookup"><span data-stu-id="e3c37-103">MF\_MT\_ORIGINAL\_4CC attribute</span></span>

<span data-ttu-id="e3c37-104">包含影片資料流程的原始編解碼器 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="e3c37-104">Contains the original codec FOURCC for a video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="e3c37-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e3c37-105">Data type</span></span>

<span data-ttu-id="e3c37-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e3c37-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e3c37-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="e3c37-107">Get/set</span></span>

<span data-ttu-id="e3c37-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="e3c37-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e3c37-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="e3c37-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e3c37-110">適用於</span><span class="sxs-lookup"><span data-stu-id="e3c37-110">Applies to</span></span>

[<span data-ttu-id="e3c37-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="e3c37-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="e3c37-112">備註</span><span class="sxs-lookup"><span data-stu-id="e3c37-112">Remarks</span></span>

<span data-ttu-id="e3c37-113">根據來源檔案，AVI 媒體來源可能會在其所提供的媒體類型上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="e3c37-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="e3c37-114">AVI 檔案包含檔案中每個資料流程的資料流程標頭。</span><span class="sxs-lookup"><span data-stu-id="e3c37-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="e3c37-115">AVI 媒體來源會將資料流程標頭轉譯為媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e3c37-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="e3c37-116">針對壓縮的影片串流，資料流程標頭包含可識別影片編解碼器的 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="e3c37-116">For compressed video streams, the stream header contains a FOURCC that identifies the video codec.</span></span> <span data-ttu-id="e3c37-117">在大多數情況下，AVI 媒體來源會將此 FOURCC 直接轉換成子類型 GUID，如「 [影片子類型 guid](video-subtype-guids.md)」主題所述。</span><span class="sxs-lookup"><span data-stu-id="e3c37-117">In most cases, the AVI media source converts this FOURCC directly to a subtype GUID, as described in the topic [Video Subtype GUIDs](video-subtype-guids.md).</span></span> <span data-ttu-id="e3c37-118">不過，在某些情況下，它會將原始 FOURCC 對應至另一個相等的 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="e3c37-118">In some cases, however, it maps the original FOURCC to another FOURCC that is equivalent.</span></span> <span data-ttu-id="e3c37-119">如果是的話，媒體來源會使用 MF \_ MT \_ 原始4CC 屬性，將原始 FOURCC 儲存在媒體類型中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e3c37-119">If so, the media source stores the original FOURCC in the media type, using the MF\_MT\_ORIGINAL\_4CC attribute.</span></span>

<span data-ttu-id="e3c37-120">FOURCC 對應會儲存在登錄中的下列機碼底下：</span><span class="sxs-lookup"><span data-stu-id="e3c37-120">The FOURCC mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="e3c37-121">**HKEY \_類別 \_ 根目錄** \\ **MediaFoundation** \\ **MapVideo4cc**</span><span class="sxs-lookup"><span data-stu-id="e3c37-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapVideo4cc**</span></span>

<span data-ttu-id="e3c37-122">每個專案都是 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="e3c37-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="e3c37-123">專案的名稱是 FOURCC 的十六進位標記法，不含 "0x" 前置詞，且字串中第一個字元的第一個字元會出現。</span><span class="sxs-lookup"><span data-stu-id="e3c37-123">The name of the entry is the hexadecimal representation of the FOURCC, without an "0x" prefix, and with the first character appearing first in the string.</span></span> <span data-ttu-id="e3c37-124">例如，FOURCC 碼 ' abcd ' 會顯示為 "61626364"。</span><span class="sxs-lookup"><span data-stu-id="e3c37-124">For example, the FOURCC code 'abcd' would appear as "61626364".</span></span> <span data-ttu-id="e3c37-125">專案的值是對等的 FOURCC 程式碼。</span><span class="sxs-lookup"><span data-stu-id="e3c37-125">The value of the entry is the equivalent FOURCC code.</span></span>

<span data-ttu-id="e3c37-126">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="e3c37-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3c37-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3c37-127">Requirements</span></span>



| <span data-ttu-id="e3c37-128">需求</span><span class="sxs-lookup"><span data-stu-id="e3c37-128">Requirement</span></span> | <span data-ttu-id="e3c37-129">值</span><span class="sxs-lookup"><span data-stu-id="e3c37-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c37-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3c37-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e3c37-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3c37-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e3c37-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3c37-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e3c37-133">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3c37-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e3c37-134">標頭</span><span class="sxs-lookup"><span data-stu-id="e3c37-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3c37-135"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e3c37-135"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3c37-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3c37-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c37-137">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e3c37-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e3c37-138">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="e3c37-138">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




