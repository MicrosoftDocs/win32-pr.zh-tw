---
description: 停用視頻處理器 MFT 中的畫面播放速率轉換。
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: 'MF_XVP_DISABLE_FRC 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1922705514c51308138f9f301a3681e598ca6278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943638"
---
# <a name="mf_xvp_disable_frc-attribute"></a><span data-ttu-id="0a654-103">MF \_ XVP \_ 停用 \_ FRC 屬性</span><span class="sxs-lookup"><span data-stu-id="0a654-103">MF\_XVP\_DISABLE\_FRC attribute</span></span>

<span data-ttu-id="0a654-104">停用 [**視頻處理器 MFT**](video-processor-mft.md)中的畫面播放速率轉換。</span><span class="sxs-lookup"><span data-stu-id="0a654-104">Disables frame-rate conversion in the [**Video Processor MFT**](video-processor-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="0a654-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="0a654-105">Data type</span></span>

<span data-ttu-id="0a654-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="0a654-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0a654-107">備註</span><span class="sxs-lookup"><span data-stu-id="0a654-107">Remarks</span></span>

<span data-ttu-id="0a654-108">如果此屬性為 **TRUE**，則視頻處理器不會執行畫面播放速率轉換。</span><span class="sxs-lookup"><span data-stu-id="0a654-108">If this attribute is **TRUE**, the video processor will not perform frame-rate conversion.</span></span> <span data-ttu-id="0a654-109">根據預設，視頻處理器會將畫面播放速率轉換成符合輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0a654-109">By default, the video processor will convert the frame rate to match the output media type.</span></span>

<span data-ttu-id="0a654-110">若要設定此屬性：</span><span class="sxs-lookup"><span data-stu-id="0a654-110">To set this attribute:</span></span>

1.  <span data-ttu-id="0a654-111">在視頻處理器上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 。</span><span class="sxs-lookup"><span data-stu-id="0a654-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="0a654-112">呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="0a654-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="0a654-113">開始串流之前，請設定屬性。</span><span class="sxs-lookup"><span data-stu-id="0a654-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a654-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a654-114">Requirements</span></span>



| <span data-ttu-id="0a654-115">需求</span><span class="sxs-lookup"><span data-stu-id="0a654-115">Requirement</span></span> | <span data-ttu-id="0a654-116">值</span><span class="sxs-lookup"><span data-stu-id="0a654-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a654-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a654-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0a654-118">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a654-118">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0a654-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a654-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0a654-120">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a654-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0a654-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0a654-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a654-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a654-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a654-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a654-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a654-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="0a654-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




