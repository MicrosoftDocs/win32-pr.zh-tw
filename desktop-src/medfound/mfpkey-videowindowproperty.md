---
description: 指定可符合模型緩衝區的內容數量（以毫秒為單位）。
ms.assetid: da959bef-1e87-4638-9a77-4135c31a3d27
title: 'MFPKEY_VIDEOWINDOW 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33d10b3a589ef3bcfc945b2c3404c7b02cb7121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512637"
---
# <a name="mfpkey_videowindow-property"></a><span data-ttu-id="fc685-103">MFPKEY \_ VIDEOWINDOW 屬性</span><span class="sxs-lookup"><span data-stu-id="fc685-103">MFPKEY\_VIDEOWINDOW Property</span></span>

<span data-ttu-id="fc685-104">指定可符合模型緩衝區的內容數量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="fc685-104">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="fc685-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="fc685-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="fc685-106">g \_ wszWMVCVideoWIndow</span><span class="sxs-lookup"><span data-stu-id="fc685-106">g\_wszWMVCVideoWIndow</span></span>

## <a name="data-type"></a><span data-ttu-id="fc685-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="fc685-107">Data Type</span></span>

<span data-ttu-id="fc685-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="fc685-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="fc685-109">預設值</span><span class="sxs-lookup"><span data-stu-id="fc685-109">Default Value</span></span>

<span data-ttu-id="fc685-110">3000</span><span class="sxs-lookup"><span data-stu-id="fc685-110">3000</span></span>

## <a name="remarks"></a><span data-ttu-id="fc685-111">備註</span><span class="sxs-lookup"><span data-stu-id="fc685-111">Remarks</span></span>

<span data-ttu-id="fc685-112">緩衝區視窗是編解碼器速率控制項中所使用的其中一個「有漏洞 bucket」模型參數。</span><span class="sxs-lookup"><span data-stu-id="fc685-112">The buffer window is one of the "leaky bucket" model parameters used in the codec rate control.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc685-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc685-113">Requirements</span></span>



| <span data-ttu-id="fc685-114">需求</span><span class="sxs-lookup"><span data-stu-id="fc685-114">Requirement</span></span> | <span data-ttu-id="fc685-115">值</span><span class="sxs-lookup"><span data-stu-id="fc685-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc685-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc685-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fc685-117">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc685-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fc685-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc685-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fc685-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc685-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fc685-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fc685-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc685-121"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fc685-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc685-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc685-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc685-123">設定影片編碼</span><span class="sxs-lookup"><span data-stu-id="fc685-123">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="fc685-124">有漏洞 Bucket 緩衝區模型</span><span class="sxs-lookup"><span data-stu-id="fc685-124">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="fc685-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="fc685-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




