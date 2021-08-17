---
description: LINEMEDIAMODE \_ 常數描述通訊會話或呼叫)  (或模式的媒體類型。
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: 'LINEMEDIAMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c11e40a81fffc967afd534ce6de591b524d835cbe97a919903bd97b1eeb4daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140011"
---
# <a name="linemediamode_-constants"></a>LINEMEDIAMODE \_ 常數

**LINEMEDIAMODE \_** 常數描述通訊會話或呼叫)  (或模式的媒體類型。

<dl> <dt>

<span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE \_ AUTOMATEDVOICE**
</dt> <dd> <dl> <dt>



在電話上偵測到語音能源，並由自動化的應用程式（例如與回應機器應用程式）在本機處理語音。 當服務提供者無法分辨來電的互動式和自動語音時，它會將通話報告為互動式語音。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE \_ DATAMODEM**
</dt> <dd> <dl> <dt>



呼叫上的資料數據機會話。 目前的數據機通訊協定需要被呼叫的工作站起始交握。 針對傳入的資料數據機呼叫，應用程式通常不會進行正面的偵測。 服務提供者如何做出這項決定。 例如，在接聽撥入電話之後的一段時間，就可以用來做為判斷這可能是資料數據機呼叫的啟發式。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**
</dt> <dd> <dl> <dt>



ADSI (類比顯示服務介面) 會話的呼叫。 ADSI 會使用下載至手機的英數位元資訊，以及在手機上使用軟按鈕的方式來增強語音通話。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE \_ DIGITALDATA**
</dt> <dd> <dl> <dt>



未指定格式的數位資料流程。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE \_ G3FAX**
</dt> <dd> <dl> <dt>



透過呼叫傳送或接收群組3傳真。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE \_ G4FAX**
</dt> <dd> <dl> <dt>



正在透過呼叫傳送或接收群組4傳真。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE \_ INTERACTIVEVOICE**
</dt> <dd> <dl> <dt>



在通話上偵測到語音能源，並以人類的互動式語音通話來處理這兩個端點的電話。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ 混合**
</dt> <dd> <dl> <dt>



呼叫上的混合會話。 Mixed 是其中一項 ISDN telematic 服務。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE \_ TDD**
</dt> <dd> <dl> <dt>



TDD (電話語音裝置的電話語音) 裝置。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE \_ TELETEX**
</dt> <dd> <dl> <dt>



呼叫上的 teletex 會話。 Teletex 是 telematic 服務之一。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**LINEMEDIAMODE \_ 電傳**
</dt> <dd> <dl> <dt>



呼叫上的電傳會話。 電傳是其中一項 telematic 服務。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**LINEMEDIAMODE \_ 影片**
</dt> <dd> <dl> <dt>



通話的媒體類型是 video。  (TAPI 2.1 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE \_ VIDEOTEX**
</dt> <dd> <dl> <dt>



呼叫上的 videotex 會話。 Videotex 是 telematic 服務之一。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE \_ VOICEVIEW**
</dt> <dd> <dl> <dt>



呼叫的媒體類型為 VoiceView。  (TAPI 1.4 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ 不明**
</dt> <dd> <dl> <dt>



媒體資料流程存在，但其模式目前不是已知的，可能會在稍後變成已知。 這會對應至具有非分類媒體類型的呼叫。 在典型的類比電話語音環境中，連入通話的媒體類型可能會是未知的，直到來電獲得回應並篩選出媒體串流以進行判斷為止。

如果設定了不明的媒體模式旗標，也可以設定其他媒體旗標。 這是用來表示媒體不明，但它可能是其他選取的媒體類型之一。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

所有32位都是保留的。

請注意，持有人模式和媒體類型是不同的概念。 來電的持有人模式是指出網路連線的品質，其主要是由網路所提供。 呼叫的媒體類型表示透過該呼叫交換的資訊資料流程類型。 群組3傳真或資料數據機是使用具有 3.1 kHz 語音持有人模式之呼叫的媒體類型。

為了回溯相容性，服務提供者必須負責檢查該行上的已協商 API 版本，如果協商的版本不支援，則不會使用這個 LINEMEDIAMODE \_ 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




