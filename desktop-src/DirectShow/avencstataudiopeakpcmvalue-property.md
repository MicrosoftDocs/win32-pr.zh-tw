---
description: 傳回音頻內容中出現的最高音量層級。
ms.assetid: 1d9a6a22-bb82-45e1-80d2-88627c90340c
title: 'AVEncStatAudioPeakPCMValue 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d75444631a63c946d4020fe91cdd3a980fc393
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108988"
---
# <a name="avencstataudiopeakpcmvalue-property"></a><span data-ttu-id="2bf73-103">AVEncStatAudioPeakPCMValue 屬性</span><span class="sxs-lookup"><span data-stu-id="2bf73-103">AVEncStatAudioPeakPCMValue property</span></span>

<span data-ttu-id="2bf73-104">傳回音頻內容中出現的最高音量層級。</span><span class="sxs-lookup"><span data-stu-id="2bf73-104">Returns the highest volume level that was present in the audio content.</span></span>

<span data-ttu-id="2bf73-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2bf73-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="2bf73-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="2bf73-106">Data type</span></span>

<span data-ttu-id="2bf73-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="2bf73-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2bf73-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="2bf73-108">Property GUID</span></span>

<span data-ttu-id="2bf73-109">**CODECAPI \_ AVEncStatAudioPeakPCMValue**</span><span class="sxs-lookup"><span data-stu-id="2bf73-109">**CODECAPI\_AVEncStatAudioPeakPCMValue**</span></span>

## <a name="remarks"></a><span data-ttu-id="2bf73-110">備註</span><span class="sxs-lookup"><span data-stu-id="2bf73-110">Remarks</span></span>

<span data-ttu-id="2bf73-111">編碼完成之後，就可以使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2bf73-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="2bf73-112">這個屬性只適用于以品質為基礎的變數位元速率 (VBR) 編碼</span><span class="sxs-lookup"><span data-stu-id="2bf73-112">This property applies only to quality-based variable bit rate (VBR) encoding</span></span>

## <a name="requirements"></a><span data-ttu-id="2bf73-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bf73-113">Requirements</span></span>



| <span data-ttu-id="2bf73-114">需求</span><span class="sxs-lookup"><span data-stu-id="2bf73-114">Requirement</span></span> | <span data-ttu-id="2bf73-115">值</span><span class="sxs-lookup"><span data-stu-id="2bf73-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bf73-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2bf73-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2bf73-117">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bf73-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2bf73-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2bf73-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2bf73-119">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bf73-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2bf73-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2bf73-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bf73-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2bf73-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bf73-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bf73-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bf73-123">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="2bf73-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2bf73-124">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="2bf73-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




