---
description: 指定拓撲是否有全域開始和停止時間。
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: 'MF_SESSION_GLOBAL_TIME 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981009"
---
# <a name="mf_session_global_time-attribute"></a><span data-ttu-id="9116b-103">MF \_ 會話 \_ GLOBAL \_ TIME 屬性</span><span class="sxs-lookup"><span data-stu-id="9116b-103">MF\_SESSION\_GLOBAL\_TIME attribute</span></span>

<span data-ttu-id="9116b-104">指定拓撲是否有全域開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="9116b-104">Specifies whether topologies have a global start and stop time.</span></span>

## <a name="data-type"></a><span data-ttu-id="9116b-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9116b-105">Data type</span></span>

<span data-ttu-id="9116b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9116b-106">**UINT32**</span></span>

<span data-ttu-id="9116b-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="9116b-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9116b-108">備註</span><span class="sxs-lookup"><span data-stu-id="9116b-108">Remarks</span></span>

<span data-ttu-id="9116b-109">當您使用 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)或 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函數的 *pConfiguration* 參數建立媒體 sesison 時，可以設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="9116b-109">You can set this attribute when you create the media sesison by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="9116b-110">如果此屬性存在且為非零值，則傳遞至媒體會話的所有拓撲都必須有 [**mf \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) 和 [**mf \_ 拓撲 \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="9116b-110">If this attribute is present and nonzero, then all topologies passed to the Media Session must have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) and [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attributes.</span></span> <span data-ttu-id="9116b-111">這些屬性會指定拓撲的開始和停止時間（相對於整個展示）。</span><span class="sxs-lookup"><span data-stu-id="9116b-111">These attributes specify the start and stop times for the topology relative to the entire presentation.</span></span>

<span data-ttu-id="9116b-112">如果這個屬性不存在或 **為 FALSE**，則拓撲不能有 [**mf \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) 或 [**mf \_ 拓撲 \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="9116b-112">If this attribute is absent or **FALSE**, the topologies must not have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) or [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attribute.</span></span>

<span data-ttu-id="9116b-113">使用這個屬性來建立編輯順序。</span><span class="sxs-lookup"><span data-stu-id="9116b-113">Use this attribute to create editing sequences.</span></span> <span data-ttu-id="9116b-114">如需詳細資訊，請參閱 [順序呈現時間](sequence-presentation-times.md)。</span><span class="sxs-lookup"><span data-stu-id="9116b-114">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="9116b-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="9116b-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9116b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9116b-116">Requirements</span></span>



| <span data-ttu-id="9116b-117">需求</span><span class="sxs-lookup"><span data-stu-id="9116b-117">Requirement</span></span> | <span data-ttu-id="9116b-118">值</span><span class="sxs-lookup"><span data-stu-id="9116b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9116b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9116b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9116b-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9116b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9116b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9116b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9116b-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9116b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9116b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9116b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9116b-124"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9116b-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9116b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9116b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9116b-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="9116b-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9116b-127">媒體會話屬性</span><span class="sxs-lookup"><span data-stu-id="9116b-127">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="9116b-128">順序呈現時間</span><span class="sxs-lookup"><span data-stu-id="9116b-128">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="9116b-129">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9116b-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9116b-130">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9116b-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="9116b-131">**MF \_ 拓撲 \_ PROJECTSTART**</span><span class="sxs-lookup"><span data-stu-id="9116b-131">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)
</dt> <dt>

[<span data-ttu-id="9116b-132">**MF \_ 拓撲 \_ PROJECTSTOP**</span><span class="sxs-lookup"><span data-stu-id="9116b-132">**MF\_TOPOLOGY\_PROJECTSTOP**</span></span>](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




