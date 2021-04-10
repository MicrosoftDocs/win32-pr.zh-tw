---
description: 指定影片播放的目的地視窗大小。
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: 'MF_TOPOLOGY_PLAYBACK_MAX_DIMS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1fc6a57c5e031bc6f35f36e688bd44986f541b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191880"
---
# <a name="mf_topology_playback_max_dims-attribute"></a><span data-ttu-id="86c18-103">MF \_ 拓撲 \_ 播放 \_ 最大 \_ 亮度屬性</span><span class="sxs-lookup"><span data-stu-id="86c18-103">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS attribute</span></span>

<span data-ttu-id="86c18-104">指定影片播放的目的地視窗大小。</span><span class="sxs-lookup"><span data-stu-id="86c18-104">Specifies the size of the destination window for video playback.</span></span>

## <a name="data-type"></a><span data-ttu-id="86c18-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="86c18-105">Data type</span></span>

<span data-ttu-id="86c18-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="86c18-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="86c18-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="86c18-107">Get/set</span></span>

<span data-ttu-id="86c18-108">若要取得這個屬性，請呼叫 [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize)。</span><span class="sxs-lookup"><span data-stu-id="86c18-108">To get this attribute, call [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).</span></span>

<span data-ttu-id="86c18-109">若要設定這個屬性，請呼叫 [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize)。</span><span class="sxs-lookup"><span data-stu-id="86c18-109">To set this attribute, call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).</span></span>

## <a name="applies-to"></a><span data-ttu-id="86c18-110">適用於</span><span class="sxs-lookup"><span data-stu-id="86c18-110">Applies to</span></span>

[<span data-ttu-id="86c18-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="86c18-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="86c18-112">備註</span><span class="sxs-lookup"><span data-stu-id="86c18-112">Remarks</span></span>

<span data-ttu-id="86c18-113">拓撲載入器會使用此屬性，在播放開始之前將管線優化。</span><span class="sxs-lookup"><span data-stu-id="86c18-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="86c18-114">如果設定此屬性，也請將 [ [MF \_ 拓撲 \_ 靜態 \_ 播放 \_ 優化](mf-topology-static-playback-optimizations.md) ] 屬性設定為 [ **TRUE**]。</span><span class="sxs-lookup"><span data-stu-id="86c18-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="86c18-115">屬性值的上方32位包含寬度，而較低的32位則包含高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="86c18-115">The upper 32 bits of the attribute value contain the width and the lower 32 bits contain the height, both in pixels.</span></span>

<span data-ttu-id="86c18-116">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="86c18-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="86c18-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="86c18-117">Requirements</span></span>



| <span data-ttu-id="86c18-118">需求</span><span class="sxs-lookup"><span data-stu-id="86c18-118">Requirement</span></span> | <span data-ttu-id="86c18-119">值</span><span class="sxs-lookup"><span data-stu-id="86c18-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="86c18-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86c18-120">Minimum supported client</span></span><br/> | <span data-ttu-id="86c18-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86c18-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="86c18-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86c18-122">Minimum supported server</span></span><br/> | <span data-ttu-id="86c18-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86c18-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="86c18-124">標頭</span><span class="sxs-lookup"><span data-stu-id="86c18-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="86c18-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="86c18-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86c18-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86c18-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c18-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="86c18-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="86c18-128">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="86c18-128">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="86c18-129">影片品質管制</span><span class="sxs-lookup"><span data-stu-id="86c18-129">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




