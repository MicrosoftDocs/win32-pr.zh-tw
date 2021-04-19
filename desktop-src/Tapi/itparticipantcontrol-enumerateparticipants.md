---
description: EnumerateParticipants 方法會列舉與目前會議相關聯的參與者。
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: 'ITParticipantControl：： EnumerateParticipants 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988655"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a>ITParticipantControl：： EnumerateParticipants 方法

\[**EnumerateParticipants** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**EnumerateParticipants** 方法會列舉與目前會議相關聯的參與者。 這個方法是針對 C 和 c + + 應用程式所提供。 Automation 用戶端應用程式（例如以 Visual Basic 撰寫的應用程式）必須使用 [**取得 \_ 參與者**](itparticipantcontrol-get-participants.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppEnumParticipants* \[擴展\]
</dt> <dd>

[**IEnumParticipant**](ienumparticipant.md)介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                         | 意義                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                          |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PpEnumParticipants* 參數不是有效的指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>       |



 

## <a name="remarks"></a>備註

TAPI 會在 **ITParticipantControl：： EnumerateParticipants** 傳回的 [**IEnumParticipant**](ienumparticipant.md)介面上呼叫 **AddRef** 方法。 應用程式必須在 **IEnumParticipant** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。

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

[**取得 \_ 參與者**](itparticipantcontrol-get-participants.md)
</dt> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




