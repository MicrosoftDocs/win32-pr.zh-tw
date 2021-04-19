---
description: LINEDEVCAPFLAGS \_ 位旗標常數是布林值的集合，其描述各種線路裝置功能。
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: 'LINEDEVCAPFLAGS_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffefca75c00fdf09b1886affbff7f0ea90bab6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995482"
---
# <a name="linedevcapflags_-constants"></a><span data-ttu-id="fed63-103">LINEDEVCAPFLAGS \_ 常數</span><span class="sxs-lookup"><span data-stu-id="fed63-103">LINEDEVCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="fed63-104">**LINEDEVCAPFLAGS \_** 位旗標常數是布林值的集合，其描述各種線路裝置功能。</span><span class="sxs-lookup"><span data-stu-id="fed63-104">The **LINEDEVCAPFLAGS\_** bit-flag constants are a collection of Booleans describing various line device capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="fed63-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS \_ CALLHUB**</span><span class="sxs-lookup"><span data-stu-id="fed63-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS\_CALLHUB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fed63-106">指出這一行是否支援呼叫中樞。</span><span class="sxs-lookup"><span data-stu-id="fed63-106">Indicates whether call hubs are supported on this line.</span></span> <span data-ttu-id="fed63-107">此旗標只會公開給協調 TAPI 3.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fed63-107">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fed63-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS \_ CALLHUBTRACKING**</span><span class="sxs-lookup"><span data-stu-id="fed63-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fed63-109">指出這一行是否支援呼叫中樞追蹤。</span><span class="sxs-lookup"><span data-stu-id="fed63-109">Indicates whether call hub tracking is supported on this line.</span></span> <span data-ttu-id="fed63-110">此旗標只會公開給協調 TAPI 3.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fed63-110">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fed63-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS \_ CLOSEDROP**</span><span class="sxs-lookup"><span data-stu-id="fed63-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS\_CLOSEDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fed63-112">指定當應用程式在行上有使用中的時，當開啟的行關閉時，會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="fed63-112">Specifies what happens when an open line is closed while the application has calls active on the line.</span></span> <span data-ttu-id="fed63-113">若 **為 TRUE**，則服務提供者會卸載 (清除) 當最後一個開啟該行的應用程式以 [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)關閉該行時，該行上所有使用中的呼叫。</span><span class="sxs-lookup"><span data-stu-id="fed63-113">If **TRUE**, the service provider drops (clears) all active calls on the line when the last application that has opened the line closes it with [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose).</span></span> <span data-ttu-id="fed63-114">如果 **為 FALSE**，則服務提供者不會在這種情況下捨棄使用中的呼叫。</span><span class="sxs-lookup"><span data-stu-id="fed63-114">If **FALSE**, the service provider does not drop active calls in such cases.</span></span> <span data-ttu-id="fed63-115">相反地，呼叫會保持作用中狀態，並受外部裝置控制。</span><span class="sxs-lookup"><span data-stu-id="fed63-115">Instead, the calls remain active and under control of external devices.</span></span> <span data-ttu-id="fed63-116">如果有其他裝置可讓通話保持運作，則服務提供者通常會將此位設定為 **FALSE** ，例如，如果類比線路路的電腦和電話組都是在合作物件設定中直接連接到它們，則即使在電腦關機之後，offhook 電話也會自動讓通話保持使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="fed63-116">A service provider typically sets this bit to **FALSE** if there is some other device that can keep the call alive, for example, if an analog line has the computer and phone set both connect directly to them in a party-line configuration, the offhook phone will automatically keep the call active even after the computer powers down.</span></span>

