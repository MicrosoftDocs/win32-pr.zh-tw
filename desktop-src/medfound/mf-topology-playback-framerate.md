---
description: 指定監視器的重新整理頻率。
ms.assetid: deeb780c-2dc2-4a9a-926a-23b9ae3bedd5
title: 'MF_TOPOLOGY_PLAYBACK_FRAMERATE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d7ff7dbc893065ebb378557f0731cd8826582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191881"
---
# <a name="mf_topology_playback_framerate-attribute"></a><span data-ttu-id="e7709-103">MF \_ 拓撲 \_ 播放 \_ 畫面播放速率屬性</span><span class="sxs-lookup"><span data-stu-id="e7709-103">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE attribute</span></span>

<span data-ttu-id="e7709-104">指定監視器的重新整理頻率。</span><span class="sxs-lookup"><span data-stu-id="e7709-104">Specifies the monitor refresh rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="e7709-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e7709-105">Data type</span></span>

<span data-ttu-id="e7709-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="e7709-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="e7709-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="e7709-107">Get/set</span></span>

<span data-ttu-id="e7709-108">若要取得這個屬性，請呼叫 [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio)。</span><span class="sxs-lookup"><span data-stu-id="e7709-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="e7709-109">若要設定這個屬性，請呼叫 [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio)。</span><span class="sxs-lookup"><span data-stu-id="e7709-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e7709-110">適用於</span><span class="sxs-lookup"><span data-stu-id="e7709-110">Applies to</span></span>

[<span data-ttu-id="e7709-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="e7709-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="e7709-112">備註</span><span class="sxs-lookup"><span data-stu-id="e7709-112">Remarks</span></span>

<span data-ttu-id="e7709-113">拓撲載入器會使用此屬性，在播放開始之前將管線優化。</span><span class="sxs-lookup"><span data-stu-id="e7709-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="e7709-114">如果設定此屬性，也請將 [ [MF \_ 拓撲 \_ 靜態 \_ 播放 \_ 優化](mf-topology-static-playback-optimizations.md) ] 屬性設定為 [ **TRUE**]。</span><span class="sxs-lookup"><span data-stu-id="e7709-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="e7709-115">畫面播放速率以比例表示。</span><span class="sxs-lookup"><span data-stu-id="e7709-115">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="e7709-116">屬性值的上方32位包含分子，而較低的32位則包含分母。</span><span class="sxs-lookup"><span data-stu-id="e7709-116">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span>

<span data-ttu-id="e7709-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="e7709-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7709-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7709-118">Requirements</span></span>



| <span data-ttu-id="e7709-119">需求</span><span class="sxs-lookup"><span data-stu-id="e7709-119">Requirement</span></span> | <span data-ttu-id="e7709-120">值</span><span class="sxs-lookup"><span data-stu-id="e7709-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7709-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7709-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e7709-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7709-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e7709-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7709-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e7709-124">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7709-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e7709-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e7709-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7709-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7709-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7709-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7709-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7709-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e7709-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e7709-129">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="e7709-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="e7709-130">影片品質管制</span><span class="sxs-lookup"><span data-stu-id="e7709-130">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




