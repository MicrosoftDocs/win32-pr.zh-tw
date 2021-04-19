---
description: 指定何時清除轉換。
ms.assetid: 1e87f58f-546f-4dd4-b218-1458ff17db53
title: 'MF_TOPONODE_FLUSH 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea241227d70d967f6f41ccd994176e9ddbbacbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980714"
---
# <a name="mf_toponode_flush-attribute"></a><span data-ttu-id="9bbd1-103">MF \_ TOPONODE \_ FLUSH 屬性</span><span class="sxs-lookup"><span data-stu-id="9bbd1-103">MF\_TOPONODE\_FLUSH attribute</span></span>

<span data-ttu-id="9bbd1-104">指定何時清除轉換。</span><span class="sxs-lookup"><span data-stu-id="9bbd1-104">Specifies when a transform is flushed.</span></span>

## <a name="data-type"></a><span data-ttu-id="9bbd1-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9bbd1-105">Data type</span></span>

<span data-ttu-id="9bbd1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9bbd1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9bbd1-107">備註</span><span class="sxs-lookup"><span data-stu-id="9bbd1-107">Remarks</span></span>

<span data-ttu-id="9bbd1-108">這個屬性會套用至 (**MF \_ 拓撲 \_ 轉換 \_ 節點**) 的轉換節點。</span><span class="sxs-lookup"><span data-stu-id="9bbd1-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="9bbd1-109">屬性的值是 [**MF \_ TOPONODE \_ FLUSH \_ 模式**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="9bbd1-109">The value of the attribute is a member of the [**MF\_TOPONODE\_FLUSH\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) enumeration.</span></span> <span data-ttu-id="9bbd1-110">如果未設定此屬性，則預設值為 **MF \_ TOPONODE \_ FLUSH \_ ALWAYS**。</span><span class="sxs-lookup"><span data-stu-id="9bbd1-110">If this attribute is not set, the default value is **MF\_TOPONODE\_FLUSH\_ALWAYS**.</span></span>

<span data-ttu-id="9bbd1-111">清除是藉由在轉換時呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) ，並 [**使用 \_ MFT \_ 訊息 \_ 命令**](mft-message-command-flush.md) 排清訊息來執行。</span><span class="sxs-lookup"><span data-stu-id="9bbd1-111">Flushing is performed by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) on the transform with the [**MFT\_MESSAGE\_COMMAND\_FLUSH**](mft-message-command-flush.md) message.</span></span> <span data-ttu-id="9bbd1-112">如需詳細資訊，請參閱 [**MFT \_ 訊息 \_ 類型**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) 列舉。</span><span class="sxs-lookup"><span data-stu-id="9bbd1-112">For more information, see [**MFT\_MESSAGE\_TYPE**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) enumeration.</span></span>

<span data-ttu-id="9bbd1-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="9bbd1-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bbd1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bbd1-114">Requirements</span></span>



| <span data-ttu-id="9bbd1-115">需求</span><span class="sxs-lookup"><span data-stu-id="9bbd1-115">Requirement</span></span> | <span data-ttu-id="9bbd1-116">值</span><span class="sxs-lookup"><span data-stu-id="9bbd1-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9bbd1-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9bbd1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9bbd1-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bbd1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9bbd1-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9bbd1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9bbd1-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bbd1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9bbd1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9bbd1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bbd1-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9bbd1-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bbd1-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bbd1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bbd1-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="9bbd1-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9bbd1-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9bbd1-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9bbd1-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9bbd1-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="9bbd1-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="9bbd1-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="9bbd1-128">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="9bbd1-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




