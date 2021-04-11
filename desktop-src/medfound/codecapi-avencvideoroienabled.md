---
description: 指出是否 \_ 將接受在輸入範例上設定的 MFSampleExtension ROIRectangle 屬性。
ms.assetid: 6B3CB513-43E8-4D30-B5A0-CD2E9C9F46BA
title: 'CODECAPI_AVEncVideoROIEnabled 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345e6ba27a983be910f0dc0ea5d3db34191bdcb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317999"
---
# <a name="codecapi_avencvideoroienabled-property"></a><span data-ttu-id="a24aa-103">CODECAPI \_ AVEncVideoROIEnabled 屬性</span><span class="sxs-lookup"><span data-stu-id="a24aa-103">CODECAPI\_AVEncVideoROIEnabled property</span></span>

<span data-ttu-id="a24aa-104">指出是否將接受在輸入範例上設定的 [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="a24aa-104">Indicates whether [MFSampleExtension\_ROIRectangle](mfsampleextension-roirectangle.md) attribute set on the input sample will be honored or not.</span></span>

## <a name="data-type"></a><span data-ttu-id="a24aa-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a24aa-105">Data type</span></span>

<span data-ttu-id="a24aa-106">**ULONG** (VT \_ UI4) </span><span class="sxs-lookup"><span data-stu-id="a24aa-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a24aa-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="a24aa-107">Property GUID</span></span>

<span data-ttu-id="a24aa-108">**CODECAPI \_ AVEncVideoROIEnabled**</span><span class="sxs-lookup"><span data-stu-id="a24aa-108">**CODECAPI\_AVEncVideoROIEnabled**</span></span>

## <a name="remarks"></a><span data-ttu-id="a24aa-109">備註</span><span class="sxs-lookup"><span data-stu-id="a24aa-109">Remarks</span></span>

<span data-ttu-id="a24aa-110">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="a24aa-110">Default value is 0.</span></span>

<span data-ttu-id="a24aa-111">如果編碼器 MFT 接受非零值，則編碼器應該會接受在輸入範例上設定的 [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="a24aa-111">If an encoder MFT accepts a non-zero value, it is expected that the encoder will honor the [MFSampleExtension\_ROIRectangle](mfsampleextension-roirectangle.md) attribute set on the input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="a24aa-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a24aa-112">Requirements</span></span>



| <span data-ttu-id="a24aa-113">需求</span><span class="sxs-lookup"><span data-stu-id="a24aa-113">Requirement</span></span> | <span data-ttu-id="a24aa-114">值</span><span class="sxs-lookup"><span data-stu-id="a24aa-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a24aa-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a24aa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a24aa-116">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a24aa-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="a24aa-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a24aa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a24aa-118">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a24aa-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a24aa-119">標頭</span><span class="sxs-lookup"><span data-stu-id="a24aa-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a24aa-120"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a24aa-120"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a24aa-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a24aa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a24aa-122">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="a24aa-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




