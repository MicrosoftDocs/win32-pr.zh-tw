---
description: 當 IPConf MSP 支援呼叫時，會在資料流程物件上公開 ITLocalParticipant 介面。
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: 'ITLocalParticipant 介面 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4017837a0b970cb791cdf454437fe2d48720028
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980120"
---
# <a name="itlocalparticipant-interface"></a>ITLocalParticipant 介面

當 IPConf MSP 支援呼叫時，會在資料流程物件上公開 **ITLocalParticipant** 介面。 MSP 會實行可讓應用程式取得和設定參與者資訊的方法。 **ITLocalParticipant** 介面是藉由在 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)上呼叫 **QueryInterface** 來建立。

## <a name="members"></a>成員

**ITLocalParticipant** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITLocalParticipant** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITLocalParticipant** 介面具有這些方法。



| 方法                                                                                     | 描述                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**取得 \_ LocalParticipantTypedInfo**](itlocalparticipant-get-localparticipanttypedinfo.md) | 取得參與者資訊，例如電子郵件名稱或地理位置。<br/> |
| [**put \_ LocalParticipantTypedInfo**](itlocalparticipant-put-localparticipanttypedinfo.md) | 設定參與者資訊。<br/>                                               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

