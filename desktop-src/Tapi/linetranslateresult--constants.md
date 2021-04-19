---
description: LINETRANSLATERESULT \_ 位旗標常數描述位址轉譯的各種結果。
ms.assetid: 7b834c57-d862-4fe6-828c-9e8fa20f3ec7
title: 'LINETRANSLATERESULT_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad10c3da2b4250ded5706e4aaa10b9b61f8739b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995097"
---
# <a name="linetranslateresult_-constants"></a><span data-ttu-id="3400a-103">LINETRANSLATERESULT \_ 常數</span><span class="sxs-lookup"><span data-stu-id="3400a-103">LINETRANSLATERESULT\_ Constants</span></span>

<span data-ttu-id="3400a-104">**LINETRANSLATERESULT \_** 位旗標常數描述位址轉譯的各種結果。</span><span class="sxs-lookup"><span data-stu-id="3400a-104">The **LINETRANSLATERESULT\_** bit-flag constants describe various results of an address translation.</span></span>

<dl> <dt>

<span data-ttu-id="3400a-105"><span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**LINETRANSLATERESULT \_ 標準**</span><span class="sxs-lookup"><span data-stu-id="3400a-105"><span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**LINETRANSLATERESULT\_CANONICAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3400a-106">指出輸入字串是有效的標準格式。</span><span class="sxs-lookup"><span data-stu-id="3400a-106">Indicates that the input string was in valid canonical format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3400a-107"><span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT \_ DIALBILLING**</span><span class="sxs-lookup"><span data-stu-id="3400a-107"><span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3400a-108">指出傳回的位址包含 "$"。</span><span class="sxs-lookup"><span data-stu-id="3400a-108">Indicates that the returned address contains a "$".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3400a-109"><span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT \_ DIALDIALTONE**</span><span class="sxs-lookup"><span data-stu-id="3400a-109"><span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3400a-110">指出傳回的位址包含 "W"。</span><span class="sxs-lookup"><span data-stu-id="3400a-110">Indicates that the returned address contains a "W".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3400a-111"><span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT \_ DIALPROMPT**</span><span class="sxs-lookup"><span data-stu-id="3400a-111"><span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT\_DIALPROMPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3400a-112">指出傳回的位址包含 "？"。</span><span class="sxs-lookup"><span data-stu-id="3400a-112">Indicates that the returned address contains a "?".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3400a-113"><span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT \_ DIALQUIET**</span><span class="sxs-lookup"><span data-stu-id="3400a-113"><span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3400a-114">指出傳回的位址包含 "@"。</span><span class="sxs-lookup"><span data-stu-id="3400a-114">Indicates that the returned address contain a "@".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3400a-115"><span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT \_ 國際**</span><span class="sxs-lookup"><span data-stu-id="3400a-115"><span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT\_INTERNATIONAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3400a-116">指出呼叫會被視為國際電話， (目的地位址中指定的國家或地區代碼，與針對 **CurrentLocation**) 指定的國家或地區碼不同。</span><span class="sxs-lookup"><span data-stu-id="3400a-116">Indicates that the call is being treated as an international call (country or region code specified in the destination address is different from the country or region code specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3400a-117"><span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT \_ INTOLLLIST**</span><span class="sxs-lookup"><span data-stu-id="3400a-117"><span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT\_INTOLLLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3400a-118">表示正在撥打近端電話，因為國家或地區有付費電話，且首碼出現在 **CurrentLocation** 的 **TollPrefixList** 中。</span><span class="sxs-lookup"><span data-stu-id="3400a-118">Indicates that the local call is being dialed as long distance because the country or region has toll calling and the prefix appears in the **TollPrefixList** of the **CurrentLocation**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3400a-119"><span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT \_ 本機**</span><span class="sxs-lookup"><span data-stu-id="3400a-119"><span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3400a-120">指出呼叫會被視為本機呼叫 (國家或地區代碼，以及目的地位址中指定的區碼，與針對 **CurrentLocation**) 指定的區域程式碼相同。</span><span class="sxs-lookup"><span data-stu-id="3400a-120">Indicates that the call is being treated as a local call (country or region code and area code specified in the destination address are the same as those specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3400a-121"><span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT \_ LONGDISTANCE**</span><span class="sxs-lookup"><span data-stu-id="3400a-121"><span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT\_LONGDISTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3400a-122">指出呼叫會被視為長途通話 (國家或地區代碼指定于目的地位址中，但區碼與針對 **CurrentLocation**) 指定的不同。</span><span class="sxs-lookup"><span data-stu-id="3400a-122">Indicates that the call is being treated as a long distance call (country or region code specified in the destination address is the same but area code is different from those specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3400a-123"><span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT \_ NOTINTOLLLIST**</span><span class="sxs-lookup"><span data-stu-id="3400a-123"><span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT\_NOTINTOLLLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3400a-124">指出國家或地區支援付費通話，但首碼未出現在 **TollPrefixList** 中，因此呼叫會以本機電話撥號。</span><span class="sxs-lookup"><span data-stu-id="3400a-124">Indicates that the country or region supports toll calling but the prefix does not appear in the **TollPrefixList**, so the call is dialed as a local call.</span></span> <span data-ttu-id="3400a-125">請注意，如果 INTOLLIST 和 NOTINTOLLIST 都是 off，則目前的國家或地區不支援收費前置詞，且與收費首碼相關的使用者介面元素不應呈現給使用者。如果其中一項是開啟的，則國家或地區支援收費清單，而且應該啟用相關的使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="3400a-125">Note that if both INTOLLIST and NOTINTOLLIST are off, the current country or region does not support toll prefixes, and user-interface elements related to toll prefixes should not be presented to the user; if either such bit is on, the country or region does support toll lists, and the related user-interface elements should be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3400a-126"><span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT \_ NOTRANSLATION**</span><span class="sxs-lookup"><span data-stu-id="3400a-126"><span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT\_NOTRANSLATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3400a-127">表示無法使用位址轉譯。</span><span class="sxs-lookup"><span data-stu-id="3400a-127">Indicates that address translation is not available.</span></span> <span data-ttu-id="3400a-128">這個元素只會公開給協調 TAPI 3.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3400a-128">This element is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3400a-129"><span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT \_ VOICEDETECT**</span><span class="sxs-lookup"><span data-stu-id="3400a-129"><span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT\_VOICEDETECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3400a-130">指出傳回的可撥出位址包含 "："。</span><span class="sxs-lookup"><span data-stu-id="3400a-130">Indicates that the returned dialable address contains a ":".</span></span> <span data-ttu-id="3400a-131">這個元素只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3400a-131">This element is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>

