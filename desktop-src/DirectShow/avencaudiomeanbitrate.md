---
description: 指定編碼音訊串流的平均位元速率，以每秒位數為單位。 這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。
ms.assetid: 9513ad64-2de9-497d-86ce-46cfdf87e0f8
title: 'AVEncAudioMeanBitRate 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e311686e6113003593c8a6dbe02a9fca1f30b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025776"
---
# <a name="avencaudiomeanbitrate-property"></a><span data-ttu-id="a3e82-104">AVEncAudioMeanBitRate 屬性</span><span class="sxs-lookup"><span data-stu-id="a3e82-104">AVEncAudioMeanBitRate property</span></span>

<span data-ttu-id="a3e82-105">指定編碼音訊串流的平均位元速率，以每秒位數為單位。</span><span class="sxs-lookup"><span data-stu-id="a3e82-105">Specifies the average bit rate of the encoded audio stream, in bits per second.</span></span> <span data-ttu-id="a3e82-106">這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。</span><span class="sxs-lookup"><span data-stu-id="a3e82-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="a3e82-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="a3e82-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a3e82-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="a3e82-108">Data type</span></span>

<span data-ttu-id="a3e82-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="a3e82-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a3e82-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="a3e82-110">Property GUID</span></span>

<span data-ttu-id="a3e82-111">**CODECAPI \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="a3e82-111">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="a3e82-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="a3e82-112">Property value</span></span>

<span data-ttu-id="a3e82-113">編碼器可以將此屬性實作為列舉集或線性範圍。</span><span class="sxs-lookup"><span data-stu-id="a3e82-113">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e82-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3e82-114">Requirements</span></span>



| <span data-ttu-id="a3e82-115">需求</span><span class="sxs-lookup"><span data-stu-id="a3e82-115">Requirement</span></span> | <span data-ttu-id="a3e82-116">值</span><span class="sxs-lookup"><span data-stu-id="a3e82-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e82-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3e82-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e82-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3e82-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a3e82-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3e82-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e82-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3e82-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a3e82-121">標頭</span><span class="sxs-lookup"><span data-stu-id="a3e82-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3e82-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a3e82-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3e82-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3e82-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e82-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="a3e82-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a3e82-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="a3e82-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




