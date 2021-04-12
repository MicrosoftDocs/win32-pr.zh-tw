---
description: 傳回編碼音訊的每秒平均位數。
ms.assetid: c90c9247-825f-4602-bb16-809969703a98
title: 'AVEncStatAudioAverageBPS 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76bcf1ca7b3ee74ae406ebd71f85988a4d13313
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025772"
---
# <a name="avencstataudioaveragebps-property"></a><span data-ttu-id="52b85-103">AVEncStatAudioAverageBPS 屬性</span><span class="sxs-lookup"><span data-stu-id="52b85-103">AVEncStatAudioAverageBPS property</span></span>

<span data-ttu-id="52b85-104">傳回編碼音訊的每秒平均位數。</span><span class="sxs-lookup"><span data-stu-id="52b85-104">Returns the average bits per second of the encoded audio.</span></span>

<span data-ttu-id="52b85-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="52b85-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="52b85-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="52b85-106">Data type</span></span>

<span data-ttu-id="52b85-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="52b85-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="52b85-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="52b85-108">Property GUID</span></span>

<span data-ttu-id="52b85-109">**CODECAPI \_ AVEncStatAudioAverageBPS**</span><span class="sxs-lookup"><span data-stu-id="52b85-109">**CODECAPI\_AVEncStatAudioAverageBPS**</span></span>

## <a name="remarks"></a><span data-ttu-id="52b85-110">備註</span><span class="sxs-lookup"><span data-stu-id="52b85-110">Remarks</span></span>

<span data-ttu-id="52b85-111">編碼完成之後，就可以使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="52b85-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="52b85-112">這個屬性只適用于以品質為基礎的變數位元速率 (VBR) 編碼</span><span class="sxs-lookup"><span data-stu-id="52b85-112">This property applies only to quality-based variable bit rate (VBR) encoding</span></span>

## <a name="requirements"></a><span data-ttu-id="52b85-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="52b85-113">Requirements</span></span>



| <span data-ttu-id="52b85-114">需求</span><span class="sxs-lookup"><span data-stu-id="52b85-114">Requirement</span></span> | <span data-ttu-id="52b85-115">值</span><span class="sxs-lookup"><span data-stu-id="52b85-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52b85-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52b85-116">Minimum supported client</span></span><br/> | <span data-ttu-id="52b85-117">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52b85-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="52b85-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52b85-118">Minimum supported server</span></span><br/> | <span data-ttu-id="52b85-119">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52b85-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="52b85-120">標頭</span><span class="sxs-lookup"><span data-stu-id="52b85-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="52b85-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="52b85-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52b85-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52b85-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52b85-123">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="52b85-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="52b85-124">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="52b85-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




