---
description: 當連接器未提供輸出保護時，此屬性會指定 (OTA) 的影片輸出信任授權單位所提供的額外保護。
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: 'MFPROTECTION_CONSTRICTVIDEO_NOOPM 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617bd629852a3aa03708d12dca7736b4f773094b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943737"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a><span data-ttu-id="e5a51-103">MFPROTECTION \_ CONSTRICTVIDEO \_ NOOPM 屬性</span><span class="sxs-lookup"><span data-stu-id="e5a51-103">MFPROTECTION\_CONSTRICTVIDEO\_NOOPM attribute</span></span>

<span data-ttu-id="e5a51-104">當連接器未提供輸出保護時，此屬性會指定 (OTA) 的影片輸出信任授權單位所提供的額外保護。</span><span class="sxs-lookup"><span data-stu-id="e5a51-104">This attribute specifies additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="e5a51-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e5a51-105">Data type</span></span>

<span data-ttu-id="e5a51-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="e5a51-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="e5a51-107">備註</span><span class="sxs-lookup"><span data-stu-id="e5a51-107">Remarks</span></span>

<span data-ttu-id="e5a51-108">這是 (OTA) 的影片輸出信任授權單位所提供的額外保護。當連接器不提供輸出保護時 (請參閱 [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)) 。</span><span class="sxs-lookup"><span data-stu-id="e5a51-108">This is an additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection (see [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)).</span></span> <span data-ttu-id="e5a51-109">在此情況下，OTA 可能會提供這項保護，其效果與 [MFPROTECTION \_ CONSTRICTVIDEO](mfprotection-constrictvideo.md) 防護相同。</span><span class="sxs-lookup"><span data-stu-id="e5a51-109">In this case the OTA may offer this protection whose effect is the same as the [MFPROTECTION\_CONSTRICTVIDEO](mfprotection-constrictvideo.md) protection.</span></span> <span data-ttu-id="e5a51-110">這是為了避免與先前呼叫 [**IMFOutputPolicy：： GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) 互動造成混淆，其中使用了 MFPROTECTION \_ CONSTRICTVIDEO 保護來協助識別桌面視窗管理員虛擬連接器。</span><span class="sxs-lookup"><span data-stu-id="e5a51-110">This is defined to avoid confusion with previous calls to [**IMFOutputPolicy::GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) interactions where the presence of MFPROTECTION\_CONSTRICTVIDEO protection was used to help identify the desktop window manager pseudo-connector.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5a51-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5a51-111">Requirements</span></span>



| <span data-ttu-id="e5a51-112">需求</span><span class="sxs-lookup"><span data-stu-id="e5a51-112">Requirement</span></span> | <span data-ttu-id="e5a51-113">值</span><span class="sxs-lookup"><span data-stu-id="e5a51-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a51-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5a51-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e5a51-115">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5a51-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e5a51-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5a51-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e5a51-117">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5a51-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e5a51-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e5a51-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5a51-119"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e5a51-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5a51-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5a51-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a51-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e5a51-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




