---
description: 指出 Microsoft 媒體基礎轉換 (MFT) 需要配置給漸進式內容的樣本數。
ms.assetid: 69F9EA59-41B4-4DE5-A77D-1D0E59BFBF3A
title: 'MF_SA_REQUIRED_SAMPLE_COUNT_PROGRESSIVE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e48d56bf1e21a64c0a4d225a72a6386b4789ae7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943642"
---
# <a name="mf_sa_required_sample_count_progressive-attribute"></a><span data-ttu-id="09d0b-103">MF \_ SA \_ 必要 \_ 範例 \_ 計數 \_ 漸進屬性</span><span class="sxs-lookup"><span data-stu-id="09d0b-103">MF\_SA\_REQUIRED\_SAMPLE\_COUNT\_PROGRESSIVE attribute</span></span>

<span data-ttu-id="09d0b-104">指出 Microsoft 媒體基礎轉換 (MFT) 需要配置給漸進式內容的樣本數。</span><span class="sxs-lookup"><span data-stu-id="09d0b-104">Indicates the number of samples that a Microsoft Media Foundation transform (MFT) requires to be allocated for progressive content.</span></span>

## <a name="data-type"></a><span data-ttu-id="09d0b-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="09d0b-105">Data type</span></span>

<span data-ttu-id="09d0b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="09d0b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="09d0b-107">備註</span><span class="sxs-lookup"><span data-stu-id="09d0b-107">Remarks</span></span>

<span data-ttu-id="09d0b-108">如果下一個節點下游有 [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)，就會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="09d0b-108">This value is used if the next node downstream has an [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span></span>

## <a name="requirements"></a><span data-ttu-id="09d0b-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="09d0b-109">Requirements</span></span>



| <span data-ttu-id="09d0b-110">需求</span><span class="sxs-lookup"><span data-stu-id="09d0b-110">Requirement</span></span> | <span data-ttu-id="09d0b-111">值</span><span class="sxs-lookup"><span data-stu-id="09d0b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09d0b-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09d0b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="09d0b-113">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09d0b-113">Windows 8 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="09d0b-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09d0b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="09d0b-115">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09d0b-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="09d0b-116">標頭</span><span class="sxs-lookup"><span data-stu-id="09d0b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="09d0b-117"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="09d0b-117"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09d0b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09d0b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09d0b-119">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="09d0b-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




