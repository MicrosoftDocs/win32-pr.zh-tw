---
description: 指定編碼器所支援的最大傳遞數目。
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: 'MFPKEY_PASSESRECOMMENDED 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e0a0d254c09965976e5659bacfacf3be06643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192249"
---
# <a name="mfpkey_passesrecommended-property"></a><span data-ttu-id="d55f1-103">MFPKEY \_ PASSESRECOMMENDED 屬性</span><span class="sxs-lookup"><span data-stu-id="d55f1-103">MFPKEY\_PASSESRECOMMENDED Property</span></span>

<span data-ttu-id="d55f1-104">指定編碼器所支援的最大傳遞數目。</span><span class="sxs-lookup"><span data-stu-id="d55f1-104">Specifies the maximum number of passes supported by the encoder.</span></span> <span data-ttu-id="d55f1-105">唯讀。</span><span class="sxs-lookup"><span data-stu-id="d55f1-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d55f1-106">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="d55f1-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="d55f1-107">g \_ wszWMVCPassesRecommended、g \_ wszWMCPMaxPasses</span><span class="sxs-lookup"><span data-stu-id="d55f1-107">g\_wszWMVCPassesRecommended, g\_wszWMCPMaxPasses</span></span>

## <a name="data-type"></a><span data-ttu-id="d55f1-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="d55f1-108">Data Type</span></span>

<span data-ttu-id="d55f1-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="d55f1-109">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="d55f1-110">備註</span><span class="sxs-lookup"><span data-stu-id="d55f1-110">Remarks</span></span>

<span data-ttu-id="d55f1-111">您可以取得這個屬性的值，呼叫 [IWMCodecProps：： GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop)。</span><span class="sxs-lookup"><span data-stu-id="d55f1-111">You can get the value of this property calling [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="d55f1-112">如果您使用 **IPropertyBag**，您必須先使用 [MFPKEY \_ FOURCC](mfpkey-fourccproperty.md) 屬性來設定所需壓縮格式的 FOURCC 值。</span><span class="sxs-lookup"><span data-stu-id="d55f1-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format by using the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d55f1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d55f1-113">Requirements</span></span>



| <span data-ttu-id="d55f1-114">需求</span><span class="sxs-lookup"><span data-stu-id="d55f1-114">Requirement</span></span> | <span data-ttu-id="d55f1-115">值</span><span class="sxs-lookup"><span data-stu-id="d55f1-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d55f1-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d55f1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d55f1-117">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d55f1-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d55f1-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d55f1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d55f1-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d55f1-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d55f1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d55f1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d55f1-121"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d55f1-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d55f1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d55f1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55f1-123">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="d55f1-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




