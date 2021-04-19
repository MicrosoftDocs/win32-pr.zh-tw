---
description: 指定何時清空轉換。
ms.assetid: 68332106-d1fe-467b-8baa-1e592b9cc243
title: 'MF_TOPONODE_DRAIN 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b87d626738b82f4504673392bd0fe159e2722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967179"
---
# <a name="mf_toponode_drain-attribute"></a><span data-ttu-id="91c9a-103">MF \_ TOPONODE \_ 清空屬性</span><span class="sxs-lookup"><span data-stu-id="91c9a-103">MF\_TOPONODE\_DRAIN attribute</span></span>

<span data-ttu-id="91c9a-104">指定何時清空轉換。</span><span class="sxs-lookup"><span data-stu-id="91c9a-104">Specifies when a transform is drained.</span></span>

## <a name="data-type"></a><span data-ttu-id="91c9a-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="91c9a-105">Data type</span></span>

<span data-ttu-id="91c9a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="91c9a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="91c9a-107">備註</span><span class="sxs-lookup"><span data-stu-id="91c9a-107">Remarks</span></span>

<span data-ttu-id="91c9a-108">這個屬性會套用至 (**MF \_ 拓撲 \_ 轉換 \_ 節點**) 的轉換節點。</span><span class="sxs-lookup"><span data-stu-id="91c9a-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="91c9a-109">屬性的值是 [**MF \_ TOPONODE \_ 清空 \_ 模式**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="91c9a-109">The value of the attribute is a member of the [**MF\_TOPONODE\_DRAIN\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) enumeration.</span></span> <span data-ttu-id="91c9a-110">如果未設定此屬性，則預設值為 [ **MF \_ TOPONODE \_ 清空 \_ 預設** 值]。</span><span class="sxs-lookup"><span data-stu-id="91c9a-110">If this attribute is not set, the default value is **MF\_TOPONODE\_DRAIN\_DEFAULT**.</span></span>

<span data-ttu-id="91c9a-111">在使用 [**MFT \_ 訊息 \_ 命令 \_ 清空**](mft-message-command-drain.md)訊息的轉換上呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) ，以進行清空。</span><span class="sxs-lookup"><span data-stu-id="91c9a-111">Draining is performed by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) on the transform with the [**MFT\_MESSAGE\_COMMAND\_DRAIN**](mft-message-command-drain.md) message.</span></span> <span data-ttu-id="91c9a-112">如需詳細資訊，請參閱 [**MFT \_ 訊息 \_ 類型**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) 列舉。</span><span class="sxs-lookup"><span data-stu-id="91c9a-112">For more information, see [**MFT\_MESSAGE\_TYPE**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) enumeration.</span></span>

<span data-ttu-id="91c9a-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="91c9a-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="91c9a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="91c9a-114">Requirements</span></span>



| <span data-ttu-id="91c9a-115">需求</span><span class="sxs-lookup"><span data-stu-id="91c9a-115">Requirement</span></span> | <span data-ttu-id="91c9a-116">值</span><span class="sxs-lookup"><span data-stu-id="91c9a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91c9a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91c9a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="91c9a-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91c9a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="91c9a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91c9a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="91c9a-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91c9a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="91c9a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="91c9a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="91c9a-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="91c9a-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91c9a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91c9a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c9a-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="91c9a-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="91c9a-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="91c9a-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="91c9a-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="91c9a-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="91c9a-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="91c9a-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="91c9a-128">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="91c9a-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




