---
description: 以毫秒為單位，以毫秒為單位，指定受限制的變數位速率 (VBR) 資料流程的尖峰位元速率 (由 MFPKEY \_ RMAX) 指定。
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: 'MFPKEY_BMAX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaca172e97c27e6e8d97902fbe3c969efc933eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985367"
---
# <a name="mfpkey_bmax-property"></a><span data-ttu-id="9ba3b-103">MFPKEY \_ BMAX 屬性</span><span class="sxs-lookup"><span data-stu-id="9ba3b-103">MFPKEY\_BMAX Property</span></span>

<span data-ttu-id="9ba3b-104">以毫秒為單位，以毫秒為單位，指定受限制的變數位速率 (VBR) 資料流程的尖峰位元速率 (由 [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)) 指定。</span><span class="sxs-lookup"><span data-stu-id="9ba3b-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by [MFPKEY\_RMAX](mfpkey-rmaxproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9ba3b-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="9ba3b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9ba3b-106">g \_ wszWMVCBMax</span><span class="sxs-lookup"><span data-stu-id="9ba3b-106">g\_wszWMVCBMax</span></span>

## <a name="data-type"></a><span data-ttu-id="9ba3b-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="9ba3b-107">Data Type</span></span>

<span data-ttu-id="9ba3b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9ba3b-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="9ba3b-109">預設值</span><span class="sxs-lookup"><span data-stu-id="9ba3b-109">Default Value</span></span>

<span data-ttu-id="9ba3b-110">沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="9ba3b-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ba3b-111">備註</span><span class="sxs-lookup"><span data-stu-id="9ba3b-111">Remarks</span></span>

<span data-ttu-id="9ba3b-112">您必須為尖峰限制的 VBR 編碼設定此值。</span><span class="sxs-lookup"><span data-stu-id="9ba3b-112">You must set this value for peak-constrained VBR encoding.</span></span> <span data-ttu-id="9ba3b-113">開始處理範例之後，必須等到您完成串流的編碼之後，才能查詢此值。</span><span class="sxs-lookup"><span data-stu-id="9ba3b-113">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="9ba3b-114">編解碼器會將此值的要求視為編碼會話的信號來解讀;您處理的下一個範例會被視為新會話的開頭。</span><span class="sxs-lookup"><span data-stu-id="9ba3b-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba3b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ba3b-115">Requirements</span></span>



| <span data-ttu-id="9ba3b-116">需求</span><span class="sxs-lookup"><span data-stu-id="9ba3b-116">Requirement</span></span> | <span data-ttu-id="9ba3b-117">值</span><span class="sxs-lookup"><span data-stu-id="9ba3b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba3b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ba3b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba3b-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ba3b-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9ba3b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ba3b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba3b-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ba3b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ba3b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9ba3b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ba3b-123"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9ba3b-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ba3b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ba3b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba3b-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="9ba3b-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




