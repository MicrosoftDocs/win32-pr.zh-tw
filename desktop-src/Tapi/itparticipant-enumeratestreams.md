---
description: EnumerateStreams 方法會列舉目前與參與者的資料流程。 這個方法是針對 C 和 c + + 應用程式所提供。 Automation 用戶端應用程式（例如以 Visual Basic 撰寫的應用程式）必須使用「取得 \_ 資料流程」方法。
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: 'ITParticipant：： EnumerateStreams 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbc92c617ed4baee3ecc33aec65cbdcf50986a27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981310"
---
# <a name="itparticipantenumeratestreams-method"></a>ITParticipant：： EnumerateStreams 方法

\[**EnumerateStreams** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**EnumerateStreams** 方法會列舉目前與參與者的資料流程。 這個方法是針對 C 和 c + + 應用程式所提供。 Automation 用戶端應用程式（例如以 Visual Basic 撰寫的應用程式）必須使用「 [**取得 \_ 資料流程**](itparticipant-get-streams.md) 」方法。

## <a name="syntax"></a>語法


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppEnumStream* \[擴展\]
</dt> <dd>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)介面指標的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                     | 意義                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl> | *PpEnumStream* 參數不是有效的指標。<br/> |



 

## <a name="remarks"></a>備註

TAPI 會在 **ITParticipant：： EnumerateStreams** 傳回的 [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)介面上呼叫 **AddRef** 方法。 應用程式必須在 **IEnumStream** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。

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

[**取得 \_ 資料流程**](itparticipant-get-streams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




