---
description: 指定音訊解碼器將使用的動態範圍控制模式。
ms.assetid: 0dbe0c40-39ac-4c1b-9da2-9b142b5bb0eb
title: 'MFPKEY_WMADEC_DRCMODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb612e08ff8bd799ec94faae68763f04db8ad052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191789"
---
# <a name="mfpkey_wmadec_drcmode-property"></a><span data-ttu-id="bd070-103">MFPKEY \_ WMADEC \_ DRCMODE 屬性</span><span class="sxs-lookup"><span data-stu-id="bd070-103">MFPKEY\_WMADEC\_DRCMODE Property</span></span>

<span data-ttu-id="bd070-104">指定音訊解碼器將使用的動態範圍控制模式。</span><span class="sxs-lookup"><span data-stu-id="bd070-104">Specifies the dynamic range control mode that the audio decoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="bd070-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="bd070-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="bd070-106">g \_ wszWMACDRCSetting</span><span class="sxs-lookup"><span data-stu-id="bd070-106">g\_wszWMACDRCSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="bd070-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="bd070-107">Data Type</span></span>

<span data-ttu-id="bd070-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="bd070-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="bd070-109">預設值</span><span class="sxs-lookup"><span data-stu-id="bd070-109">Default Value</span></span>

<span data-ttu-id="bd070-110">0</span><span class="sxs-lookup"><span data-stu-id="bd070-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="bd070-111">備註</span><span class="sxs-lookup"><span data-stu-id="bd070-111">Remarks</span></span>

<span data-ttu-id="bd070-112">這個整數值的範圍是從0到2。</span><span class="sxs-lookup"><span data-stu-id="bd070-112">This integer value ranges from 0 to 2.</span></span> <span data-ttu-id="bd070-113">值愈大，未壓縮音訊輸出的動態範圍就越小。</span><span class="sxs-lookup"><span data-stu-id="bd070-113">The greater the value, the smaller the dynamic range of the uncompressed audio output.</span></span> <span data-ttu-id="bd070-114">0值表示編解碼器不執行任何動態範圍控制，也就是說，編解碼器不會改變編碼內容的固有動態範圍。</span><span class="sxs-lookup"><span data-stu-id="bd070-114">A value of 0 signals the codec to perform no dynamic range control, that is, the codec will not alter the inherent dynamic range of the encoded content.</span></span>

<span data-ttu-id="bd070-115">如果此值設為1或2，則編解碼器會使用下列屬性來判斷所需的動態範圍控制項：</span><span class="sxs-lookup"><span data-stu-id="bd070-115">If this value is set to 1 or 2, the codec will use the following properties to determine the needed dynamic range control:</span></span>

-   [<span data-ttu-id="bd070-116">MFPKEY \_ WMADRC \_ AVGREF</span><span class="sxs-lookup"><span data-stu-id="bd070-116">MFPKEY\_WMADRC\_AVGREF</span></span>](mfpkey-wmadrc-avgrefproperty.md)
-   [<span data-ttu-id="bd070-117">MFPKEY \_ WMADRC \_ PEAKREF</span><span class="sxs-lookup"><span data-stu-id="bd070-117">MFPKEY\_WMADRC\_PEAKREF</span></span>](mfpkey-wmadrc-peakrefproperty.md)
-   [<span data-ttu-id="bd070-118">MFPKEY \_ WMADRC \_ AVGTARGET</span><span class="sxs-lookup"><span data-stu-id="bd070-118">MFPKEY\_WMADRC\_AVGTARGET</span></span>](mfpkey-wmadrc-avgtargetproperty.md)
-   [<span data-ttu-id="bd070-119">MFPKEY \_ WMADRC \_ PEAKTARGET</span><span class="sxs-lookup"><span data-stu-id="bd070-119">MFPKEY\_WMADRC\_PEAKTARGET</span></span>](mfpkey-wmadrc-peaktargetproperty.md)

<span data-ttu-id="bd070-120">如果您未提供目標值，編解碼器將會提供它自己的值。</span><span class="sxs-lookup"><span data-stu-id="bd070-120">If you do not provide target values, the codec will provide its own.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd070-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd070-121">Requirements</span></span>



| <span data-ttu-id="bd070-122">需求</span><span class="sxs-lookup"><span data-stu-id="bd070-122">Requirement</span></span> | <span data-ttu-id="bd070-123">值</span><span class="sxs-lookup"><span data-stu-id="bd070-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd070-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd070-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bd070-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd070-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bd070-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd070-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bd070-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd070-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd070-128">標頭</span><span class="sxs-lookup"><span data-stu-id="bd070-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd070-129"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="bd070-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd070-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd070-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd070-131">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="bd070-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




