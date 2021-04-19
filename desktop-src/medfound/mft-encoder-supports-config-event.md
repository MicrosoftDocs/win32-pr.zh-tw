---
description: 指定在串流處理時，MFT 編碼器支援接收 MEEncodingParameter 事件。
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: 'MFT_ENCODER_SUPPORTS_CONFIG_EVENT 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49c688abc4d372a463115c369e4616babe3bcaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976821"
---
# <a name="mft_encoder_supports_config_event-attribute"></a><span data-ttu-id="0a75e-103">MFT \_ 編碼器 \_ 支援 \_ CONFIG \_ 事件屬性</span><span class="sxs-lookup"><span data-stu-id="0a75e-103">MFT\_ENCODER\_SUPPORTS\_CONFIG\_EVENT attribute</span></span>

<span data-ttu-id="0a75e-104">指定在串流處理時，MFT 編碼器支援接收 [MEEncodingParameter](meencodingparameters.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="0a75e-104">Specifies that the MFT encoder supports receiving [MEEncodingParameter](meencodingparameters.md) events while streaming.</span></span>

## <a name="data-type"></a><span data-ttu-id="0a75e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="0a75e-105">Data type</span></span>

<span data-ttu-id="0a75e-106">**Bool** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="0a75e-106">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0a75e-107">備註</span><span class="sxs-lookup"><span data-stu-id="0a75e-107">Remarks</span></span>

<span data-ttu-id="0a75e-108">由 MFT 編碼器透過 IMFTransform 傳送 [**：:P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)。</span><span class="sxs-lookup"><span data-stu-id="0a75e-108">Sent by the MFT encoder through [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a75e-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a75e-109">Requirements</span></span>



| <span data-ttu-id="0a75e-110">需求</span><span class="sxs-lookup"><span data-stu-id="0a75e-110">Requirement</span></span> | <span data-ttu-id="0a75e-111">值</span><span class="sxs-lookup"><span data-stu-id="0a75e-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a75e-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a75e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0a75e-113">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a75e-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0a75e-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a75e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0a75e-115">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a75e-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="0a75e-116">標頭</span><span class="sxs-lookup"><span data-stu-id="0a75e-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a75e-117"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a75e-117"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a75e-118">Idl</span><span class="sxs-lookup"><span data-stu-id="0a75e-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0a75e-119"><dt>Mftransform .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0a75e-119"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a75e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a75e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a75e-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="0a75e-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0a75e-122">**IMFTransform：:P rocessEvent**</span><span class="sxs-lookup"><span data-stu-id="0a75e-122">**IMFTransform::ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




