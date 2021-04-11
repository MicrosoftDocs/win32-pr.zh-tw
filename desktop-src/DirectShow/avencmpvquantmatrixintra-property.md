---
description: 指定巨大區塊內部的 luma 量化矩陣。 這個屬性會套用至 MPEG 視頻編碼器。
ms.assetid: 65e6e276-1da7-47ee-b337-0ff64a9c4cff
title: 'AVEncMPVQuantMatrixIntra 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337b570583b77dcc8d0f3f2608beac3b5efb277f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935667"
---
# <a name="avencmpvquantmatrixintra-property"></a><span data-ttu-id="7583f-104">AVEncMPVQuantMatrixIntra 屬性</span><span class="sxs-lookup"><span data-stu-id="7583f-104">AVEncMPVQuantMatrixIntra property</span></span>

<span data-ttu-id="7583f-105">指定巨大區塊內部的 luma 量化矩陣。</span><span class="sxs-lookup"><span data-stu-id="7583f-105">Specifies the luma quantization matrix for intra macroblocks.</span></span> <span data-ttu-id="7583f-106">這個屬性會套用至 MPEG 視頻編碼器。</span><span class="sxs-lookup"><span data-stu-id="7583f-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="7583f-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="7583f-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="7583f-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="7583f-108">Data type</span></span>

<span data-ttu-id="7583f-109">**BSTR** (**VT \_ bstr**) </span><span class="sxs-lookup"><span data-stu-id="7583f-109">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7583f-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="7583f-110">Property GUID</span></span>

<span data-ttu-id="7583f-111">**CODECAPI \_ AVEncMPVQuantMatrixIntra**</span><span class="sxs-lookup"><span data-stu-id="7583f-111">**CODECAPI\_AVEncMPVQuantMatrixIntra**</span></span>

## <a name="property-value"></a><span data-ttu-id="7583f-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="7583f-112">Property value</span></span>

<span data-ttu-id="7583f-113">這個屬性的值是一個字串，其中包含編碼為十六進位值字串的 64 8 位係數 (128 個字元) 。</span><span class="sxs-lookup"><span data-stu-id="7583f-113">The value of this property is a string that contains the 64 8-bit coefficients encoded as a string of hexadecimal values (128 characters).</span></span>

## <a name="requirements"></a><span data-ttu-id="7583f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7583f-114">Requirements</span></span>



| <span data-ttu-id="7583f-115">需求</span><span class="sxs-lookup"><span data-stu-id="7583f-115">Requirement</span></span> | <span data-ttu-id="7583f-116">值</span><span class="sxs-lookup"><span data-stu-id="7583f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7583f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7583f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7583f-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7583f-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7583f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7583f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7583f-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7583f-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7583f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7583f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7583f-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="7583f-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7583f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7583f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7583f-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="7583f-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7583f-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="7583f-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




