---
description: 指定拓撲載入器是否會啟用拓撲中的 Microsoft DirectX Video 加速 (DXVA) 。
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: 'MF_TOPOLOGY_DXVA_MODE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad75b37a2ca2e971077b05d1bbeb92748530614
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972624"
---
# <a name="mf_topology_dxva_mode-attribute"></a><span data-ttu-id="6ffc2-103">MF \_ 拓撲 \_ DXVA \_ 模式屬性</span><span class="sxs-lookup"><span data-stu-id="6ffc2-103">MF\_TOPOLOGY\_DXVA\_MODE attribute</span></span>

<span data-ttu-id="6ffc2-104">指定拓撲載入器是否會啟用拓撲中的 Microsoft DirectX Video 加速 (DXVA) 。</span><span class="sxs-lookup"><span data-stu-id="6ffc2-104">Specifies whether the topology loader enables Microsoft DirectX Video Acceleration (DXVA) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="6ffc2-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="6ffc2-105">Data type</span></span>

<span data-ttu-id="6ffc2-106">**[**MFTOPOLOGY \_以 \_**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** **UINT32** 形式儲存的 DXVA 模式</span><span class="sxs-lookup"><span data-stu-id="6ffc2-106">**[**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="6ffc2-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="6ffc2-107">Get/set</span></span>

<span data-ttu-id="6ffc2-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="6ffc2-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6ffc2-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="6ffc2-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="6ffc2-110">適用於</span><span class="sxs-lookup"><span data-stu-id="6ffc2-110">Applies to</span></span>

[<span data-ttu-id="6ffc2-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="6ffc2-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="6ffc2-112">備註</span><span class="sxs-lookup"><span data-stu-id="6ffc2-112">Remarks</span></span>

<span data-ttu-id="6ffc2-113">這個屬性的值是 [**MFTOPOLOGY \_ DXVA \_ 模式**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) 列舉常數。</span><span class="sxs-lookup"><span data-stu-id="6ffc2-113">The value of this attribute is an [**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) enumeration constant.</span></span> <span data-ttu-id="6ffc2-114">預設值為 **MFTOPOLOGY \_ DXVA \_ default**。</span><span class="sxs-lookup"><span data-stu-id="6ffc2-114">The default value is **MFTOPOLOGY\_DXVA\_DEFAULT**.</span></span>

<span data-ttu-id="6ffc2-115">這個屬性會控制哪些 MFTs 會收到 Direct3D 裝置管理員的指標。</span><span class="sxs-lookup"><span data-stu-id="6ffc2-115">This attribute controls which MFTs receive a pointer to the Direct3D device manager.</span></span> <span data-ttu-id="6ffc2-116">若要啟用完整的影片加速，請將值設定為 **MFTOPOLOGY \_ DXVA \_ full**。</span><span class="sxs-lookup"><span data-stu-id="6ffc2-116">To enable full video acceleration, set the value to **MFTOPOLOGY\_DXVA\_FULL**.</span></span> <span data-ttu-id="6ffc2-117">值 **MFTOPOLOGY \_ DXVA \_ 預設** 值是針對回溯相容性所定義，它會符合所有舊版 Microsoft 媒體基礎的行為。</span><span class="sxs-lookup"><span data-stu-id="6ffc2-117">The value **MFTOPOLOGY\_DXVA\_DEFAULT** is defined for backward compatibility; it matches the behavior of all earlier versions of Microsoft Media Foundation.</span></span>

<span data-ttu-id="6ffc2-118">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="6ffc2-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ffc2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ffc2-119">Requirements</span></span>



| <span data-ttu-id="6ffc2-120">需求</span><span class="sxs-lookup"><span data-stu-id="6ffc2-120">Requirement</span></span> | <span data-ttu-id="6ffc2-121">值</span><span class="sxs-lookup"><span data-stu-id="6ffc2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffc2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ffc2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6ffc2-123">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ffc2-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6ffc2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ffc2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6ffc2-125">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ffc2-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6ffc2-126">標頭</span><span class="sxs-lookup"><span data-stu-id="6ffc2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ffc2-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ffc2-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ffc2-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ffc2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ffc2-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="6ffc2-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6ffc2-130">Direct3D 裝置管理員</span><span class="sxs-lookup"><span data-stu-id="6ffc2-130">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="6ffc2-131">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="6ffc2-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




