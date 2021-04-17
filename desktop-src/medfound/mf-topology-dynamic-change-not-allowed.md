---
description: 指定當資料流程的格式變更時，媒體會話是否嘗試修改拓撲。
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: 'MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ade7308c4fadef315fae0828a5c2cb29575b03a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468988"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a><span data-ttu-id="d46ee-103">MF \_ 拓撲 \_ 動態 \_ 變更 \_ 不 \_ 允許屬性</span><span class="sxs-lookup"><span data-stu-id="d46ee-103">MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute</span></span>

<span data-ttu-id="d46ee-104">指定當資料流程的格式變更時，媒體會話是否嘗試修改拓撲。</span><span class="sxs-lookup"><span data-stu-id="d46ee-104">Specifies whether the Media Session attempts to modify the topology when the format of a stream changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="d46ee-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="d46ee-105">Data type</span></span>

<span data-ttu-id="d46ee-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d46ee-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="d46ee-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="d46ee-107">Get/set</span></span>

<span data-ttu-id="d46ee-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="d46ee-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d46ee-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="d46ee-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d46ee-110">適用於</span><span class="sxs-lookup"><span data-stu-id="d46ee-110">Applies to</span></span>

[<span data-ttu-id="d46ee-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="d46ee-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="d46ee-112">備註</span><span class="sxs-lookup"><span data-stu-id="d46ee-112">Remarks</span></span>

<span data-ttu-id="d46ee-113">如果串流期間的資料流程格式有所變更，則此屬性會控制媒體會話的回應方式。</span><span class="sxs-lookup"><span data-stu-id="d46ee-113">This attribute controls how the Media Session responds if the format of a stream changes during streaming.</span></span>

<span data-ttu-id="d46ee-114">如果格式變更，而 [MF \_ 拓撲 \_ 動態 \_ 變更 \_ 不 \_ 允許] 屬性為 **FALSE**，則媒體會話可能會將新節點插入拓撲中，以符合新的格式。</span><span class="sxs-lookup"><span data-stu-id="d46ee-114">If the format changes and the MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute is **FALSE**, the Media Session might insert new nodes into the topology to match the new format.</span></span> <span data-ttu-id="d46ee-115">例如，如果影片大小變更，媒體會話可能會新增媒體基礎轉換 (MFT) 調整影片的大小。</span><span class="sxs-lookup"><span data-stu-id="d46ee-115">For example, if the video size changes, the Media Session might add a Media Foundation transform (MFT) that resizes the video.</span></span> <span data-ttu-id="d46ee-116">否則，如果屬性為 **TRUE**，則媒體會話不會修改拓撲。</span><span class="sxs-lookup"><span data-stu-id="d46ee-116">Otherwise, if the attribute is **TRUE**, the Media Session will not modify the topology.</span></span>

<span data-ttu-id="d46ee-117">這個屬性的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d46ee-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="d46ee-118">建議的值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d46ee-118">The recommended value is **FALSE**.</span></span>

<span data-ttu-id="d46ee-119">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="d46ee-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d46ee-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d46ee-120">Requirements</span></span>



| <span data-ttu-id="d46ee-121">需求</span><span class="sxs-lookup"><span data-stu-id="d46ee-121">Requirement</span></span> | <span data-ttu-id="d46ee-122">值</span><span class="sxs-lookup"><span data-stu-id="d46ee-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d46ee-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d46ee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d46ee-124">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d46ee-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d46ee-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d46ee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d46ee-126">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d46ee-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d46ee-127">標頭</span><span class="sxs-lookup"><span data-stu-id="d46ee-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d46ee-128"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d46ee-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d46ee-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d46ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d46ee-130">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="d46ee-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d46ee-131">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="d46ee-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




