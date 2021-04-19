---
description: 指定媒體會話是否在此拓撲節點所代表的媒體接收器上使用預先進行。
ms.assetid: 1781f3a0-6baa-4e06-b2eb-9a8f572aa040
title: 'MF_TOPONODE_DISABLE_PREROLL 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d031a4ee50262e717731ae517d4441e9be9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988418"
---
# <a name="mf_toponode_disable_preroll-attribute"></a><span data-ttu-id="0d425-103">MF TOPONODE 停用預先進行的 \_ \_ \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="0d425-103">MF\_TOPONODE\_DISABLE\_PREROLL attribute</span></span>

<span data-ttu-id="0d425-104">指定媒體會話是否在此拓撲節點所代表的媒體接收器上使用預先進行。</span><span class="sxs-lookup"><span data-stu-id="0d425-104">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="0d425-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="0d425-105">Data type</span></span>

<span data-ttu-id="0d425-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0d425-106">**UINT32**</span></span>

<span data-ttu-id="0d425-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="0d425-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d425-108">備註</span><span class="sxs-lookup"><span data-stu-id="0d425-108">Remarks</span></span>

<span data-ttu-id="0d425-109">這個屬性會套用至 (**MF \_ 拓撲 \_ 輸出 \_ 節點**) 的輸出節點。</span><span class="sxs-lookup"><span data-stu-id="0d425-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="0d425-110">如果這個屬性的值為 **TRUE**，則即使媒體接收器公開 [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) 介面，媒體會話也不會將任何資料預先寫入媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="0d425-110">If the value of this attribute is **TRUE**, the Media Session does not preroll any data to the media sink, even if the media sink exposes the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span> <span data-ttu-id="0d425-111">如果此值為 **FALSE**，則媒體會話會在媒體接收器執行 **IMFMediaSinkPreroll** 時 prerolls 資料。</span><span class="sxs-lookup"><span data-stu-id="0d425-111">If the value is **FALSE**, the Media Session prerolls data if the media sink implements **IMFMediaSinkPreroll**.</span></span> <span data-ttu-id="0d425-112">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0d425-112">The default value is **FALSE**.</span></span>

<span data-ttu-id="0d425-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="0d425-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d425-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d425-114">Requirements</span></span>



| <span data-ttu-id="0d425-115">需求</span><span class="sxs-lookup"><span data-stu-id="0d425-115">Requirement</span></span> | <span data-ttu-id="0d425-116">值</span><span class="sxs-lookup"><span data-stu-id="0d425-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d425-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d425-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0d425-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d425-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0d425-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d425-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0d425-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d425-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0d425-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0d425-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d425-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d425-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d425-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d425-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d425-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="0d425-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0d425-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0d425-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0d425-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0d425-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0d425-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="0d425-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="0d425-128">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="0d425-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




