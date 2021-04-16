---
description: 指定編碼影片的中繼框架寬度。
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: 'MFPKEY_FORCEFRAMEWIDTH 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea4c8c7ac025de1c089c592a591136df966797d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513108"
---
# <a name="mfpkey_forceframewidth-property"></a><span data-ttu-id="815c9-103">MFPKEY \_ FORCEFRAMEWIDTH 屬性</span><span class="sxs-lookup"><span data-stu-id="815c9-103">MFPKEY\_FORCEFRAMEWIDTH Property</span></span>

<span data-ttu-id="815c9-104">指定編碼影片的中繼框架寬度。</span><span class="sxs-lookup"><span data-stu-id="815c9-104">Specifies an intermediate frame width for encoded video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="815c9-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="815c9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="815c9-106">g \_ wszWMVCForceFrameWidth</span><span class="sxs-lookup"><span data-stu-id="815c9-106">g\_wszWMVCForceFrameWidth</span></span>

## <a name="data-type"></a><span data-ttu-id="815c9-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="815c9-107">Data Type</span></span>

<span data-ttu-id="815c9-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="815c9-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="815c9-109">備註</span><span class="sxs-lookup"><span data-stu-id="815c9-109">Remarks</span></span>

<span data-ttu-id="815c9-110">您可以設定此值和 [MFPKEY \_ FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md) 屬性，以強制編碼器以小於輸入或輸出框架大小的框架大小來編碼影片串流。</span><span class="sxs-lookup"><span data-stu-id="815c9-110">You can set this value and the [MFPKEY\_FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md) property to force the encoder to encode the video stream with a frame size that is smaller than the input or output frame sizes.</span></span> <span data-ttu-id="815c9-111">解碼時，影片將會調整大小為其原始輸入解析度。</span><span class="sxs-lookup"><span data-stu-id="815c9-111">When decoded, the video will be resized to its original input resolution.</span></span>

<span data-ttu-id="815c9-112">任一軸的有效框架維度都是2到8192圖元。</span><span class="sxs-lookup"><span data-stu-id="815c9-112">Valid frame dimensions on either axis are 2 to 8192 pixels.</span></span> <span data-ttu-id="815c9-113">框架維度必須可以整除2。</span><span class="sxs-lookup"><span data-stu-id="815c9-113">Frame dimensions must be divisible by 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="815c9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="815c9-114">Requirements</span></span>



| <span data-ttu-id="815c9-115">需求</span><span class="sxs-lookup"><span data-stu-id="815c9-115">Requirement</span></span> | <span data-ttu-id="815c9-116">值</span><span class="sxs-lookup"><span data-stu-id="815c9-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="815c9-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="815c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="815c9-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="815c9-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="815c9-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="815c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="815c9-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="815c9-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="815c9-121">標頭</span><span class="sxs-lookup"><span data-stu-id="815c9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="815c9-122"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="815c9-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="815c9-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="815c9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="815c9-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="815c9-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




