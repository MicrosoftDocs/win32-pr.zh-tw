---
description: 指定是否要載入以硬體為基礎的 Microsoft 媒體基礎轉換 (拓撲中的 MFTs) 。
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: 'MF_TOPOLOGY_HARDWARE_MODE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec7933e9a380bbf5e66f4030a214f3f4aa93abc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971151"
---
# <a name="mf_topology_hardware_mode-attribute"></a><span data-ttu-id="d2347-103">MF \_ 拓撲 \_ 硬體 \_ 模式屬性</span><span class="sxs-lookup"><span data-stu-id="d2347-103">MF\_TOPOLOGY\_HARDWARE\_MODE attribute</span></span>

<span data-ttu-id="d2347-104">指定是否要載入以硬體為基礎的 Microsoft 媒體基礎轉換 (拓撲中的 MFTs) 。</span><span class="sxs-lookup"><span data-stu-id="d2347-104">Specifies whether to load hardware-based Microsoft Media Foundation transforms (MFTs) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="d2347-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="d2347-105">Data type</span></span>

<span data-ttu-id="d2347-106">**[**MFTOPOLOGY \_以 \_**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** **UINT32** 形式儲存的硬體模式</span><span class="sxs-lookup"><span data-stu-id="d2347-106">**[**MFTOPOLOGY\_HARDWARE\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="d2347-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="d2347-107">Get/set</span></span>

<span data-ttu-id="d2347-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="d2347-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d2347-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="d2347-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d2347-110">適用於</span><span class="sxs-lookup"><span data-stu-id="d2347-110">Applies to</span></span>

[<span data-ttu-id="d2347-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="d2347-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="d2347-112">備註</span><span class="sxs-lookup"><span data-stu-id="d2347-112">Remarks</span></span>

<span data-ttu-id="d2347-113">此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="d2347-113">This attribute is optional.</span></span> <span data-ttu-id="d2347-114">在解析拓撲之前，請先設定屬性。</span><span class="sxs-lookup"><span data-stu-id="d2347-114">Set the attribute before resolving the topology.</span></span>



| <span data-ttu-id="d2347-115">值</span><span class="sxs-lookup"><span data-stu-id="d2347-115">Value</span></span>                                  | <span data-ttu-id="d2347-116">描述</span><span class="sxs-lookup"><span data-stu-id="d2347-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2347-117">**MFTOPOLOGY \_ HWMODE \_ 使用 \_ 硬體**</span><span class="sxs-lookup"><span data-stu-id="d2347-117">**MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**</span></span>  | <span data-ttu-id="d2347-118">拓撲載入器會載入以硬體為基礎的 MFTs，例如硬體解碼器（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d2347-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="d2347-119">如果找不到硬體解碼器，或硬體解碼器因為某些原因而無法連線，拓撲載入器會自動切換回軟體解碼。</span><span class="sxs-lookup"><span data-stu-id="d2347-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="d2347-120">**\_ \_ 僅限 MFTOPOLOGY HWMODE SOFTWARE \_**</span><span class="sxs-lookup"><span data-stu-id="d2347-120">**MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**</span></span> | <span data-ttu-id="d2347-121">拓撲載入器只會載入軟體 MFTs，包括軟體解碼器。</span><span class="sxs-lookup"><span data-stu-id="d2347-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="d2347-122">預設值為 **MFTOPOLOGY \_ HWMODE \_ SOFTWARE \_**，以與現有的應用程式相容。</span><span class="sxs-lookup"><span data-stu-id="d2347-122">The default value is **MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**, for compatibility with existing applications.</span></span> <span data-ttu-id="d2347-123">建議的值為 **MFTOPOLOGY \_ HWMODE \_ USE \_ 硬體**。</span><span class="sxs-lookup"><span data-stu-id="d2347-123">The recommended value is **MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**.</span></span>

<span data-ttu-id="d2347-124">如果拓撲載入器將硬體 MFT 插入拓撲中，它會在 [拓撲] 節點上設定 [ [mft \_ 列舉 \_ 硬體 \_ URL] \_ 屬性](mft-enum-hardware-url-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="d2347-124">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="d2347-125">若要檢查硬體 MFT 是否存在，請列舉已解析拓撲中的節點，並檢查此屬性是否存在。</span><span class="sxs-lookup"><span data-stu-id="d2347-125">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="d2347-126">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="d2347-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2347-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2347-127">Requirements</span></span>



| <span data-ttu-id="d2347-128">需求</span><span class="sxs-lookup"><span data-stu-id="d2347-128">Requirement</span></span> | <span data-ttu-id="d2347-129">值</span><span class="sxs-lookup"><span data-stu-id="d2347-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d2347-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2347-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d2347-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2347-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d2347-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2347-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d2347-133">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2347-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d2347-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d2347-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2347-135"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2347-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2347-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2347-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2347-137">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="d2347-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d2347-138">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="d2347-138">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




