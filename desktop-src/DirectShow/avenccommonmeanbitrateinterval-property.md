---
description: 指定套用平均位元速率的時間間隔。 這個屬性會與 AVEncCommonMeanBitRate 屬性搭配使用。
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: 'AVEncCommonMeanBitRateInterval 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffee31b0ac54d195051f1cc973d2fdcb058f202
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467892"
---
# <a name="avenccommonmeanbitrateinterval-property"></a><span data-ttu-id="84f6e-104">AVEncCommonMeanBitRateInterval 屬性</span><span class="sxs-lookup"><span data-stu-id="84f6e-104">AVEncCommonMeanBitRateInterval property</span></span>

<span data-ttu-id="84f6e-105">指定套用平均位元速率的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="84f6e-105">Specifies the time interval over which the average bit rate applies.</span></span> <span data-ttu-id="84f6e-106">這個屬性會與 [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) 屬性搭配使用。</span><span class="sxs-lookup"><span data-stu-id="84f6e-106">This property is used in conjunction with the [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property.</span></span>

<span data-ttu-id="84f6e-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="84f6e-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="84f6e-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="84f6e-108">Data type</span></span>

<span data-ttu-id="84f6e-109">**UINT64** (**VT \_ UI8**) </span><span class="sxs-lookup"><span data-stu-id="84f6e-109">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="84f6e-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="84f6e-110">Property GUID</span></span>

<span data-ttu-id="84f6e-111">**CODECAPI \_ AVEncCommonMeanBitRateInterval**</span><span class="sxs-lookup"><span data-stu-id="84f6e-111">**CODECAPI\_AVEncCommonMeanBitRateInterval**</span></span>

## <a name="property-value"></a><span data-ttu-id="84f6e-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="84f6e-112">Property value</span></span>

<span data-ttu-id="84f6e-113">這個屬性具有線性範圍的值。</span><span class="sxs-lookup"><span data-stu-id="84f6e-113">This property has a linear range of values.</span></span> <span data-ttu-id="84f6e-114">若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="84f6e-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="84f6e-115">備註</span><span class="sxs-lookup"><span data-stu-id="84f6e-115">Remarks</span></span>

<span data-ttu-id="84f6e-116">針對兩個傳遞的變數位元速率 (VBR) 編碼方式，值為0表示時間間隔是內容的完整持續時間。</span><span class="sxs-lookup"><span data-stu-id="84f6e-116">For two-pass variable bit rate (VBR) encoding, the value zero indicates that the time interval is the entire duration of the content.</span></span> <span data-ttu-id="84f6e-117">針對單一傳遞的常數速率 (CBR) 編碼方式，值為零表示編碼器選取的間隔 (通常是0.5 秒) 。</span><span class="sxs-lookup"><span data-stu-id="84f6e-117">For single-pass constant bit rate (CBR) encoding, the value zero indicates that the encoder selects the interval (typically 0.5 seconds).</span></span>

## <a name="requirements"></a><span data-ttu-id="84f6e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="84f6e-118">Requirements</span></span>



| <span data-ttu-id="84f6e-119">需求</span><span class="sxs-lookup"><span data-stu-id="84f6e-119">Requirement</span></span> | <span data-ttu-id="84f6e-120">值</span><span class="sxs-lookup"><span data-stu-id="84f6e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84f6e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84f6e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="84f6e-122">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84f6e-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="84f6e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84f6e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="84f6e-124">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84f6e-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="84f6e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="84f6e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="84f6e-126"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="84f6e-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84f6e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84f6e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f6e-128">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="84f6e-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="84f6e-129">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="84f6e-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




