---
description: 為編碼的影片指定中繼框架高度。
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: 'MFPKEY_FORCEFRAMEHEIGHT 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e4662ce56ea4c20d44abdd05641219bc6b94ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192259"
---
# <a name="mfpkey_forceframeheight-property"></a><span data-ttu-id="73129-103">MFPKEY \_ FORCEFRAMEHEIGHT 屬性</span><span class="sxs-lookup"><span data-stu-id="73129-103">MFPKEY\_FORCEFRAMEHEIGHT Property</span></span>

<span data-ttu-id="73129-104">為編碼的影片指定中繼框架高度。</span><span class="sxs-lookup"><span data-stu-id="73129-104">Specifies an intermediate frame height for encoded video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="73129-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="73129-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="73129-106">g \_ wszWMVCForceFrameHeight</span><span class="sxs-lookup"><span data-stu-id="73129-106">g\_wszWMVCForceFrameHeight</span></span>

## <a name="data-type"></a><span data-ttu-id="73129-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="73129-107">Data Type</span></span>

<span data-ttu-id="73129-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="73129-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="73129-109">備註</span><span class="sxs-lookup"><span data-stu-id="73129-109">Remarks</span></span>

<span data-ttu-id="73129-110">您可以設定此值和 [MFPKEY \_ FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) 屬性，以強制編碼器以小於輸入或輸出框架大小的框架大小來編碼影片串流。</span><span class="sxs-lookup"><span data-stu-id="73129-110">You can set this value and the [MFPKEY\_FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) property to force the encoder to encode the video stream with a frame size that is smaller than the input or output frame sizes.</span></span> <span data-ttu-id="73129-111">解碼時，影片將會調整大小為其原始輸入解析度。</span><span class="sxs-lookup"><span data-stu-id="73129-111">When decoded, the video will be resized to its original input resolution.</span></span>

<span data-ttu-id="73129-112">任一軸的有效框架維度都是2到8192圖元。</span><span class="sxs-lookup"><span data-stu-id="73129-112">Valid frame dimensions on either axis are 2 to 8192 pixels.</span></span> <span data-ttu-id="73129-113">框架維度必須可以整除2。</span><span class="sxs-lookup"><span data-stu-id="73129-113">Frame dimensions must be divisible by 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="73129-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="73129-114">Requirements</span></span>



| <span data-ttu-id="73129-115">需求</span><span class="sxs-lookup"><span data-stu-id="73129-115">Requirement</span></span> | <span data-ttu-id="73129-116">值</span><span class="sxs-lookup"><span data-stu-id="73129-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73129-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73129-117">Minimum supported client</span></span><br/> | <span data-ttu-id="73129-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73129-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="73129-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73129-119">Minimum supported server</span></span><br/> | <span data-ttu-id="73129-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73129-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73129-121">標頭</span><span class="sxs-lookup"><span data-stu-id="73129-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="73129-122"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="73129-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73129-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73129-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73129-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="73129-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




