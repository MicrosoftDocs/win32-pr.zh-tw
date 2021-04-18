---
description: 指定用戶端電腦上的說話者設定。
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: 'MFPKEY_WMADEC_SPKRCFG 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513040"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a><span data-ttu-id="546b4-103">MFPKEY \_ WMADEC \_ SPKRCFG 屬性</span><span class="sxs-lookup"><span data-stu-id="546b4-103">MFPKEY\_WMADEC\_SPKRCFG Property</span></span>

<span data-ttu-id="546b4-104">指定用戶端電腦上的說話者設定。</span><span class="sxs-lookup"><span data-stu-id="546b4-104">Specifies the speaker configuration on the client computer.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="546b4-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="546b4-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="546b4-106">g \_ wszWMACSpeakerConfig</span><span class="sxs-lookup"><span data-stu-id="546b4-106">g\_wszWMACSpeakerConfig</span></span>

## <a name="data-type"></a><span data-ttu-id="546b4-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="546b4-107">Data Type</span></span>

<span data-ttu-id="546b4-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="546b4-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="546b4-109">預設值</span><span class="sxs-lookup"><span data-stu-id="546b4-109">Default Value</span></span>

<span data-ttu-id="546b4-110">未採用任何特定的說話者設定。</span><span class="sxs-lookup"><span data-stu-id="546b4-110">No specific speaker configuration is assumed.</span></span>

## <a name="remarks"></a><span data-ttu-id="546b4-111">備註</span><span class="sxs-lookup"><span data-stu-id="546b4-111">Remarks</span></span>

<span data-ttu-id="546b4-112">您應該將此值設定為下表中的其中一個常數或值。</span><span class="sxs-lookup"><span data-stu-id="546b4-112">You should set this value to one of the constants or values in the following table.</span></span> <span data-ttu-id="546b4-113">這些常數定義于 Microsoft DirectSound 中，為了方便起見，在這裡列出。</span><span class="sxs-lookup"><span data-stu-id="546b4-113">The constants are defined in Microsoft DirectSound, and are listed here for convenience.</span></span> <span data-ttu-id="546b4-114">若要為您的編譯器解析這些常數名稱，您必須包含 dsound。</span><span class="sxs-lookup"><span data-stu-id="546b4-114">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="546b4-115">常數</span><span class="sxs-lookup"><span data-stu-id="546b4-115">Constant</span></span>             | <span data-ttu-id="546b4-116">值</span><span class="sxs-lookup"><span data-stu-id="546b4-116">Value</span></span>      | <span data-ttu-id="546b4-117">描述</span><span class="sxs-lookup"><span data-stu-id="546b4-117">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="546b4-118">DSSPEAKER \_ DIRECTOUT</span><span class="sxs-lookup"><span data-stu-id="546b4-118">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="546b4-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="546b4-119">0x00000000</span></span> | <span data-ttu-id="546b4-120">系統會直接傳遞音訊，而不是針對喇叭進行設定。</span><span class="sxs-lookup"><span data-stu-id="546b4-120">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="546b4-121">DSSPEAKER \_ 耳機</span><span class="sxs-lookup"><span data-stu-id="546b4-121">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="546b4-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="546b4-122">0x00000001</span></span> | <span data-ttu-id="546b4-123">用戶端電腦配備耳機。</span><span class="sxs-lookup"><span data-stu-id="546b4-123">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="546b4-124">DSSPEAKER \_ MONO</span><span class="sxs-lookup"><span data-stu-id="546b4-124">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="546b4-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="546b4-125">0x00000002</span></span> | <span data-ttu-id="546b4-126">用戶端電腦配備了 monoaural 喇叭。</span><span class="sxs-lookup"><span data-stu-id="546b4-126">The client computer is equipped with a monoaural speaker.</span></span>                    |
| <span data-ttu-id="546b4-127">DSSPEAKER \_ 四</span><span class="sxs-lookup"><span data-stu-id="546b4-127">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="546b4-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="546b4-128">0x00000003</span></span> | <span data-ttu-id="546b4-129">用戶端電腦配備了 quadraphonic 喇叭。</span><span class="sxs-lookup"><span data-stu-id="546b4-129">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="546b4-130">DSSPEAKER \_ 身歷聲</span><span class="sxs-lookup"><span data-stu-id="546b4-130">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="546b4-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="546b4-131">0x00000004</span></span> | <span data-ttu-id="546b4-132">用戶端電腦配備了身歷聲喇叭。</span><span class="sxs-lookup"><span data-stu-id="546b4-132">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="546b4-133">DSSPEAKER \_ 環繞</span><span class="sxs-lookup"><span data-stu-id="546b4-133">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="546b4-134">0x00000005</span><span class="sxs-lookup"><span data-stu-id="546b4-134">0x00000005</span></span> | <span data-ttu-id="546b4-135">用戶端電腦配備四個聲道的環繞音效喇叭。</span><span class="sxs-lookup"><span data-stu-id="546b4-135">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="546b4-136">DSSPEAKER \_ 5POINT1</span><span class="sxs-lookup"><span data-stu-id="546b4-136">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="546b4-137">0x00000006</span><span class="sxs-lookup"><span data-stu-id="546b4-137">0x00000006</span></span> | <span data-ttu-id="546b4-138">用戶端電腦配備了五個喇叭和一個喇叭。</span><span class="sxs-lookup"><span data-stu-id="546b4-138">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="546b4-139">DSSPEAKER \_ 7POINT1</span><span class="sxs-lookup"><span data-stu-id="546b4-139">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="546b4-140">0x00000007</span><span class="sxs-lookup"><span data-stu-id="546b4-140">0x00000007</span></span> | <span data-ttu-id="546b4-141">用戶端電腦配備了七個喇叭和一個喇叭。</span><span class="sxs-lookup"><span data-stu-id="546b4-141">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="546b4-142">針對此屬性所設定的值會決定由編解碼器音訊之編解碼器列舉的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="546b4-142">The value set for this property determines the output formats enumerated by the codec for multichannel audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="546b4-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="546b4-143">Requirements</span></span>



| <span data-ttu-id="546b4-144">需求</span><span class="sxs-lookup"><span data-stu-id="546b4-144">Requirement</span></span> | <span data-ttu-id="546b4-145">值</span><span class="sxs-lookup"><span data-stu-id="546b4-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="546b4-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="546b4-146">Minimum supported client</span></span><br/> | <span data-ttu-id="546b4-147">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="546b4-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="546b4-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="546b4-148">Minimum supported server</span></span><br/> | <span data-ttu-id="546b4-149">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="546b4-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="546b4-150">標頭</span><span class="sxs-lookup"><span data-stu-id="546b4-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="546b4-151"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="546b4-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="546b4-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="546b4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="546b4-153">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="546b4-153">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




