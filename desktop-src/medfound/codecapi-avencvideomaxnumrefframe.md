---
description: 指定編碼器所支援的最大參考框架。
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: 'CODECAPI_AVEncVideoMaxNumRefFrame 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8f5a7794410012bd1a025e794e1fd23f4b332
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116045"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a><span data-ttu-id="5531d-103">CODECAPI \_ AVEncVideoMaxNumRefFrame 屬性</span><span class="sxs-lookup"><span data-stu-id="5531d-103">CODECAPI\_AVEncVideoMaxNumRefFrame property</span></span>

<span data-ttu-id="5531d-104">指定編碼器所支援的最大參考框架。</span><span class="sxs-lookup"><span data-stu-id="5531d-104">Specifies the maximum reference frames supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="5531d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="5531d-105">Data type</span></span>

<span data-ttu-id="5531d-106">**ULONG** (VT \_ UI4) </span><span class="sxs-lookup"><span data-stu-id="5531d-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5531d-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="5531d-107">Property GUID</span></span>

<span data-ttu-id="5531d-108">**CODECAPI \_ AVEncVideoMaxNumRefFrame**</span><span class="sxs-lookup"><span data-stu-id="5531d-108">**CODECAPI\_AVEncVideoMaxNumRefFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="5531d-109">備註</span><span class="sxs-lookup"><span data-stu-id="5531d-109">Remarks</span></span>

<span data-ttu-id="5531d-110">針對 h.264，這會對應至 h.264 規格中定義的 Sequence 參數 Set variable **max \_ num \_ ref \_ 框架** 。</span><span class="sxs-lookup"><span data-stu-id="5531d-110">For H.264, this maps to the Sequence Parameter Set variable **max\_num\_ref\_frames** as defined in H.264 specification.</span></span>

<span data-ttu-id="5531d-111">**H.264/AVC 編碼器：**</span><span class="sxs-lookup"><span data-stu-id="5531d-111">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="5531d-112">編碼器可能會使用較少的參考框架，以遵守位流中指定的層級。</span><span class="sxs-lookup"><span data-stu-id="5531d-112">Encoders may use fewer reference frames in order to obey the level specified in the bitstream.</span></span>

<span data-ttu-id="5531d-113">編碼器應支援 [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)、 [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)和 [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="5531d-113">Encoders shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="5531d-114">這是靜態屬性，表示只能在編碼會話開始之前設定。</span><span class="sxs-lookup"><span data-stu-id="5531d-114">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="5531d-115">建議的預設值為2。</span><span class="sxs-lookup"><span data-stu-id="5531d-115">Recommended default value is 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="5531d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5531d-116">Requirements</span></span>



| <span data-ttu-id="5531d-117">需求</span><span class="sxs-lookup"><span data-stu-id="5531d-117">Requirement</span></span> | <span data-ttu-id="5531d-118">值</span><span class="sxs-lookup"><span data-stu-id="5531d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5531d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5531d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5531d-120">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5531d-120">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="5531d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5531d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5531d-122">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5531d-122">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5531d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5531d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5531d-124"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="5531d-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5531d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5531d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5531d-126">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="5531d-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

