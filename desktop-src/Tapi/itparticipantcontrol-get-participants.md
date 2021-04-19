---
description: 取得 \_ 參與者方法會建立與目前會議相關聯的參與者集合。
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: 'ITParticipantControl：： get_Participants 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4a99e0efe7702a3358684b00af5e8faa96461c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999209"
---
# <a name="itparticipantcontrolget_participants-method"></a>ITParticipantControl：：取得 \_ 參與者方法

\[**取得 \_參與者** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**取得 \_ 參與者** 方法會建立與目前會議相關聯的參與者集合。 這個方法是針對 Automation 用戶端應用程式所提供，例如以 Visual Basic 撰寫的應用程式。 C 和 c + + 應用程式必須使用 [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVariant* \[擴展\]
</dt> <dd>

**VARIANT** 的指標，其中包含 [**ITParticipant**](itparticipant.md)介面指標的 [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                         | 意義                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PVariant* 參數不是有效的指標。<br/>     |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

TAPI 會在 **ITParticipantControl：： get \_ 參與者** 所傳回的 [**ITParticipant**](itparticipant.md)介面上呼叫 **AddRef** 方法。 應用程式必須在 **ITParticipant** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITParticipantControl**](itparticipantcontrol.md)
</dt> <dt>

[**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md)
</dt> <dt>

[**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