<span data-ttu-id="fed63-117">應用程式應該檢查此旗標，以判斷是否要使用 [確定]/[取消] 對話方塊來警告使用者 (，) 使用中的呼叫將會遺失。</span><span class="sxs-lookup"><span data-stu-id="fed63-117">Applications should check this flag to determine whether to warn the user (with an OK/Cancel dialog box) that active calls will be lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fed63-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS \_ CROSSADDRCONF**</span><span class="sxs-lookup"><span data-stu-id="fed63-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS\_CROSSADDRCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fed63-119">指定是否可以 conferenced 此行上不同位址的呼叫。</span><span class="sxs-lookup"><span data-stu-id="fed63-119">Specifies whether calls on different addresses on this line can be conferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fed63-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS \_ DIALBILLING**</span><span class="sxs-lookup"><span data-stu-id="fed63-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fed63-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS \_ DIALDIALTONE**</span><span class="sxs-lookup"><span data-stu-id="fed63-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fed63-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS \_ DIALQUIET**</span><span class="sxs-lookup"><span data-stu-id="fed63-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fed63-123">這些旗標會指出指定的線路裝置是否支援 "$"、"@" 或 "W" 可撥出字串修飾詞。</span><span class="sxs-lookup"><span data-stu-id="fed63-123">These flags indicate whether the "$", "@", or "W" dialable string modifier is supported for a given line device.</span></span> <span data-ttu-id="fed63-124">如果支援修飾詞則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fed63-124">It is **TRUE** if the modifier is supported; otherwise, **FALSE**.</span></span> <span data-ttu-id="fed63-125">線路裝置永遠不支援 "？" (提示使用者繼續撥號) 。</span><span class="sxs-lookup"><span data-stu-id="fed63-125">The "?" (prompt user to continue dialing) is never supported by a line device.</span></span> <span data-ttu-id="fed63-126">這些旗標可讓應用程式事先判斷哪些修飾詞會導致產生 LINEERR。</span><span class="sxs-lookup"><span data-stu-id="fed63-126">These flags allow an application to determine up front which modifiers would result in the generation of a LINEERR.</span></span> <span data-ttu-id="fed63-127">應用程式可選擇預先掃描的可辨識字串是否有不支援的字元，或將「原始」字串從 [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) 直接傳遞給提供者，做為 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) 或 [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) 等函式的一部分，並讓函式產生錯誤，以告訴它不支援的修飾詞在字串中第一次發生。</span><span class="sxs-lookup"><span data-stu-id="fed63-127">The application has the choice of pre-scanning dialable strings for unsupported characters or of passing the "raw" string from [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) directly to the provider as part of functions such as [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) or [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) and let the function generate an error to tell it which unsupported modifier occurs first in the string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fed63-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS \_ HIGHLEVCOMP**</span><span class="sxs-lookup"><span data-stu-id="fed63-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS\_HIGHLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fed63-129">指定這一行是否支援高層級的相容性資訊元素。</span><span class="sxs-lookup"><span data-stu-id="fed63-129">Specifies whether high-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fed63-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS \_ LOWLEVCOMP**</span><span class="sxs-lookup"><span data-stu-id="fed63-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS\_LOWLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fed63-131">指定這一行是否支援低層級的相容性資訊元素。</span><span class="sxs-lookup"><span data-stu-id="fed63-131">Specifies whether low-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fed63-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS \_ MEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="fed63-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS\_MEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fed63-133">指定是否可在這一行呼叫媒體控制項作業。</span><span class="sxs-lookup"><span data-stu-id="fed63-133">Specifies whether media-control operations are available for calls at this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fed63-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS \_ MSP**</span><span class="sxs-lookup"><span data-stu-id="fed63-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS\_MSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fed63-135">指出媒體服務提供者 (MSP) 是否與該行相關聯。</span><span class="sxs-lookup"><span data-stu-id="fed63-135">Indicates whether a Media Service Provider (MSP) is associated with the line.</span></span> <span data-ttu-id="fed63-136">此旗標只會公開給協調 TAPI 3.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fed63-136">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fed63-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS \_ MULTIPLEADDR**</span><span class="sxs-lookup"><span data-stu-id="fed63-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS\_MULTIPLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fed63-138">指定 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)、 [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)、 [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)或 [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) 是否能夠一次處理多個位址 (與反向多工) 。</span><span class="sxs-lookup"><span data-stu-id="fed63-138">Specifies whether [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI\_lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), or [**TSPI\_lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) is able to deal with multiple addresses at once (as for inverse multiplexing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fed63-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS \_ PRI加值稅EOBJECTS**</span><span class="sxs-lookup"><span data-stu-id="fed63-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS\_PRIVATEOBJECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fed63-140">指出是否已執行 [提供者特定的介面](./provider-specific-interfaces.md) 。</span><span class="sxs-lookup"><span data-stu-id="fed63-140">Indicates whether [provider-specific Interfaces](./provider-specific-interfaces.md) have been implemented.</span></span> <span data-ttu-id="fed63-141">此旗標只會公開給協調 TAPI 3.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fed63-141">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fed63-142">備註</span><span class="sxs-lookup"><span data-stu-id="fed63-142">Remarks</span></span>

<span data-ttu-id="fed63-143">無延伸。</span><span class="sxs-lookup"><span data-stu-id="fed63-143">No extensibility.</span></span> <span data-ttu-id="fed63-144">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="fed63-144">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="fed63-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="fed63-145">Requirements</span></span>



| <span data-ttu-id="fed63-146">需求</span><span class="sxs-lookup"><span data-stu-id="fed63-146">Requirement</span></span> | <span data-ttu-id="fed63-147">值</span><span class="sxs-lookup"><span data-stu-id="fed63-147">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fed63-148">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="fed63-148">TAPI version</span></span><br/> | <span data-ttu-id="fed63-149">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="fed63-149">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fed63-150">標頭</span><span class="sxs-lookup"><span data-stu-id="fed63-150">Header</span></span><br/>       | <dl> <span data-ttu-id="fed63-151"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="fed63-151"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fed63-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fed63-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed63-153">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="fed63-153">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="fed63-154">**lineDial**</span><span class="sxs-lookup"><span data-stu-id="fed63-154">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="fed63-155">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="fed63-155">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="fed63-156">**lineTranslateAddress**</span><span class="sxs-lookup"><span data-stu-id="fed63-156">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

