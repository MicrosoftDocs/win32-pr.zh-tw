---
description: 指定與拓撲節點相關聯的轉換是否支援 (DXVA) 的 DirectX Video 加速。
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: 'MF_TOPONODE_D3DAWARE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d94d06f2834092159fb813ecffd69ec8a157c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469492"
---
# <a name="mf_toponode_d3daware-attribute"></a><span data-ttu-id="209a1-103">MF \_ TOPONODE \_ D3DAWARE 屬性</span><span class="sxs-lookup"><span data-stu-id="209a1-103">MF\_TOPONODE\_D3DAWARE attribute</span></span>

<span data-ttu-id="209a1-104">指定與拓撲節點相關聯的轉換是否支援 (DXVA) 的 DirectX Video 加速。</span><span class="sxs-lookup"><span data-stu-id="209a1-104">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA).</span></span>

## <a name="data-type"></a><span data-ttu-id="209a1-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="209a1-105">Data type</span></span>

<span data-ttu-id="209a1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="209a1-106">**UINT32**</span></span>

<span data-ttu-id="209a1-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="209a1-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="209a1-108">備註</span><span class="sxs-lookup"><span data-stu-id="209a1-108">Remarks</span></span>

<span data-ttu-id="209a1-109">這個屬性會套用至 (**MF \_ 拓撲 \_ 轉換 \_ 節點**) 的轉換節點。</span><span class="sxs-lookup"><span data-stu-id="209a1-109">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="209a1-110">應用程式通常不會直接使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="209a1-110">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="209a1-111">當基礎媒體基礎轉換具有 [**MF \_ SA \_ D3D \_ 感知**](mf-sa-d3d-aware-attribute.md) 屬性時，媒體會話會在轉換節點上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="209a1-111">The Media Session sets this attribute on a transform node if the underlying Media Foundation transform has the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute.</span></span>

<span data-ttu-id="209a1-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="209a1-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="209a1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="209a1-113">Requirements</span></span>



| <span data-ttu-id="209a1-114">需求</span><span class="sxs-lookup"><span data-stu-id="209a1-114">Requirement</span></span> | <span data-ttu-id="209a1-115">值</span><span class="sxs-lookup"><span data-stu-id="209a1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="209a1-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="209a1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="209a1-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="209a1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="209a1-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="209a1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="209a1-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="209a1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="209a1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="209a1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="209a1-121"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="209a1-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="209a1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="209a1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="209a1-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="209a1-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="209a1-124">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="209a1-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="209a1-125">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="209a1-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="209a1-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="209a1-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="209a1-127">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="209a1-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




