---
description: 應用程式會呼叫 PeriodicUpdatePicture 方法來設定資料流程中的計時器，以定期要求圖片更新。 圖片更新會導致高頻寬使用量，因此通常會使用這個方法，而不是 UpdatePicture。
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: 'IKeyFrameControl：:P eriodicUpdatePicture 方法 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bbfb18b0be96d611f0fe385cc825602dc316ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989271"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a>IKeyFrameControl：:P eriodicUpdatePicture 方法

\[**PeriodicUpdatePicture** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

應用程式會呼叫 **PeriodicUpdatePicture** 方法來設定資料流程中的計時器，以定期要求圖片更新。 圖片更新會導致高頻寬使用量，因此通常會使用這個方法，而不是 [**UpdatePicture**](ikeyframecontrol-updatepicture.md)。

如果在資料流程為使用中時呼叫方法，計時器將會立即啟動。 如果資料流程未處於使用中狀態，則當資料流程進入作用中狀態時，就會啟動計時器。

## <a name="syntax"></a>語法


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fEnable* \[在\]
</dt> <dd>

**TRUE** 會啟用計時器。 **FALSE** 會停用它。

</dd> <dt>

*dwInterval* \[在\]
</dt> <dd>

計時器的間隔（以秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 方法成功。<br/>              |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 因為未預期的原因而失敗。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>H323priv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[H323 MSP](h323-msp.md)
</dt> </dl>

 

 




