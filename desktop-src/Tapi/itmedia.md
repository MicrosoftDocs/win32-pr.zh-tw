---
description: ITMedia 介面是會話描述項通訊協定 (SDP 中媒體的標記法，請參閱 RFC 2327) 。
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: 'ITMedia 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfd1cf7dcf8ef294481a4687dbac950f97b4adede6a6871222292127e6255057
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034638"
---
# <a name="itmedia-interface"></a>ITMedia 介面

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**ITMedia** 介面是會話描述項通訊協定 (SDP 中媒體的標記法，請參閱 RFC 2327) 。 此介面會匯出方法來取得和設定基本媒體屬性，例如類型。 [**ITMediaCollection：： get \_ 專案**](itmediacollection-get-item.md)和 [**ITMediaCollection：： Create**](itmediacollection-create.md)方法會建立 **ITMedia** 介面。

## <a name="members"></a>成員

**ITMedia** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ITMedia** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITMedia** 介面具有這些方法。



| 方法                                                          | 描述                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**取得 \_ FormatCodes**](itmedia-get-formatcodes.md)             | 取得媒體承載格式碼的清單。<br/>                                          |
| [**取得 \_ MediaName**](itmedia-get-medianame.md)                 | 取得媒體名稱。<br/>                                                                  |
| [**取得 \_ MediaTitle**](itmedia-get-mediatitle.md)               | 取得媒體標題。<br/>                                                                 |
| [**取得 \_ NumPorts**](itmedia-get-numports.md)                   | 取得會話所需的埠數目。<br/>                                      |
| [**取得 \_ StartPort**](itmedia-get-startport.md)                 | 取得第一個埠的16位埠值。<br/>                                        |
| [**取得 \_ TransportProtocol**](itmedia-get-transportprotocol.md) | 取得傳輸通訊協定。<br/>                                                          |
| [**put \_ FormatCodes**](itmedia-put-formatcodes.md)             | 設定媒體承載格式代碼的清單。<br/>                                          |
| [**put \_ MediaName**](itmedia-put-medianame.md)                 | 設定媒體名稱。<br/>                                                                  |
| [**put \_ MediaTitle**](itmedia-put-mediatitle.md)               | 設定媒體標題。<br/>                                                                 |
| [**put \_ TransportProtocol**](itmedia-put-transportprotocol.md) | 設定傳輸通訊協定。<br/>                                                          |
| [**SetPortInfo**](itmedia-setportinfo.md)                      | 設定第一個埠的16位埠值，以及會話所需的埠數目。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> <dt>

[**ITSDP**](itsdp.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

