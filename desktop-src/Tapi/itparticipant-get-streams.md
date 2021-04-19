---
description: 取得 \_ 資料流程方法會建立與目前參與者相關聯的資料流程集合。
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: 'ITParticipant：： get_Streams 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a920929c71e01632edcd8c4c78029b479d8b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987117"
---
# <a name="itparticipantget_streams-method"></a>ITParticipant：： get \_ 串流方法

\[**取得 \_資料流程** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**取得 \_ 資料流程** 方法會建立與目前參與者相關聯的資料流程集合。 這個方法是針對 Automation 用戶端應用程式所提供，例如以 Visual Basic 撰寫的應用程式。 C 和 c + + 應用程式必須使用 [**EnumerateStreams**](itparticipant-enumeratestreams.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVariant* \[擴展\]
</dt> <dd>

**VARIANT** 的指標，其中包含 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)介面指標的 [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                         | 意義                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PVariant* 參數不是有效的指標。<br/>     |



 

## <a name="remarks"></a>備註

TAPI 會在 **ITParticipant：： get \_ 資料流程** 所傳回的 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)介面上呼叫 **AddRef** 方法。 應用程式必須在 **ITStream** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**EnumerateStreams**](itparticipant-enumeratestreams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

