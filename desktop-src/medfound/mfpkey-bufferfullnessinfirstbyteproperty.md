---
description: 指定編碼的影片位資料流程是否包含每個主要畫面格的緩衝區填滿值。
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: 'MFPKEY_BUFFERFULLNESSINFIRSTBYTE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001436"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a><span data-ttu-id="1536e-103">MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE 屬性</span><span class="sxs-lookup"><span data-stu-id="1536e-103">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE Property</span></span>

<span data-ttu-id="1536e-104">指定編碼的影片位資料流程是否包含每個主要畫面格的緩衝區填滿值。</span><span class="sxs-lookup"><span data-stu-id="1536e-104">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1536e-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="1536e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1536e-106">g \_ wszWMVCBufferFullnessInFirstByte</span><span class="sxs-lookup"><span data-stu-id="1536e-106">g\_wszWMVCBufferFullnessInFirstByte</span></span>

## <a name="data-type"></a><span data-ttu-id="1536e-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="1536e-107">Data Type</span></span>

<span data-ttu-id="1536e-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="1536e-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="1536e-109">備註</span><span class="sxs-lookup"><span data-stu-id="1536e-109">Remarks</span></span>

<span data-ttu-id="1536e-110">取得此值之前，您必須先設定輸出類型。</span><span class="sxs-lookup"><span data-stu-id="1536e-110">You must set an output type before getting this value.</span></span>

<span data-ttu-id="1536e-111">您可以使用 [IWMCodecProps：： GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop)取得這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1536e-111">You can get the value of this property using [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="1536e-112">如果您使用 **IPropertyBag**，您必須先使用 [MFPKEY \_ FOURCC](mfpkey-fourccproperty.md) 屬性來設定所需壓縮格式的 FOURCC 值。</span><span class="sxs-lookup"><span data-stu-id="1536e-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format with the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

<span data-ttu-id="1536e-113">在所有主要畫面格的第一個位元組中具有緩衝區飽和度，可讓您在串連壓縮的影片串流時，判斷所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="1536e-113">Having the buffer fullness in the first byte of all key frames enables you to determine the buffer size required when concatenating compressed video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="1536e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1536e-114">Requirements</span></span>



| <span data-ttu-id="1536e-115">需求</span><span class="sxs-lookup"><span data-stu-id="1536e-115">Requirement</span></span> | <span data-ttu-id="1536e-116">值</span><span class="sxs-lookup"><span data-stu-id="1536e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1536e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1536e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1536e-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1536e-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1536e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1536e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1536e-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1536e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1536e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1536e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1536e-122"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="1536e-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1536e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1536e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1536e-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="1536e-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




