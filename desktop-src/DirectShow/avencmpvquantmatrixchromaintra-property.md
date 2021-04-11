---
description: 指定巨大區塊內的色度量化矩陣。 這個屬性會套用至 MPEG 視頻編碼器。
ms.assetid: 9da6130f-c064-4b6b-b0ab-ba99118fd249
title: 'AVEncMPVQuantMatrixChromaIntra 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7253a3064acbff74ce22134a40a52d87c78113a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108625"
---
# <a name="avencmpvquantmatrixchromaintra-property"></a><span data-ttu-id="d5b90-104">AVEncMPVQuantMatrixChromaIntra 屬性</span><span class="sxs-lookup"><span data-stu-id="d5b90-104">AVEncMPVQuantMatrixChromaIntra property</span></span>

<span data-ttu-id="d5b90-105">指定巨大區塊內的色度量化矩陣。</span><span class="sxs-lookup"><span data-stu-id="d5b90-105">Specifies the chroma quantization matrix for intra macroblocks.</span></span> <span data-ttu-id="d5b90-106">這個屬性會套用至 MPEG 視頻編碼器。</span><span class="sxs-lookup"><span data-stu-id="d5b90-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="d5b90-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d5b90-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d5b90-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="d5b90-108">Data type</span></span>

<span data-ttu-id="d5b90-109">**BSTR** (**VT \_ bstr**) </span><span class="sxs-lookup"><span data-stu-id="d5b90-109">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d5b90-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="d5b90-110">Property GUID</span></span>

<span data-ttu-id="d5b90-111">**CODECAPI \_ AVEncMPVQuantMatrixChromaIntra**</span><span class="sxs-lookup"><span data-stu-id="d5b90-111">**CODECAPI\_AVEncMPVQuantMatrixChromaIntra**</span></span>

## <a name="property-value"></a><span data-ttu-id="d5b90-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="d5b90-112">Property value</span></span>

<span data-ttu-id="d5b90-113">這個屬性的值是一個字串，其中包含編碼為十六進位值字串的 64 8 位係數 (128 個字元) 。</span><span class="sxs-lookup"><span data-stu-id="d5b90-113">The value of this property is a string that contains the 64 8-bit coefficients encoded as a string of hexadecimal values (128 characters).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5b90-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5b90-114">Requirements</span></span>



| <span data-ttu-id="d5b90-115">需求</span><span class="sxs-lookup"><span data-stu-id="d5b90-115">Requirement</span></span> | <span data-ttu-id="d5b90-116">值</span><span class="sxs-lookup"><span data-stu-id="d5b90-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b90-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5b90-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d5b90-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5b90-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d5b90-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5b90-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d5b90-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5b90-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d5b90-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d5b90-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5b90-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5b90-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5b90-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5b90-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5b90-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="d5b90-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d5b90-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="d5b90-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




