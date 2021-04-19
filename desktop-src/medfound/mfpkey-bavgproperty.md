---
description: 以毫秒為單位，以毫秒為單位，指定受限制的變數位速率 (VBR) 資料流程的平均位元速率 (由 MFPKEY \_ RAVG) 指定。
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: 'MFPKEY_BAVG 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983606"
---
# <a name="mfpkey_bavg-property"></a><span data-ttu-id="235a4-103">MFPKEY \_ BAVG 屬性</span><span class="sxs-lookup"><span data-stu-id="235a4-103">MFPKEY\_BAVG Property</span></span>

<span data-ttu-id="235a4-104">以毫秒為單位，以毫秒為單位，指定受限制的變數位速率 (VBR) 資料流程的平均位元速率 (由 [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)) 指定。</span><span class="sxs-lookup"><span data-stu-id="235a4-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by [MFPKEY\_RAVG](mfpkey-ravgproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="235a4-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="235a4-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="235a4-106">g \_ wszWMVCBAvg</span><span class="sxs-lookup"><span data-stu-id="235a4-106">g\_wszWMVCBAvg</span></span>

## <a name="data-type"></a><span data-ttu-id="235a4-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="235a4-107">Data Type</span></span>

<span data-ttu-id="235a4-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="235a4-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="235a4-109">預設值</span><span class="sxs-lookup"><span data-stu-id="235a4-109">Default Value</span></span>

<span data-ttu-id="235a4-110">沒有預設值，但編解碼器會根據其他受限制的 VBR 設定來計算適當的值。</span><span class="sxs-lookup"><span data-stu-id="235a4-110">No default value, but the codec will compute an appropriate value based on the other constrained VBR settings.</span></span>

## <a name="remarks"></a><span data-ttu-id="235a4-111">備註</span><span class="sxs-lookup"><span data-stu-id="235a4-111">Remarks</span></span>

<span data-ttu-id="235a4-112">此值是由編解碼器在最終編碼傳遞之後計算。</span><span class="sxs-lookup"><span data-stu-id="235a4-112">This value is computed by the codec after the final encoding pass.</span></span> <span data-ttu-id="235a4-113">在編碼完成之前，您不應該查詢此值。</span><span class="sxs-lookup"><span data-stu-id="235a4-113">You should not query for this value until after encoding is complete.</span></span> <span data-ttu-id="235a4-114">編解碼器會將此值的要求視為編碼會話的信號來解讀;您處理的下一個範例會被視為新會話的開頭。</span><span class="sxs-lookup"><span data-stu-id="235a4-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="235a4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="235a4-115">Requirements</span></span>



| <span data-ttu-id="235a4-116">需求</span><span class="sxs-lookup"><span data-stu-id="235a4-116">Requirement</span></span> | <span data-ttu-id="235a4-117">值</span><span class="sxs-lookup"><span data-stu-id="235a4-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="235a4-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="235a4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="235a4-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="235a4-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="235a4-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="235a4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="235a4-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="235a4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="235a4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="235a4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="235a4-123"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="235a4-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="235a4-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="235a4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="235a4-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="235a4-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




