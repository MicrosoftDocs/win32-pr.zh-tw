---
description: 指定尖峰位速率（以每秒位數為單位），用於受條件約束的2傳遞變數位速率 (VBR) 播放。
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: 'MFPKEY_RMAX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3568e0a3ee506640200413a5dc222c7cccec2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192227"
---
# <a name="mfpkey_rmax-property"></a><span data-ttu-id="1f73b-103">MFPKEY \_ RMAX 屬性</span><span class="sxs-lookup"><span data-stu-id="1f73b-103">MFPKEY\_RMAX Property</span></span>

<span data-ttu-id="1f73b-104">指定尖峰位速率（以每秒位數為單位），用於受條件約束的2傳遞變數位速率 (VBR) 播放。</span><span class="sxs-lookup"><span data-stu-id="1f73b-104">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) playback.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1f73b-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="1f73b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1f73b-106">g \_ wszWMVCMaxBitrate</span><span class="sxs-lookup"><span data-stu-id="1f73b-106">g\_wszWMVCMaxBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="1f73b-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="1f73b-107">Data Type</span></span>

<span data-ttu-id="1f73b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1f73b-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="1f73b-109">預設值</span><span class="sxs-lookup"><span data-stu-id="1f73b-109">Default Value</span></span>

<span data-ttu-id="1f73b-110">沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="1f73b-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f73b-111">備註</span><span class="sxs-lookup"><span data-stu-id="1f73b-111">Remarks</span></span>

<span data-ttu-id="1f73b-112">此值代表播放的尖峰位元速率。</span><span class="sxs-lookup"><span data-stu-id="1f73b-112">This value represents the peak bit rate for playback.</span></span> <span data-ttu-id="1f73b-113">[MFPKEY \_ BMAX](mfpkey-bmaxproperty.md)的值是用來根據這位速率來描述緩衝區; 實際上，條件約束的 VBR 類似于常數位元速率 (CBR) 使用此值做為位元速率。</span><span class="sxs-lookup"><span data-stu-id="1f73b-113">The value of [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is used to describe the buffer in terms of this bit rate; in effect, constrained VBR is similar to constant bit rate (CBR) using this value as the bit rate.</span></span> <span data-ttu-id="1f73b-114">不過，只要緩衝區增加，就可以用較低的位元速率播放受限的 VBR 資料流程。</span><span class="sxs-lookup"><span data-stu-id="1f73b-114">However, a constrained VBR stream can be played back at a lower bit rate, as long as the buffer is increased.</span></span>

<span data-ttu-id="1f73b-115">您必須設定此值，以進行尖峰限制的雙通路 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="1f73b-115">You must set this value for peak-constrained two-pass VBR encoding.</span></span> <span data-ttu-id="1f73b-116">開始處理範例之後，必須等到您完成串流的編碼之後，才能查詢此值。</span><span class="sxs-lookup"><span data-stu-id="1f73b-116">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="1f73b-117">編碼器會將此值的要求解讀為編碼會話結束的信號;您處理的下一個範例會被視為新會話的開頭。</span><span class="sxs-lookup"><span data-stu-id="1f73b-117">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="1f73b-118">通常，這個值是大於 [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)值的兩到三倍。</span><span class="sxs-lookup"><span data-stu-id="1f73b-118">Typically, this value is two to three times greater than the value of [MFPKEY\_RAVG](mfpkey-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f73b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f73b-119">Requirements</span></span>



| <span data-ttu-id="1f73b-120">需求</span><span class="sxs-lookup"><span data-stu-id="1f73b-120">Requirement</span></span> | <span data-ttu-id="1f73b-121">值</span><span class="sxs-lookup"><span data-stu-id="1f73b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f73b-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f73b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1f73b-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f73b-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1f73b-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f73b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1f73b-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f73b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f73b-126">標頭</span><span class="sxs-lookup"><span data-stu-id="1f73b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f73b-127"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f73b-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f73b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f73b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f73b-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="1f73b-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