> [!Note]  
> <span data-ttu-id="3400a-132">"：" (冒號) 字元將會新增至可在可撥入的字串中內嵌並傳遞至目的地位址的字元清單。</span><span class="sxs-lookup"><span data-stu-id="3400a-132">The ":" (colon) character will be added to the list of characters that can be embedded in a dialable string and passed into destination addresses.</span></span> <span data-ttu-id="3400a-133">嘗試從應用程式傳遞至支援早于2.0 的 API 版本的線路裝置，很可能會導致 LINEERR \_ INVALADDRESS，或可能在完全忽略的字元中。</span><span class="sxs-lookup"><span data-stu-id="3400a-133">Attempting to pass it from an application to a line device that supports an API version earlier than 2.0 will most likely result in LINEERR\_INVALADDRESS, or possibly in the character being ignored entirely.</span></span> <span data-ttu-id="3400a-134">此字元的意義是「暫停直到偵測到語音提示，然後繼續撥號」;它可在自動撥入提供語音提示的系統時使用，例如長途電話卡處理器。</span><span class="sxs-lookup"><span data-stu-id="3400a-134">The meaning of this character is "Pause until a voice prompt is detected, then continue dialing"; it is intended for use when automatically dialing into systems that give voice prompts, such as long distance calling card processors.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3400a-135">備註</span><span class="sxs-lookup"><span data-stu-id="3400a-135">Remarks</span></span>

<span data-ttu-id="3400a-136">無延伸。</span><span class="sxs-lookup"><span data-stu-id="3400a-136">No extensibility.</span></span> <span data-ttu-id="3400a-137">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="3400a-137">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="3400a-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="3400a-138">Requirements</span></span>



| <span data-ttu-id="3400a-139">需求</span><span class="sxs-lookup"><span data-stu-id="3400a-139">Requirement</span></span> | <span data-ttu-id="3400a-140">值</span><span class="sxs-lookup"><span data-stu-id="3400a-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3400a-141">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="3400a-141">TAPI version</span></span><br/> | <span data-ttu-id="3400a-142">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3400a-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3400a-143">標頭</span><span class="sxs-lookup"><span data-stu-id="3400a-143">Header</span></span><br/>       | <dl> <span data-ttu-id="3400a-144"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="3400a-144"><dt>Tapi.h</dt></span></span> </dl> |



 

 




