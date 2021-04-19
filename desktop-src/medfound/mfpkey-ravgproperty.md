---
description: 指定平均位元速率（以每秒位數為單位），用於2次傳遞、變數位速率 (VBR) 編碼。
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: 'MFPKEY_RAVG 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad15d2445dc2acea1e91f4d01fad6e7bd83edb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971741"
---
# <a name="mfpkey_ravg-property"></a><span data-ttu-id="203e7-103">MFPKEY \_ RAVG 屬性</span><span class="sxs-lookup"><span data-stu-id="203e7-103">MFPKEY\_RAVG Property</span></span>

<span data-ttu-id="203e7-104">指定平均位元速率（以每秒位數為單位），用於2次傳遞、變數位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="203e7-104">Specifies the average bit rate, in bits per second, used for 2-pass, variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="203e7-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="203e7-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="203e7-106">g \_ wszWMVCAvgBitrate</span><span class="sxs-lookup"><span data-stu-id="203e7-106">g\_wszWMVCAvgBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="203e7-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="203e7-107">Data Type</span></span>

<span data-ttu-id="203e7-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="203e7-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="203e7-109">備註</span><span class="sxs-lookup"><span data-stu-id="203e7-109">Remarks</span></span>

<span data-ttu-id="203e7-110">在受限制和不受限制的 VBR 中，此值是橫跨內容持續時間的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="203e7-110">In both constrained and unconstrained VBR, this value is the average bit rate across the duration of the content.</span></span>

<span data-ttu-id="203e7-111">您必須為兩個雙通路的 VBR 編碼模式設定這個值。</span><span class="sxs-lookup"><span data-stu-id="203e7-111">You must set this value for both modes of two-pass VBR encoding.</span></span> <span data-ttu-id="203e7-112">開始處理範例之後，必須等到您完成串流的編碼之後，才能查詢此值。</span><span class="sxs-lookup"><span data-stu-id="203e7-112">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="203e7-113">編碼器會將此值的要求解讀為編碼會話結束的信號;您處理的下一個範例會被視為新會話的開頭。</span><span class="sxs-lookup"><span data-stu-id="203e7-113">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="203e7-114">您也可以在1遍的 VBR 編碼會話結束時讀取這個屬性。</span><span class="sxs-lookup"><span data-stu-id="203e7-114">This property can also be read at the end of a 1-pass VBR encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="203e7-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="203e7-115">Requirements</span></span>



| <span data-ttu-id="203e7-116">需求</span><span class="sxs-lookup"><span data-stu-id="203e7-116">Requirement</span></span> | <span data-ttu-id="203e7-117">值</span><span class="sxs-lookup"><span data-stu-id="203e7-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="203e7-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="203e7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="203e7-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="203e7-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="203e7-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="203e7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="203e7-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="203e7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="203e7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="203e7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="203e7-123"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="203e7-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="203e7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="203e7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="203e7-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="203e7-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




