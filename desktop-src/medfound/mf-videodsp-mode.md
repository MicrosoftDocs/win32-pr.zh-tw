---
description: 設定影片防震 MFT 的處理模式。
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: 'MF_VIDEODSP_MODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114012"
---
# <a name="mf_videodsp_mode-attribute"></a><span data-ttu-id="48dfa-103">MF \_ VIDEODSP \_ 模式屬性</span><span class="sxs-lookup"><span data-stu-id="48dfa-103">MF\_VIDEODSP\_MODE attribute</span></span>

<span data-ttu-id="48dfa-104">設定 [**影片防震 MFT**](video-stabilization-mft.md)的處理模式。</span><span class="sxs-lookup"><span data-stu-id="48dfa-104">Sets the processing mode of the [**Video Stabilization MFT**](video-stabilization-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="48dfa-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="48dfa-105">Data type</span></span>

<span data-ttu-id="48dfa-106">**MFVideoDSPMode** 儲存為 **UIINT32**</span><span class="sxs-lookup"><span data-stu-id="48dfa-106">**MFVideoDSPMode** stored as **UIINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="48dfa-107">備註</span><span class="sxs-lookup"><span data-stu-id="48dfa-107">Remarks</span></span>

<span data-ttu-id="48dfa-108">這個屬性的值是 [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) 列舉值。</span><span class="sxs-lookup"><span data-stu-id="48dfa-108">The value of this attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="48dfa-109">這個屬性可用來啟用或停用影像穩定，並且可以針對每個輸出範例進行更新。</span><span class="sxs-lookup"><span data-stu-id="48dfa-109">This attribute can be used to enable or disable the image stabilization, and can be updated for each output sample.</span></span>

<span data-ttu-id="48dfa-110">若要設定此屬性：</span><span class="sxs-lookup"><span data-stu-id="48dfa-110">To set this attribute:</span></span>

1.  <span data-ttu-id="48dfa-111">在影片穩定的 MFT 上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) ，以取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="48dfa-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video stabilization MFT to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="48dfa-112">呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) 來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="48dfa-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="48dfa-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="48dfa-113">Requirements</span></span>



| <span data-ttu-id="48dfa-114">需求</span><span class="sxs-lookup"><span data-stu-id="48dfa-114">Requirement</span></span> | <span data-ttu-id="48dfa-115">值</span><span class="sxs-lookup"><span data-stu-id="48dfa-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48dfa-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48dfa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="48dfa-117">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48dfa-117">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="48dfa-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48dfa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="48dfa-119">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48dfa-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="48dfa-120">標頭</span><span class="sxs-lookup"><span data-stu-id="48dfa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="48dfa-121"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="48dfa-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48dfa-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48dfa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48dfa-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="48dfa-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="48dfa-124">**影片防震 MFT**</span><span class="sxs-lookup"><span data-stu-id="48dfa-124">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




