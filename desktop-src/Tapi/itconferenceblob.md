---
description: 操縱文字會議描述。
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: 'ITConferenceBlob 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa130e4456f206b27e41d03ead47138c777f9dad9e41d5d834bb018b29fc5447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119379088"
---
# <a name="itconferenceblob-interface"></a>ITConferenceBlob 介面

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**ITConferenceBlob** 介面會操控文字會議描述。 介面的設計目的是要與會議描述的格式和語法無關。 若要操作會議描述的特定層面，應用程式必須查詢另一個介面。 目前只支援 SDP 會議說明;應用程式必須使用 **QueryInterface** 進行 [**ITSdp**](itsdp.md) ，才能存取 SDP 會議描述的各種欄位。 **ITConferenceBlob** 介面是藉由在 [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)上呼叫 **QueryInterface** 來建立。

## <a name="members"></a>成員

**ITConferenceBlob** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ITConferenceBlob** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITConferenceBlob** 介面具有這些方法。



| 方法                                                             | 描述                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ CharacterSet**](itconferenceblob-get-characterset.md)     | 取得 blob [**\_ 字元集 \_**](blob-character-set.md) 指標，其中 BLOB 字元是否為 ASCII、Unicode 等等。<br/> |
| [**取得 \_ ConferenceBlob**](itconferenceblob-get-conferenceblob.md) | 取得會議 blob 的指標。<br/>                                                                                             |
| [**Init**](itconferenceblob-init.md)                              | 初始化會議 blob。<br/>                                                                                                   |
| [**SetConferenceBlob**](itconferenceblob-setconferenceblob.md)    | 認可會議 blob 的變更。<br/>                                                                                            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

