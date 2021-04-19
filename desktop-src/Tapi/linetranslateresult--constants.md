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
# <a name="linetranslateresult_-constants"></a>LINETRANSLATERESULT \_ 常數

**LINETRANSLATERESULT \_** 位旗標常數描述位址轉譯的各種結果。

<dl> <dt>

<span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**LINETRANSLATERESULT \_ 標準**
</dt> <dd> <dl> <dt>



指出輸入字串是有效的標準格式。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT \_ DIALBILLING**
</dt> <dd> <dl> <dt>



指出傳回的位址包含 "$"。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>



指出傳回的位址包含 "W"。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT \_ DIALPROMPT**
</dt> <dd> <dl> <dt>



指出傳回的位址包含 "？"。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT \_ DIALQUIET**
</dt> <dd> <dl> <dt>



指出傳回的位址包含 "@"。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT \_ 國際**
</dt> <dd> <dl> <dt>



指出呼叫會被視為國際電話， (目的地位址中指定的國家或地區代碼，與針對 **CurrentLocation**) 指定的國家或地區碼不同。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT \_ INTOLLLIST**
</dt> <dd> <dl> <dt>



表示正在撥打近端電話，因為國家或地區有付費電話，且首碼出現在 **CurrentLocation** 的 **TollPrefixList** 中。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT \_ 本機**
</dt> <dd> <dl> <dt>



指出呼叫會被視為本機呼叫 (國家或地區代碼，以及目的地位址中指定的區碼，與針對 **CurrentLocation**) 指定的區域程式碼相同。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT \_ LONGDISTANCE**
</dt> <dd> <dl> <dt>



指出呼叫會被視為長途通話 (國家或地區代碼指定于目的地位址中，但區碼與針對 **CurrentLocation**) 指定的不同。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT \_ NOTINTOLLLIST**
</dt> <dd> <dl> <dt>



指出國家或地區支援付費通話，但首碼未出現在 **TollPrefixList** 中，因此呼叫會以本機電話撥號。 請注意，如果 INTOLLIST 和 NOTINTOLLIST 都是 off，則目前的國家或地區不支援收費前置詞，且與收費首碼相關的使用者介面元素不應呈現給使用者。如果其中一項是開啟的，則國家或地區支援收費清單，而且應該啟用相關的使用者介面元素。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT \_ NOTRANSLATION**
</dt> <dd> <dl> <dt>



表示無法使用位址轉譯。 這個元素只會公開給協調 TAPI 3.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT \_ VOICEDETECT**
</dt> <dd> <dl> <dt>



指出傳回的可撥出位址包含 "："。 這個元素只會公開給協調 TAPI 2.0 版或更新版本的應用程式。

> [!Note]  
> "：" (冒號) 字元將會新增至可在可撥入的字串中內嵌並傳遞至目的地位址的字元清單。 嘗試從應用程式傳遞至支援早于2.0 的 API 版本的線路裝置，很可能會導致 LINEERR \_ INVALADDRESS，或可能在完全忽略的字元中。 此字元的意義是「暫停直到偵測到語音提示，然後繼續撥號」;它可在自動撥入提供語音提示的系統時使用，例如長途電話卡處理器。

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




