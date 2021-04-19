---
description: Get \_ MediaTypes 方法會取得與參與者相關聯的媒體類型。
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: 'ITParticipant：： get_MediaTypes 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985537"
---
# <a name="itparticipantget_mediatypes-method"></a>ITParticipant：： get \_ MediaTypes 方法

\[**取得 \_MediaTypes** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ MediaTypes** 方法會取得與參與者相關聯的 [**媒體類型**](tapimediatype--constants.md)。

## <a name="syntax"></a>語法


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*plMediaType* \[擴展\]
</dt> <dd>

媒體類型旗標的指標，例如 TAPIMEDIATYPE \_ VIDEO。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PlMediaType* 參數不是有效的指標。<br/>  |



 

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

[**媒體類型**](tapimediatype--constants.md)
</dt> </dl>

 

 




