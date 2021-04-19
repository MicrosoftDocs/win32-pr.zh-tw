---
description: 從語音捕捉 DSP (AEC) ，抓取聲場回應取消的品質計量。
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: 'MFPKEY_WMAAECMA_QUALITY_METRICS 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3740630bc23c4e3e0e824e55b4e34bcd8b1347f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977807"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a><span data-ttu-id="3b3b6-103">MFPKEY \_ WMAAECMA \_ 品質 \_ 計量屬性</span><span class="sxs-lookup"><span data-stu-id="3b3b6-103">MFPKEY\_WMAAECMA\_QUALITY\_METRICS Property</span></span>

<span data-ttu-id="3b3b6-104">從語音捕捉 DSP (AEC) ，抓取聲場回應取消的品質計量。</span><span class="sxs-lookup"><span data-stu-id="3b3b6-104">Retrieves quality metrics on acoustic echo cancellation (AEC) from the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3b3b6-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="3b3b6-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3b3b6-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="3b3b6-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="3b3b6-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="3b3b6-107">Data Type</span></span>

<span data-ttu-id="3b3b6-108">VT \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="3b3b6-108">VT\_BLOB</span></span>

## <a name="remarks"></a><span data-ttu-id="3b3b6-109">備註</span><span class="sxs-lookup"><span data-stu-id="3b3b6-109">Remarks</span></span>

<span data-ttu-id="3b3b6-110">這個屬性的值是 [AecQualityMetrics \_ 結構](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) 結構。</span><span class="sxs-lookup"><span data-stu-id="3b3b6-110">The value of this property is an [AecQualityMetrics\_Struct](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) structure.</span></span> <span data-ttu-id="3b3b6-111">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="3b3b6-111">This property is read-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b3b6-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b3b6-112">Requirements</span></span>



| <span data-ttu-id="3b3b6-113">需求</span><span class="sxs-lookup"><span data-stu-id="3b3b6-113">Requirement</span></span> | <span data-ttu-id="3b3b6-114">值</span><span class="sxs-lookup"><span data-stu-id="3b3b6-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b3b6-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b3b6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3b3b6-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b3b6-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3b3b6-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b3b6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3b3b6-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b3b6-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3b3b6-119">標頭</span><span class="sxs-lookup"><span data-stu-id="3b3b6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b3b6-120"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b3b6-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b3b6-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b3b6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b3b6-122">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="3b3b6-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="3b3b6-123">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="3b3b6-123">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
