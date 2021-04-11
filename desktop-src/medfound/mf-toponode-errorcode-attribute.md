---
description: 包含此拓撲節點最近連接失敗的錯誤碼。
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: 'MF_TOPONODE_ERRORCODE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114028"
---
# <a name="mf_toponode_errorcode-attribute"></a><span data-ttu-id="a5d56-103">MF \_ TOPONODE \_ ERRORCODE 屬性</span><span class="sxs-lookup"><span data-stu-id="a5d56-103">MF\_TOPONODE\_ERRORCODE attribute</span></span>

<span data-ttu-id="a5d56-104">包含此拓撲節點最近連接失敗的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a5d56-104">Contains the error code from the most recent connection failure for this toplogy node.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5d56-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a5d56-105">Data type</span></span>

<span data-ttu-id="a5d56-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a5d56-106">**UINT32**</span></span>

<span data-ttu-id="a5d56-107">Ttreat 為 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a5d56-107">Ttreat as an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5d56-108">備註</span><span class="sxs-lookup"><span data-stu-id="a5d56-108">Remarks</span></span>

<span data-ttu-id="a5d56-109">這個屬性會套用至所有節點類型。</span><span class="sxs-lookup"><span data-stu-id="a5d56-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="a5d56-110">這個屬性的值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a5d56-110">The value of this attribute is an **HRESULT** value.</span></span>

<span data-ttu-id="a5d56-111">媒體會話或拓撲載入器可能會設定屬性。</span><span class="sxs-lookup"><span data-stu-id="a5d56-111">The Media Session or the topology loader might set the attribute.</span></span> <span data-ttu-id="a5d56-112">應用程式通常會讀取此屬性，但不會設定它。</span><span class="sxs-lookup"><span data-stu-id="a5d56-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="a5d56-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="a5d56-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5d56-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5d56-114">Requirements</span></span>



| <span data-ttu-id="a5d56-115">需求</span><span class="sxs-lookup"><span data-stu-id="a5d56-115">Requirement</span></span> | <span data-ttu-id="a5d56-116">值</span><span class="sxs-lookup"><span data-stu-id="a5d56-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d56-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5d56-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a5d56-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5d56-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a5d56-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5d56-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a5d56-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5d56-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a5d56-121">標頭</span><span class="sxs-lookup"><span data-stu-id="a5d56-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5d56-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5d56-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5d56-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5d56-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5d56-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a5d56-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5d56-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a5d56-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a5d56-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a5d56-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a5d56-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="a5d56-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="a5d56-128">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="a5d56-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




