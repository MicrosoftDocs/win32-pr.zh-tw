---
description: LINEBEARERMODE \_ 位旗標常數描述通話的不同持有人模式。
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: 'LINEBEARERMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7d48689dd435e0a07e1ce9fa5a2a9915b1bf69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999515"
---
# <a name="linebearermode_-constants"></a>LINEBEARERMODE \_ 常數

**LINEBEARERMODE \_** 位旗標常數描述通話的不同持有人模式。 當應用程式進行呼叫時，它可以要求特定的持有人模式。 這些模式可用來針對來自基礎電話網絡的要求連接，選取特定的服務品質。 指定行上可用的持有人模式是線路的裝置功能。

<dl> <dt>

<span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE \_ ALTSPEECHDATA**
</dt> <dd> <dl> <dt>



相同呼叫 (ISDN) 的其他語音或不受限制資料傳輸。


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**LINEBEARERMODE \_ 資料**
</dt> <dd> <dl> <dt>



呼叫上不受限制的資料傳輸。 資料速率是另外指定的。


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE \_ 多次使用**
</dt> <dd> <dl> <dt>



由 ISDN 定義的多次使用模式。


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE \_ NONCALLSIGNALING**
</dt> <dd> <dl> <dt>



這會對應至從應用程式到服務提供者或交換器的非通話關聯信號連線， (由 TAPI) 視為媒體串流。


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE \_ 傳遞**
</dt> <dd> <dl> <dt>



當呼叫在 LINEBEARERMODE 傳遞中為作用中時 \_ ，服務提供者可讓應用程式直接存取附加的硬體來控制。 這種模式主要是由應用程式 desiring 對非同步數據機的暫時直接控制（透過 [通訊功能](/windows/desktop/DevIO/communications-functions)來存取），以設定或使用服務提供者不支援的特殊功能。


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE \_ RESTRICTEDDATA**
</dt> <dd> <dl> <dt>



數位資料的持有人服務，其中每個八位的低序位七位可能包含使用者資料 (例如，用於切換的 56kbit/s 服務) 。


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE \_ 語音**
</dt> <dd> <dl> <dt>



這對應于呼叫上的 g. g.711 語音傳輸。 網路可以使用處理技術，例如類比傳輸、回應取消，以及壓縮/解壓縮。 不保證位完整性。 語音的目的不是支援傳真和數據機媒體類型。


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE \_ 語音**
</dt> <dd> <dl> <dt>



這是標準的 3.1 kHz 類比語音等級持有人服務。 不保證位完整性。 語音可以支援傳真和數據機媒體類型。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

您可以為裝置專屬的延伸模組指派高序位16位。 低序位16位是保留的。

請注意，持有人模式和媒體類型是不同的概念。 來電的持有人模式是指出網路連線的品質，其主要是由網路所提供。 呼叫的媒體類型表示透過該呼叫交換的資訊資料流程類型。 群組3傳真或資料數據機是使用具有 3.1 kHz 語音持有人模式之呼叫的媒體類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

