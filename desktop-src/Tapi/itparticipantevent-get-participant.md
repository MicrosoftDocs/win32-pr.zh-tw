---
description: Get \_ 參與者方法會取得 ITParticipant 介面陣列的指標，代表牽涉到事件的參與者。
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: 'ITParticipantEvent：： get_Participant 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e9ee84bac69bd77237f1a50b9a008b2830258
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978751"
---
# <a name="itparticipanteventget_participant-method"></a>ITParticipantEvent：： get \_ 參與者方法

\[**取得 \_參與者** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ 參與者** 方法會取得 [**ITParticipant**](itparticipant.md)介面陣列的指標，代表牽涉到事件的參與者。

## <a name="syntax"></a>語法


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppParticipant* \[擴展\]
</dt> <dd>

[**ITParticipant**](itparticipant.md)介面陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                           | 意義                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>            | 方法成功。<br/>                                     |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | 記憶體不足，無法執行操作。<br/>  |
| <dl> <dt>**TAPI \_ E \_ NOITEMS**</dt> </dl> | 沒有與此事件相關聯的參與者。<br/>  |
| <dl> <dt>**E \_ 指標**</dt> </dl>       | *PpParticipant* 參數不是有效的指標。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




