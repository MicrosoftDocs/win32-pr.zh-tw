---
description: 指定通道矩陣，用來將來源通道轉換成目的通道 (例如，將5.1 轉換成身歷聲) 。
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: 'MFPKEY_WMRESAMP_CHANNELMTX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e39f9a9344dd080362859592fcf1f71657ee8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979078"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a><span data-ttu-id="b503f-103">MFPKEY \_ WMRESAMP \_ CHANNELMTX 屬性</span><span class="sxs-lookup"><span data-stu-id="b503f-103">MFPKEY\_WMRESAMP\_CHANNELMTX Property</span></span>

<span data-ttu-id="b503f-104">指定通道矩陣，用來將來源通道轉換成目的通道 (例如，將5.1 轉換成身歷聲) 。</span><span class="sxs-lookup"><span data-stu-id="b503f-104">Specifies the channel matrix, which is used to convert the source channels into the destination channels (for example, to convert 5.1 to stereo).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b503f-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="b503f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b503f-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="b503f-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="b503f-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="b503f-107">Data Type</span></span>

<span data-ttu-id="b503f-108">VT \_ I4 \| vt \_ 陣列</span><span class="sxs-lookup"><span data-stu-id="b503f-108">VT\_I4 \| VT\_ARRAY</span></span>

## <a name="applies-to"></a><span data-ttu-id="b503f-109">套用至</span><span class="sxs-lookup"><span data-stu-id="b503f-109">Applies To</span></span>

-   [<span data-ttu-id="b503f-110">音訊 Resampler DSP</span><span class="sxs-lookup"><span data-stu-id="b503f-110">Audio Resampler DSP</span></span>](audioresampler.md)

## <a name="remarks"></a><span data-ttu-id="b503f-111">備註</span><span class="sxs-lookup"><span data-stu-id="b503f-111">Remarks</span></span>

<span data-ttu-id="b503f-112">屬性的值是 Ns x Nd 係數的矩陣，其中 Ns 是來源通道的數目，Nd 是目的地通道的數目。</span><span class="sxs-lookup"><span data-stu-id="b503f-112">The value of the property is a matrix of Ns x Nd coefficients, where Ns is the number of source channels and Nd is the number of destination channels.</span></span> <span data-ttu-id="b503f-113">係數會以分貝指定，使用下列公式：</span><span class="sxs-lookup"><span data-stu-id="b503f-113">Coefficients are specified in decibels using the following formula:</span></span>

<span data-ttu-id="b503f-114"> (int)  (65536 \* 20 \* Log10 (dB) ) </span><span class="sxs-lookup"><span data-stu-id="b503f-114">(int)(65536\*20\*log10(dB))</span></span>

<span data-ttu-id="b503f-115">矩陣會以資料列主要順序的形式儲存，其中的資料列編號是來源通道，而資料行編號則是目的地通道。</span><span class="sxs-lookup"><span data-stu-id="b503f-115">The matrix is stored as an array in row-major order where the row number is the source channel and the column number is the destination channel.</span></span>

<span data-ttu-id="b503f-116">因此，如果矩陣如下所示：</span><span class="sxs-lookup"><span data-stu-id="b503f-116">Thus, if the matrix is the following:</span></span>

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

<span data-ttu-id="b503f-117">然後，您會將陣列指定為：</span><span class="sxs-lookup"><span data-stu-id="b503f-117">then you would specify the array as:</span></span>

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

## <a name="requirements"></a><span data-ttu-id="b503f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b503f-118">Requirements</span></span>



| <span data-ttu-id="b503f-119">需求</span><span class="sxs-lookup"><span data-stu-id="b503f-119">Requirement</span></span> | <span data-ttu-id="b503f-120">值</span><span class="sxs-lookup"><span data-stu-id="b503f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b503f-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b503f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b503f-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b503f-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b503f-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b503f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b503f-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b503f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b503f-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b503f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b503f-126"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b503f-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b503f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b503f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b503f-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="b503f-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
