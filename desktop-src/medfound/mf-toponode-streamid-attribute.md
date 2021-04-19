---
description: 與此拓撲節點相關聯之資料流程接收的資料流程識別碼。
ms.assetid: 0b8060ab-1463-45c2-8277-d15122561248
title: 'MF_TOPONODE_STREAMID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2377183927cf75c6e0a7436384426dcab94680c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986388"
---
# <a name="mf_toponode_streamid-attribute"></a><span data-ttu-id="19565-103">MF \_ TOPONODE \_ STREAMID 屬性</span><span class="sxs-lookup"><span data-stu-id="19565-103">MF\_TOPONODE\_STREAMID attribute</span></span>

<span data-ttu-id="19565-104">與此拓撲節點相關聯之資料流程接收的資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="19565-104">The stream identifier of the stream sink associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="19565-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="19565-105">Data type</span></span>

<span data-ttu-id="19565-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="19565-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="19565-107">備註</span><span class="sxs-lookup"><span data-stu-id="19565-107">Remarks</span></span>

<span data-ttu-id="19565-108">這個屬性會套用至 (**MF \_ 拓撲 \_ 輸出 \_ 節點**) 的輸出節點。</span><span class="sxs-lookup"><span data-stu-id="19565-108">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="19565-109">當媒體會話載入拓撲時，它會查詢具有指定識別碼之資料流程接收的媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="19565-109">When the Media Session loads the topology, it queries the media sink for a stream sink with the specified identifier.</span></span> <span data-ttu-id="19565-110">如果失敗，則會嘗試將新的資料流程接收新增至媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="19565-110">If that fails, it attempts to add a new stream sink to the media sink.</span></span>

<span data-ttu-id="19565-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="19565-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="19565-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="19565-112">Requirements</span></span>



| <span data-ttu-id="19565-113">需求</span><span class="sxs-lookup"><span data-stu-id="19565-113">Requirement</span></span> | <span data-ttu-id="19565-114">值</span><span class="sxs-lookup"><span data-stu-id="19565-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19565-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19565-115">Minimum supported client</span></span><br/> | <span data-ttu-id="19565-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19565-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="19565-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19565-117">Minimum supported server</span></span><br/> | <span data-ttu-id="19565-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19565-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="19565-119">標頭</span><span class="sxs-lookup"><span data-stu-id="19565-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="19565-120"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="19565-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19565-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19565-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19565-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="19565-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="19565-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="19565-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="19565-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="19565-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="19565-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="19565-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="19565-126">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="19565-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




