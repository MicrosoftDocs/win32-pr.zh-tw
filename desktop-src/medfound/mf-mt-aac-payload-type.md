---
description: 指定 Advanced Audio 編碼 (AAC) 資料流程的裝載類型。
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: 'MF_MT_AAC_PAYLOAD_TYPE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3edba98bdac54b12fb6e3e44fb67373f7fce6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994166"
---
# <a name="mf_mt_aac_payload_type-attribute"></a><span data-ttu-id="4fb01-103">MF \_ MT \_ AAC \_ 裝載 \_ 類型屬性</span><span class="sxs-lookup"><span data-stu-id="4fb01-103">MF\_MT\_AAC\_PAYLOAD\_TYPE attribute</span></span>

<span data-ttu-id="4fb01-104">指定 Advanced Audio 編碼 (AAC) 資料流程的裝載類型。</span><span class="sxs-lookup"><span data-stu-id="4fb01-104">Specifies the payload type of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="4fb01-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="4fb01-105">Data type</span></span>

<span data-ttu-id="4fb01-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4fb01-106">**UINT32**</span></span>

<span data-ttu-id="4fb01-107">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="4fb01-107">The following values are possible.</span></span>



| <span data-ttu-id="4fb01-108">值</span><span class="sxs-lookup"><span data-stu-id="4fb01-108">Value</span></span>                                                                        | <span data-ttu-id="4fb01-109">意義</span><span class="sxs-lookup"><span data-stu-id="4fb01-109">Meaning</span></span>                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4fb01-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4fb01-110"><dt>0</dt></span></span> </dl> | <span data-ttu-id="4fb01-111">資料流程只包含原始 \_ 資料 \_ 區塊元素。</span><span class="sxs-lookup"><span data-stu-id="4fb01-111">The stream contains raw\_data\_block elements only.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="4fb01-112"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4fb01-112"><dt>1</dt></span></span> </dl> | <span data-ttu-id="4fb01-113">音訊資料傳輸串流 (ADTS) 。</span><span class="sxs-lookup"><span data-stu-id="4fb01-113">Audio Data Transport Stream (ADTS).</span></span> <span data-ttu-id="4fb01-114">資料流程包含 adts \_ 序列（如 mpeg-2 所定義）。</span><span class="sxs-lookup"><span data-stu-id="4fb01-114">The stream contains an adts\_sequence, as defined by MPEG-2.</span></span><br/>                       |
| <dl> <span data-ttu-id="4fb01-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4fb01-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="4fb01-116">音訊資料交換格式 (ADIF) 。</span><span class="sxs-lookup"><span data-stu-id="4fb01-116">Audio Data Interchange Format (ADIF).</span></span> <span data-ttu-id="4fb01-117">資料流程包含 adif \_ 序列（如 mpeg-2 所定義）。</span><span class="sxs-lookup"><span data-stu-id="4fb01-117">The stream contains an adif\_sequence, as defined by MPEG-2.</span></span><br/>                     |
| <dl> <span data-ttu-id="4fb01-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4fb01-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="4fb01-119">此資料流程包含具有同步處理層的 MPEG-2 音訊廣播串流 (LOA) 和多工層 (LATM) 。</span><span class="sxs-lookup"><span data-stu-id="4fb01-119">The stream contains an MPEG-4 audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="4fb01-120">取得/設定</span><span class="sxs-lookup"><span data-stu-id="4fb01-120">Get/set</span></span>

<span data-ttu-id="4fb01-121">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="4fb01-121">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4fb01-122">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="4fb01-122">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4fb01-123">套用至</span><span class="sxs-lookup"><span data-stu-id="4fb01-123">Applies To</span></span>

[<span data-ttu-id="4fb01-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4fb01-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="4fb01-125">備註</span><span class="sxs-lookup"><span data-stu-id="4fb01-125">Remarks</span></span>

<span data-ttu-id="4fb01-126">MF \_ MT \_ AAC \_ 裝載 \_ 類型是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="4fb01-126">MF\_MT\_AAC\_PAYLOAD\_TYPE is optional.</span></span> <span data-ttu-id="4fb01-127">如果未指定此屬性，則會使用預設值0，這會指定資料流程只包含原始 \_ 資料 \_ 區塊元素。</span><span class="sxs-lookup"><span data-stu-id="4fb01-127">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw\_data\_block elements only.</span></span>

<span data-ttu-id="4fb01-128">僅適用于 **MFAudioFormat \_ AAC**。</span><span class="sxs-lookup"><span data-stu-id="4fb01-128">Applies only to **MFAudioFormat\_AAC**.</span></span>

<span data-ttu-id="4fb01-129">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="4fb01-129">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fb01-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fb01-130">Requirements</span></span>



| <span data-ttu-id="4fb01-131">需求</span><span class="sxs-lookup"><span data-stu-id="4fb01-131">Requirement</span></span> | <span data-ttu-id="4fb01-132">值</span><span class="sxs-lookup"><span data-stu-id="4fb01-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb01-133">標頭</span><span class="sxs-lookup"><span data-stu-id="4fb01-133">Header</span></span><br/> | <dl> <span data-ttu-id="4fb01-134"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="4fb01-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fb01-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fb01-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb01-136">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4fb01-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4fb01-137">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="4fb01-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




