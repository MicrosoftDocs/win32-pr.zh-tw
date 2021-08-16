---
description: ITParticipant 介面是由 IPConf MSP 所執行。 它可讓應用程式取得會議參與者的相關資訊，並取得與這些參與者相關聯之資料流程的指標。
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: 'ITParticipant 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab4ff4c496616804efc1a65a728bbb658fba5bb1278939bdfb2185705684c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682648"
---
# <a name="itparticipant-interface"></a>ITParticipant 介面

\[**ITParticipant** 無法在 Windows Vista、Windows Server 2008 及後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**ITParticipant** 介面是由 [IPConf MSP](ipconf-msp.md)所執行。 它可讓應用程式取得會議參與者的相關資訊，並取得與這些參與者相關聯之資料流程的指標。

當呼叫使用 IP 會議時，會在呼叫物件上公開這個介面。 您可以使用 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)指標呼叫 **QueryInterface** 來取得指標。

## <a name="members"></a>成員

**ITParticipant** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITParticipant** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITParticipant** 介面具有這些方法。



| 方法                                                                      | 描述                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateStreams**](itparticipant-enumeratestreams.md)                  | 列舉與目前參與者相關聯的資料流程。<br/>                                                                                                  |
| [**取得 \_ MediaTypes**](itparticipant-get-mediatypes.md)                     | 取得與參與者相關聯的 [**媒體類型**](tapimediatype--constants.md) 。<br/>                                                                      |
| [**取得 \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) | 取得所需資訊類型的 BSTR 標記法，例如 PTI \_ EMAILADDRESS。<br/>                                                                     |
| [**取得 \_ 狀態**](itparticipant-get-status.md)                             | 取得參與者的狀態。<br/>                                                                                                                          |
| [**取得 \_ 資料流程**](itparticipant-get-streams.md)                           | 建立與目前參與者相關聯的資料流程集合。 提供給 Automation 用戶端應用程式，例如以 Visual Basic 撰寫的應用程式。<br/> |
| [**put \_ 狀態**](itparticipant-put-status.md)                             | 設定是否啟用與參與者相關聯的資料流程。<br/>                                                                                            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[IPConf MSP 介面](ipconf-msp-interfaces.md)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

