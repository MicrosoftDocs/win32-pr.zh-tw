---
description: 指定平均編碼的位元速率（以位/秒為單位）。 這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。
ms.assetid: 8519685a-4f5b-44af-ad46-09eba7a198c6
title: 'AVEncCommonMeanBitRate 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4eaec7fc6578e6e69a45616ee6de059bb7a378b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510279"
---
# <a name="avenccommonmeanbitrate-property"></a><span data-ttu-id="f5b08-104">AVEncCommonMeanBitRate 屬性</span><span class="sxs-lookup"><span data-stu-id="f5b08-104">AVEncCommonMeanBitRate property</span></span>

<span data-ttu-id="f5b08-105">指定平均編碼的位元速率（以位/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f5b08-105">Specifies the average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="f5b08-106">這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。</span><span class="sxs-lookup"><span data-stu-id="f5b08-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="f5b08-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f5b08-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="f5b08-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="f5b08-108">Data type</span></span>

<span data-ttu-id="f5b08-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="f5b08-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f5b08-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="f5b08-110">Property GUID</span></span>

<span data-ttu-id="f5b08-111">**CODECAPI \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="f5b08-111">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="f5b08-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="f5b08-112">Property value</span></span>

<span data-ttu-id="f5b08-113">編碼器可以將此屬性實作為列舉集或線性範圍。</span><span class="sxs-lookup"><span data-stu-id="f5b08-113">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5b08-114">備註</span><span class="sxs-lookup"><span data-stu-id="f5b08-114">Remarks</span></span>

<span data-ttu-id="f5b08-115">這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)一起使用。</span><span class="sxs-lookup"><span data-stu-id="f5b08-115">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5b08-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5b08-116">Requirements</span></span>



| <span data-ttu-id="f5b08-117">需求</span><span class="sxs-lookup"><span data-stu-id="f5b08-117">Requirement</span></span> | <span data-ttu-id="f5b08-118">值</span><span class="sxs-lookup"><span data-stu-id="f5b08-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b08-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5b08-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b08-120">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5b08-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f5b08-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5b08-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b08-122">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5b08-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f5b08-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f5b08-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5b08-124"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f5b08-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5b08-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5b08-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b08-126">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="f5b08-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="f5b08-127">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="f5b08-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

