---
description: 指出哪些輸出是 t 節點上的主要輸出。
ms.assetid: f7d98837-75da-48cc-8307-091be2d95392
title: 'MF_TOPONODE_PRIMARYOUTPUT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4130f1df4789ad910ae013eab43168983b47c316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318643"
---
# <a name="mf_toponode_primaryoutput-attribute"></a><span data-ttu-id="03e68-103">MF \_ TOPONODE \_ PRIMARYOUTPUT 屬性</span><span class="sxs-lookup"><span data-stu-id="03e68-103">MF\_TOPONODE\_PRIMARYOUTPUT attribute</span></span>

<span data-ttu-id="03e68-104">指出哪些輸出是 t 節點上的主要輸出。</span><span class="sxs-lookup"><span data-stu-id="03e68-104">Indicates which output is the primary output on a tee node.</span></span>

## <a name="data-type"></a><span data-ttu-id="03e68-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="03e68-105">Data type</span></span>

<span data-ttu-id="03e68-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="03e68-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="03e68-107">備註</span><span class="sxs-lookup"><span data-stu-id="03e68-107">Remarks</span></span>

<span data-ttu-id="03e68-108">這個屬性會套用至 (**MF \_ 拓撲 \_ t \_** a t a t a t 節點) 的 t 節點。</span><span class="sxs-lookup"><span data-stu-id="03e68-108">This attribute applies to tee nodes (**MF\_TOPOLOGY\_TEE\_NODE**).</span></span>

<span data-ttu-id="03e68-109">這個屬性的值是這個指標節點上輸出連接的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="03e68-109">The value of this attribute is the zero-based index of an output connection on this tee node.</span></span> <span data-ttu-id="03e68-110">此值指出哪些輸出是主要輸出資料流程。</span><span class="sxs-lookup"><span data-stu-id="03e68-110">This value indicates which output is the primary output stream.</span></span> <span data-ttu-id="03e68-111">管線會等待來自主要輸出的要求，然後再處理來自其他輸出的要求。</span><span class="sxs-lookup"><span data-stu-id="03e68-111">The pipeline waits for a request from the primary output before processing requests from the other outputs.</span></span>

<span data-ttu-id="03e68-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="03e68-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="03e68-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="03e68-113">Requirements</span></span>



| <span data-ttu-id="03e68-114">需求</span><span class="sxs-lookup"><span data-stu-id="03e68-114">Requirement</span></span> | <span data-ttu-id="03e68-115">值</span><span class="sxs-lookup"><span data-stu-id="03e68-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03e68-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03e68-116">Minimum supported client</span></span><br/> | <span data-ttu-id="03e68-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03e68-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="03e68-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03e68-118">Minimum supported server</span></span><br/> | <span data-ttu-id="03e68-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03e68-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="03e68-120">標頭</span><span class="sxs-lookup"><span data-stu-id="03e68-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="03e68-121"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="03e68-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03e68-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03e68-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03e68-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="03e68-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="03e68-124">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="03e68-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="03e68-125">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="03e68-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="03e68-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="03e68-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="03e68-127">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="03e68-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




