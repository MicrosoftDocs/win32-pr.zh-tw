---
description: 指定嘗試解析拓撲的狀態。
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: 'MF_TOPOLOGY_RESOLUTION_STATUS 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848521"
---
# <a name="mf_topology_resolution_status-attribute"></a><span data-ttu-id="66990-103">MF \_ 拓撲 \_ 解析 \_ 狀態屬性</span><span class="sxs-lookup"><span data-stu-id="66990-103">MF\_TOPOLOGY\_RESOLUTION\_STATUS attribute</span></span>

<span data-ttu-id="66990-104">指定嘗試解析拓撲的狀態。</span><span class="sxs-lookup"><span data-stu-id="66990-104">Specifies the status of an attempt to resolve a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="66990-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="66990-105">Data type</span></span>

<span data-ttu-id="66990-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="66990-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="66990-107">備註</span><span class="sxs-lookup"><span data-stu-id="66990-107">Remarks</span></span>

<span data-ttu-id="66990-108">拓撲載入器或媒體會話可能會在拓撲上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="66990-108">The topology loader or the Media Session might set this attribute on a topology.</span></span> <span data-ttu-id="66990-109">這個屬性的值是來自于 [**MF \_ 拓撲 \_ 解析 \_ 狀態 \_ 旗標**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags)列舉的位 **or** of 旗標。</span><span class="sxs-lookup"><span data-stu-id="66990-109">The value of this attribute is a bitwise **OR** of flags from the [**MF\_TOPOLOGY\_RESOLUTION\_STATUS\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) enumeration.</span></span>

<span data-ttu-id="66990-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="66990-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="66990-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="66990-111">Requirements</span></span>



| <span data-ttu-id="66990-112">需求</span><span class="sxs-lookup"><span data-stu-id="66990-112">Requirement</span></span> | <span data-ttu-id="66990-113">值</span><span class="sxs-lookup"><span data-stu-id="66990-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66990-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66990-114">Minimum supported client</span></span><br/> | <span data-ttu-id="66990-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66990-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="66990-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66990-116">Minimum supported server</span></span><br/> | <span data-ttu-id="66990-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66990-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="66990-118">標頭</span><span class="sxs-lookup"><span data-stu-id="66990-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="66990-119"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="66990-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66990-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66990-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66990-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="66990-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="66990-122">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="66990-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="66990-123">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="66990-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="66990-124">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="66990-124">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[<span data-ttu-id="66990-125">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="66990-125">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




