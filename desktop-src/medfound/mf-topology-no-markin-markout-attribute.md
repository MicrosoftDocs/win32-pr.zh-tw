---
description: 指定管線是否修剪範例。
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: 'MF_TOPOLOGY_NO_MARKIN_MARKOUT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191882"
---
# <a name="mf_topology_no_markin_markout-attribute"></a><span data-ttu-id="214f9-103">MF \_ 拓撲 \_ NO \_ MARKIN \_ MARKOUT 屬性</span><span class="sxs-lookup"><span data-stu-id="214f9-103">MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT attribute</span></span>

<span data-ttu-id="214f9-104">指定管線是否修剪範例。</span><span class="sxs-lookup"><span data-stu-id="214f9-104">Specifies whether the pipeline trims samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="214f9-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="214f9-105">Data type</span></span>

<span data-ttu-id="214f9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="214f9-106">**UINT32**</span></span>

<span data-ttu-id="214f9-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="214f9-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="214f9-108">備註</span><span class="sxs-lookup"><span data-stu-id="214f9-108">Remarks</span></span>

<span data-ttu-id="214f9-109">根據預設，管線會修剪範例以符合正確的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="214f9-109">By default, the pipeline trims samples to match the correct presentation times.</span></span> <span data-ttu-id="214f9-110">修剪是在具有 [**mf \_ TOPONODE \_ MARKIN \_**](mf-toponode-markin-here-attribute.md) 的拓撲節點和 [**mf \_ TOPONODE \_ MARKOUT \_ 這裡**](mf-toponode-markout-here-attribute.md) 的屬性上完成。</span><span class="sxs-lookup"><span data-stu-id="214f9-110">Trimming is done at the topology nodes that have the [**MF\_TOPONODE\_MARKIN\_HERE**](mf-toponode-markin-here-attribute.md) and [**MF\_TOPONODE\_MARKOUT\_HERE**](mf-toponode-markout-here-attribute.md) attributes.</span></span> <span data-ttu-id="214f9-111">如果拓撲上的 [ **MF \_ 拓撲 \_ NO \_ MARKIN \_ MARKOUT** ] 屬性設定為 **TRUE** ，管線不會修剪範例，且會忽略 **此處的 mf \_ TOPONODE \_ MARKIN \_** 和 **mf \_ TOPONODE \_ MARKOUT \_ 這裡** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="214f9-111">If the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute is set to **TRUE** on the topology, the pipeline does not trim samples, and the **MF\_TOPONODE\_MARKIN\_HERE** and **MF\_TOPONODE\_MARKOUT\_HERE** attributes are ignored.</span></span> <span data-ttu-id="214f9-112">如果屬性未設定，或值 **為 FALSE**，則管線會修剪範例。</span><span class="sxs-lookup"><span data-stu-id="214f9-112">If the attribute is not set, or has the value **FALSE**, the pipeline trims samples.</span></span>

<span data-ttu-id="214f9-113">如果應用程式從管線接收壓縮的範例，且需要取得所有的主要畫面格，則應用程式可能會將 [ **MF \_ 拓撲 \_ NO \_ MARKIN \_ MARKOUT** ] 屬性設定為 [ **TRUE** ]，否則可能會被修剪。</span><span class="sxs-lookup"><span data-stu-id="214f9-113">An application might set the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute to **TRUE** if the application receives compressed samples from the pipeline and needs to get all of the key frames, which might otherwise be trimmed.</span></span>

<span data-ttu-id="214f9-114">這個屬性的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="214f9-114">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="214f9-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="214f9-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="214f9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="214f9-116">Requirements</span></span>



| <span data-ttu-id="214f9-117">需求</span><span class="sxs-lookup"><span data-stu-id="214f9-117">Requirement</span></span> | <span data-ttu-id="214f9-118">值</span><span class="sxs-lookup"><span data-stu-id="214f9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="214f9-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="214f9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="214f9-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="214f9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="214f9-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="214f9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="214f9-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="214f9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="214f9-123">標頭</span><span class="sxs-lookup"><span data-stu-id="214f9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="214f9-124"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="214f9-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="214f9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="214f9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214f9-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="214f9-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="214f9-127">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="214f9-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="214f9-128">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="214f9-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="214f9-129">**MF \_ TOPONODE \_ MARKIN \_ 這裡**</span><span class="sxs-lookup"><span data-stu-id="214f9-129">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="214f9-130">**MF \_ TOPONODE \_ MARKOUT \_ 這裡**</span><span class="sxs-lookup"><span data-stu-id="214f9-130">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="214f9-131">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="214f9-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




