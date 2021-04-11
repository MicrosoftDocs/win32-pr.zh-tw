---
description: 指定編解碼器將用來偵測交錯式來源影片的邏輯。
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: 'MFPKEY_VTYPE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e95bab3120e60a2faa1a3be47c6459205f5f34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848452"
---
# <a name="mfpkey_vtype-property"></a><span data-ttu-id="b2619-103">MFPKEY \_ VTYPE 屬性</span><span class="sxs-lookup"><span data-stu-id="b2619-103">MFPKEY\_VTYPE Property</span></span>

<span data-ttu-id="b2619-104">指定編解碼器將用來偵測交錯式來源影片的邏輯。</span><span class="sxs-lookup"><span data-stu-id="b2619-104">Specifies the logic that the codec will use to detect interlaced source video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b2619-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="b2619-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b2619-106">g \_ wszWMVCVType</span><span class="sxs-lookup"><span data-stu-id="b2619-106">g\_wszWMVCVType</span></span>

## <a name="data-type"></a><span data-ttu-id="b2619-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="b2619-107">Data Type</span></span>

<span data-ttu-id="b2619-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b2619-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="b2619-109">預設值</span><span class="sxs-lookup"><span data-stu-id="b2619-109">Default Value</span></span>

<span data-ttu-id="b2619-110">0</span><span class="sxs-lookup"><span data-stu-id="b2619-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="b2619-111">備註</span><span class="sxs-lookup"><span data-stu-id="b2619-111">Remarks</span></span>

<span data-ttu-id="b2619-112">這個屬性可以設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b2619-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="b2619-113">值</span><span class="sxs-lookup"><span data-stu-id="b2619-113">Value</span></span> | <span data-ttu-id="b2619-114">描述</span><span class="sxs-lookup"><span data-stu-id="b2619-114">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2619-115">0</span><span class="sxs-lookup"><span data-stu-id="b2619-115">0</span></span>     | <span data-ttu-id="b2619-116">編解碼器將會使用標準的框架類型偵測邏輯。</span><span class="sxs-lookup"><span data-stu-id="b2619-116">The codec will use the standard frame-type detection logic.</span></span>                                                                                 |
| <span data-ttu-id="b2619-117">1</span><span class="sxs-lookup"><span data-stu-id="b2619-117">1</span></span>     | <span data-ttu-id="b2619-118">編解碼器會將所有來源影片框架視為交錯框架。</span><span class="sxs-lookup"><span data-stu-id="b2619-118">The codec will treat all source video frames as interlaced frames.</span></span>                                                                          |
| <span data-ttu-id="b2619-119">2</span><span class="sxs-lookup"><span data-stu-id="b2619-119">2</span></span>     | <span data-ttu-id="b2619-120">編解碼器會將所有來源影片框架視為交錯式影片的欄位。</span><span class="sxs-lookup"><span data-stu-id="b2619-120">The codec will treat all source video frames as fields of interlaced video.</span></span>                                                                 |
| <span data-ttu-id="b2619-121">3</span><span class="sxs-lookup"><span data-stu-id="b2619-121">3</span></span>     | <span data-ttu-id="b2619-122">編解碼器會自動判斷輸入的影片畫面是交錯的框架或交錯式影片的欄位。</span><span class="sxs-lookup"><span data-stu-id="b2619-122">The codec will automatically determine whether input video frames are interlaced frames or fields of interlaced video.</span></span>                      |
| <span data-ttu-id="b2619-123">4</span><span class="sxs-lookup"><span data-stu-id="b2619-123">4</span></span>     | <span data-ttu-id="b2619-124">編解碼器會自動判斷輸入的影片畫面是漸進式的框架、交錯的框架或交錯式影片的欄位。</span><span class="sxs-lookup"><span data-stu-id="b2619-124">The codec will automatically determine whether input video frames are progressive frames, interlaced frames, or fields of interlaced video.</span></span> |



 

<span data-ttu-id="b2619-125">這個屬性會決定漸進式或交錯式影片編碼所使用的圖片編碼方法。</span><span class="sxs-lookup"><span data-stu-id="b2619-125">This property determines the picture encoding method used for progressive or interlaced video encoding.</span></span>

<span data-ttu-id="b2619-126">如果未指定任何影片類型，編解碼器將會使用漸進式編碼會話的漸進式幀編碼，以及交錯編碼會話的欄位交錯編碼。</span><span class="sxs-lookup"><span data-stu-id="b2619-126">If no video type is specified, the codec will use progressive frame encoding for progressive encoding sessions, and field interlaced encoding for interlaced encoding sessions.</span></span> <span data-ttu-id="b2619-127">影片編碼會話的類型 (漸進式或交錯式) 是使用 [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) 屬性來設定。</span><span class="sxs-lookup"><span data-stu-id="b2619-127">The type of video encoding session (progressive or interlaced) is set by using the [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="b2619-128">[MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md)屬性必須設定為 VARIANT \_ TRUE，才能產生交錯輸出; 否則，設定 MPFKEY \_ VTYPE 屬性將沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="b2619-128">The [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property must be set to VARIANT\_TRUE in order to produce interlaced output; otherwise, setting the MPFKEY\_VTYPE property will have no effect.</span></span>

 

<span data-ttu-id="b2619-129">當交錯式影片經過編碼時，可以指定數個圖片編碼方法。</span><span class="sxs-lookup"><span data-stu-id="b2619-129">When interlaced video is being encoded, it is possible to specify several picture encoding methods.</span></span> <span data-ttu-id="b2619-130">編碼交錯式影片的最有效率方式通常是使用 (2) 的「欄位交錯」方法。</span><span class="sxs-lookup"><span data-stu-id="b2619-130">Typically the most efficient way to encode interlaced video is to use the field interlaced method (2).</span></span> <span data-ttu-id="b2619-131">如果來源影片包含很少的動作，框架交錯方法 (1) 或自動框架/欄位方法 (2) 可能更適合。</span><span class="sxs-lookup"><span data-stu-id="b2619-131">If the source video contains very little motion, the frame interlaced method (1) or the auto frame/field method (2) might be more suitable.</span></span>

<span data-ttu-id="b2619-132">編碼混合的內容 (同時包含漸進式和交錯的框架) 時，最好使用 value auto frame/field/累進方法 (4) 。</span><span class="sxs-lookup"><span data-stu-id="b2619-132">When encoding mixed content (containing both progressive and interlaced frames), it's best to use the value auto frame/field/progressive method (4).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2619-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2619-133">Requirements</span></span>



| <span data-ttu-id="b2619-134">需求</span><span class="sxs-lookup"><span data-stu-id="b2619-134">Requirement</span></span> | <span data-ttu-id="b2619-135">值</span><span class="sxs-lookup"><span data-stu-id="b2619-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2619-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2619-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b2619-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2619-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b2619-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2619-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b2619-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2619-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2619-140">標頭</span><span class="sxs-lookup"><span data-stu-id="b2619-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2619-141"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2619-141"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2619-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2619-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2619-143">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="b2619-143">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




