---
description: 指定此解碼器的目前輸入格式。
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: 'AVDecCommonInputFormat 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7432d2a48727ec144d4206d4a11bfe65ce2c5d2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467832"
---
# <a name="avdeccommoninputformat-property"></a><span data-ttu-id="07bae-103">AVDecCommonInputFormat 屬性</span><span class="sxs-lookup"><span data-stu-id="07bae-103">AVDecCommonInputFormat property</span></span>

<span data-ttu-id="07bae-104">指定此解碼器的目前輸入格式。</span><span class="sxs-lookup"><span data-stu-id="07bae-104">Specifies the current input format for the decoder.</span></span>

<span data-ttu-id="07bae-105">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="07bae-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="07bae-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="07bae-106">Data type</span></span>

<span data-ttu-id="07bae-107">**BSTR** (**VT \_ bstr**) </span><span class="sxs-lookup"><span data-stu-id="07bae-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="07bae-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="07bae-108">Property GUID</span></span>

<span data-ttu-id="07bae-109">**CODECAPI \_ AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="07bae-109">**CODECAPI\_AVDecCommonInputFormat**</span></span>

## <a name="property-value"></a><span data-ttu-id="07bae-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="07bae-110">Property value</span></span>

<span data-ttu-id="07bae-111">這個屬性的值是 **BSTR** ，其中包含 GUID 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="07bae-111">The value of this property is a **BSTR** that contains the string representation of a GUID.</span></span> <span data-ttu-id="07bae-112">定義了下列 Guid。</span><span class="sxs-lookup"><span data-stu-id="07bae-112">The following GUIDs are defined.</span></span>



| <span data-ttu-id="07bae-113">**GUID**</span><span class="sxs-lookup"><span data-stu-id="07bae-113">**GUID**</span></span>                                            | <span data-ttu-id="07bae-114">Description</span><span class="sxs-lookup"><span data-stu-id="07bae-114">Description</span></span>                                    |
|-----------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="07bae-115">**CODECAPI \_ GUID \_ AVDecAudioInputAAC**</span><span class="sxs-lookup"><span data-stu-id="07bae-115">**CODECAPI\_GUID\_AVDecAudioInputAAC**</span></span>              | <span data-ttu-id="07bae-116">Advanced Audio 編碼 (AAC) </span><span class="sxs-lookup"><span data-stu-id="07bae-116">Advanced Audio Coding (AAC)</span></span>                    |
| <span data-ttu-id="07bae-117">**CODECAPI \_ GUID \_ AVDecAudioInputDolbyDigitalPlus**</span><span class="sxs-lookup"><span data-stu-id="07bae-117">**CODECAPI\_GUID\_AVDecAudioInputDolbyDigitalPlus**</span></span> | <span data-ttu-id="07bae-118">杜比數位加號音訊</span><span class="sxs-lookup"><span data-stu-id="07bae-118">Dolby Digital Plus audio</span></span>                       |
| <span data-ttu-id="07bae-119">**CODECAPI \_ GUID \_ AVDecAudioInputDolby**</span><span class="sxs-lookup"><span data-stu-id="07bae-119">**CODECAPI\_GUID\_AVDecAudioInputDolby**</span></span>            | <span data-ttu-id="07bae-120">杜比音訊</span><span class="sxs-lookup"><span data-stu-id="07bae-120">Dolby audio</span></span>                                    |
| <span data-ttu-id="07bae-121">**CODECAPI \_ GUID \_ AVDecAudioInputDTS**</span><span class="sxs-lookup"><span data-stu-id="07bae-121">**CODECAPI\_GUID\_AVDecAudioInputDTS**</span></span>              | <span data-ttu-id="07bae-122">DTS 音訊</span><span class="sxs-lookup"><span data-stu-id="07bae-122">DTS audio</span></span>                                      |
| <span data-ttu-id="07bae-123">**CODECAPI \_ GUID \_ AVDecAudioInputHEAAC**</span><span class="sxs-lookup"><span data-stu-id="07bae-123">**CODECAPI\_GUID\_AVDecAudioInputHEAAC**</span></span>            | <span data-ttu-id="07bae-124">High-Efficiency (AAC) 的 Advanced 音訊編碼</span><span class="sxs-lookup"><span data-stu-id="07bae-124">High-Efficiency Advanced Audio Coding (HE-AAC)</span></span> |
| <span data-ttu-id="07bae-125">**CODECAPI \_ GUID \_ AVDecAudioInputMPEG**</span><span class="sxs-lookup"><span data-stu-id="07bae-125">**CODECAPI\_GUID\_AVDecAudioInputMPEG**</span></span>             | <span data-ttu-id="07bae-126">MPEG 音訊</span><span class="sxs-lookup"><span data-stu-id="07bae-126">MPEG audio</span></span>                                     |
| <span data-ttu-id="07bae-127">**CODECAPI \_ GUID \_ AVDecAudioInputPCM**</span><span class="sxs-lookup"><span data-stu-id="07bae-127">**CODECAPI\_GUID\_AVDecAudioInputPCM**</span></span>              | <span data-ttu-id="07bae-128">PCM 音訊</span><span class="sxs-lookup"><span data-stu-id="07bae-128">PCM audio</span></span>                                      |
| <span data-ttu-id="07bae-129">**CODECAPI \_ GUID \_ AVDecAudioInputWMA**</span><span class="sxs-lookup"><span data-stu-id="07bae-129">**CODECAPI\_GUID\_AVDecAudioInputWMA**</span></span>              | <span data-ttu-id="07bae-130">Windows Media 音訊</span><span class="sxs-lookup"><span data-stu-id="07bae-130">Windows Media Audio</span></span>                            |
| <span data-ttu-id="07bae-131">**CODECAPI \_ GUID \_ AVDecAudioInputWMAPro**</span><span class="sxs-lookup"><span data-stu-id="07bae-131">**CODECAPI\_GUID\_AVDecAudioInputWMAPro**</span></span>           | <span data-ttu-id="07bae-132">Windows Media 音訊 9 Professional (WMA Pro) </span><span class="sxs-lookup"><span data-stu-id="07bae-132">Windows Media Audio 9 Professional (WMA Pro)</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="07bae-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="07bae-133">Requirements</span></span>



| <span data-ttu-id="07bae-134">需求</span><span class="sxs-lookup"><span data-stu-id="07bae-134">Requirement</span></span> | <span data-ttu-id="07bae-135">值</span><span class="sxs-lookup"><span data-stu-id="07bae-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07bae-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07bae-136">Minimum supported client</span></span><br/> | <span data-ttu-id="07bae-137">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07bae-137">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="07bae-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07bae-138">Minimum supported server</span></span><br/> | <span data-ttu-id="07bae-139">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07bae-139">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="07bae-140">標頭</span><span class="sxs-lookup"><span data-stu-id="07bae-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="07bae-141"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="07bae-141"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07bae-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07bae-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07bae-143">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="07bae-143">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="07bae-144">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="07bae-144">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




