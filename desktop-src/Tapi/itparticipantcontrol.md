---
description: ITParticipantControl 介面是由 IPConf MSP 所執行。
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: 'ITParticipantControl 介面 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075748f0c35cbc5af3c6cd07277d15222e0658
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998408"
---
# <a name="itparticipantcontrol-interface"></a>ITParticipantControl 介面

\[**ITParticipantControl** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**ITParticipantControl** 介面是由 IPConf MSP 所執行。 此介面會在呼叫物件上公開。 這個介面可讓應用程式取得會議中參與者的指標。 **ITParticipantControl** 介面是藉由在 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)上呼叫 **QueryInterface** 來建立。

## <a name="members"></a>成員

**ITParticipantControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITParticipantControl** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITParticipantControl** 介面具有這些方法。



| 方法                                                                      | 描述                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) | 列舉目前參與會議的參與者。<br/>                                                                                                    |
| [**取得 \_ 參與者**](itparticipantcontrol-get-participants.md)          | 建立與目前會議相關聯的參與者集合。 提供給 Automation 用戶端應用程式，例如以 Visual Basic 撰寫的應用程式。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

