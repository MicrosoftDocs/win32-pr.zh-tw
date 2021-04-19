---
description: ITSdp 介面提供 (SDP 的會話描述項通訊協定操作方法，請參閱 RFC 2327) 會議 blob 元件。
ms.assetid: 77c1e302-6290-4eeb-b7c9-462a13b29dcd
title: 'ITSdp 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401dbe2548375227be2ca024ee75de3054fa6f6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978532"
---
# <a name="itsdp-interface"></a>ITSdp 介面

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**ITSdp** 介面提供 (SDP 的會話描述項通訊協定操作方法，請參閱 RFC 2327) 會議 blob 元件。 這個攔截器提供的功能包括：

-   提供所有媒體通用屬性的存取權。 這些內容包括與建立者的個人資訊、會話描述和網址類別型資訊有關的屬性。
-   提供透過屬性存取時間和媒體集合的起點。

**ITSdp** 介面是藉由在 [**ITConferenceBlob**](itconferenceblob.md)上呼叫 **QueryInterface** 來建立。

## <a name="members"></a>成員

**ITSdp** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ITSdp** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITSdp** 介面具有這些方法。



| 方法                                                    | 描述                                                                                         |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**取得 \_ 描述**](itsdp-get-description.md)         | 取得會話描述。<br/>                                                            |
| [**取得 \_ IsValid**](itsdp-get-isvalid.md)                 | 驗證適用于結構和域值的 SDP blob。<br/>                                   |
| [**取得 \_ MachineAddress**](itsdp-get-machineaddress.md)   | 取得來源主機的電腦位址。<br/>                                        |
| [**取得 \_ MediaCollection**](itsdp-get-mediacollection.md) | 取得會議 [**ITMediaCollection**](itmediacollection.md) 介面的指標。<br/> |
| [**取得 \_ 名稱**](itsdp-get-name.md)                       | 取得會話名稱。<br/>                                                                   |
| [**取得 \_ 建立者**](itsdp-get-originator.md)           | 取得會議製作者。<br/>                                                              |
| [**取得 \_ ProtocolVersion**](itsdp-get-protocolversion.md) | 取得 SDP 通訊協定版本。<br/>                                                           |
| [**取得 \_ SessionId**](itsdp-get-sessionid.md)             | 取得32位 NTP (網路時間通訊協定) 值，作為會話識別碼。<br/> |
| [**取得 \_ SessionVersion**](itsdp-get-sessionversion.md)   | 取得32位 (理想的 NTP) 值，作為會話版本。<br/>                  |
| [**取得 \_ TimeCollection**](itsdp-get-timecollection.md)   | 取得會議 [**ITTimeCollection**](ittimecollection.md) 介面的指標。<br/>   |
| [**取得 \_ Url**](itsdp-get-url.md)                         | 取得 URL。<br/>                                                                            |
| [**GetEmailNames**](itsdp-getemailnames.md)              | 取得與會議 blob 相關聯的電子郵件名稱和位址陣列。<br/>                |
| [**GetPhoneNumbers**](itsdp-getphonenumbers.md)          | 取得電話號碼。<br/>                                                                  |
| [**put \_ 描述**](itsdp-put-description.md)         | 設定會話描述。<br/>                                                            |
| [**put \_ MachineAddress**](itsdp-put-machineaddress.md)   | 設定來源主機的電腦位址。<br/>                                        |
| [**put \_ 名稱**](itsdp-put-name.md)                       | 設定會話名稱。<br/>                                                                   |
| [**put \_ 建立者**](itsdp-put-originator.md)           | 取得會議製作者。<br/>                                                              |
| [**put \_ SessionVersion**](itsdp-put-sessionversion.md)   | 設定會話版本。<br/>                                                                    |
| [**put \_ Url**](itsdp-put-url.md)                         | 設定 URL。<br/>                                                                            |
| [**SetEmailNames**](itsdp-setemailnames.md)              | 設定與會議 blob 相關聯的電子郵件名稱和位址陣列。<br/>                 |
| [**SetPhoneNumbers**](itsdp-setphonenumbers.md)          | 設定電話號碼。<br/>                                                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

