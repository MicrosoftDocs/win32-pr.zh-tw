---
description: LINECALLFEATURE2 \_ 常數列出可用於會議、傳輸和停車通話的補充功能。
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: 'LINECALLFEATURE2_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977e71f722fba34da6b2ecbd6a3e914c34a0aae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989597"
---
# <a name="linecallfeature2_-constants"></a>LINECALLFEATURE2 \_ 常數

**LINECALLFEATURE2 \_** 常數列出可用於會議、傳輸和停車通話的補充功能。

<dl> <dt>

<span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ COMPLCALLBACK**
</dt> <dd> <dl> <dt>



如果這個位是 on，則可以使用 LINECOMPLMODE 回呼選項搭配 LineCompleteCall 來叫用「回呼」功能 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) LINECALLFEATURE \_ COMPLETECALL 位也會在 **dwCallFeatures** 成員中開啟。


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ COMPLCAMPON**
</dt> <dd> <dl> <dt>



如果這個位開啟，可以使用 LINECOMPLMODE CAMPON 選項搭配 LineCompleteCall 來叫用「camp 開啟」功能 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) LINECALLFEATURE \_ COMPLETECALL 位也會在 **dwCallFeatures** 成員中開啟。


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ COMPLINTRUDE**
</dt> <dd> <dl> <dt>



如果這個位是 on，則可以使用 LINECOMPLMODE intrude 選項搭配 LineCompleteCall 來叫用 "intrude" 功能 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) LINECALLFEATURE \_ COMPLETECALL 位也會在 **dwCallFeatures** 成員中開啟。


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ COMPLMESSAGE**
</dt> <dd> <dl> <dt>



如果這個位是 on，則可以使用 LINECOMPLMODE message 選項搭配 LineCompleteCall 來叫用「離開訊息」功能 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) LINECALLFEATURE \_ COMPLETECALL 位也會在 **dwCallFeatures** 成員中開啟。


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ NOHOLDCONFERENCE**
</dt> <dd> <dl> <dt>



如果這個位是 on，則可以使用 LINECALLPARAMFLAGS NOHOLDCONFERENCE 選項搭配 LineSetupConference 來建立「無保留會議」 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) LINECALLFEATURE \_ SETUPCONF 位也會在 **dwCallFeatures** 成員中開啟。


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ ONESTEPTRANSFER**
</dt> <dd> <dl> <dt>



如果這個位是 on，則可以使用 LINECALLPARAMFLAGS ONESTEPTRANSFER 選項搭配 LineSetupTransfer 來建立「單一步驟轉移」 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer) LINECALLFEATURE \_ SETUPTRANSFER 位也會在 **dwCallFeatures** 成員中開啟。

> [!Note]  
> 如果 [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)中的 **dwCallFeatures2** 成員未指定任何 "COMPL" 位，但指定了 LINECALLFEATURE COMPLETECALL，則其中任何一項都 \_ 可以運作，但服務提供者尚未指定。

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ TRANSFERCONF**
</dt> <dd> <dl> <dt>



如果這個位開啟， [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) 函式就可以用來將傳輸解析為三向會議。 LINECALLFEATURE \_ COMPLETETRANSF 位也會在 **dwCallFeatures** 成員中開啟。


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ TRANSFERNORM**
</dt> <dd> <dl> <dt>



如果這個位是 on， [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) 函式可以用來將傳輸解析為一般傳輸。 LINECALLFEATURE \_ COMPLETETRANSF 位也會在 **dwCallFeatures** 成員中開啟。

> [!Note]  
> 如果 [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)中的 **dwCallFeatures2** 成員未指定 TRANSFERNORM 或 TRANSFERCONF，但指定了 LINECALLFEATURE \_ COMPLETETRANSF，則可能會有任何作用，但服務提供者尚未指定。

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ PARKDIRECT**
</dt> <dd> <dl> <dt>



如果這個位開啟，則可以使用 LINEPARKMODE 導向選項搭配 LinePark 來叫用「導向的公園」功能 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linepark) LINECALLFEATURE \_ 公園位也會在 **dwCallFeatures** 成員中開啟。


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 \_ PARKNONDIRECT**
</dt> <dd> <dl> <dt>



如果這個位開啟，則可以使用 LINEPARKMODE NONDIRECTED 選項搭配 LinePark 來叫用「非導向的公園」功能 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linepark) LINECALLFEATURE \_ 公園位也會在 **dwCallFeatures** 成員中開啟。

> [!Note]  
> 如果 [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)中的 **dwCallFeatures2** 成員未指定 PARKDIRECT 或 PARKNONDIRECT，但指定了 LINECALLFEATURE \_ 公園，則可能會有任何作用，但服務提供者尚未指定。

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




