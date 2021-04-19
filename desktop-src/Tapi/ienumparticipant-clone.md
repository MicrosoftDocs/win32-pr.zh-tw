---
description: Clone 方法會建立另一個列舉值，其中包含與目前相同的列舉狀態。 這種方法在 Visual Basic 和指令碼語言中是隱藏的。
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: 'IEnumParticipant：： Clone 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b094f47738fd23f2762b7012a4e23c8b89da57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001208"
---
# <a name="ienumparticipantclone-method"></a>IEnumParticipant：： Clone 方法

\[在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用 **複製**。 RTC 用戶端 API 提供類似的功能。\]

**Clone** 方法會建立另一個列舉值，其中包含與目前相同的列舉狀態。 這種方法在 Visual Basic 和指令碼語言中是隱藏的。

## <a name="syntax"></a>語法


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppEnum* \[擴展\]
</dt> <dd>

新 [**IEnumParticipant**](ienumparticipant.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PpEnum* 參數不是有效的指標。<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>  | 因不明原因而失敗。<br/>                          |



 

## <a name="remarks"></a>備註

TAPI 會在 **IEnumParticipant：： Clone** 所傳回的 [**IEnumParticipant**](ienumparticipant.md)介面上呼叫 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)方法。 應用程式必須在 **IEnumParticipant** 介面上呼叫 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ，才能釋放與其相關聯的資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

