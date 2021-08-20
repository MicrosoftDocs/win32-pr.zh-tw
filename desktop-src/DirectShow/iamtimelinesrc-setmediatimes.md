---
description: SetMediaTimes 方法會設定媒體停止和開始時間。
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: 'IAMTimelineSrc：： SetMediaTimes 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5de058e31da605b96f7b013c03e9c0d020daa11ec676618b4a13f5ff92e701f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154924"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a>IAMTimelineSrc：： SetMediaTimes 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetMediaTimes`方法會設定媒體停止和開始時間。

## <a name="syntax"></a>語法


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*開始* 
</dt> <dd>

媒體開始時間，以 100-毫微秒單位表示。

</dd> <dt>

*停止* 
</dt> <dd>

媒體停止時間，以 100-毫微秒單位表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

媒體時間是相對於原始媒體檔案的停止和開始時間。 當您將影片或音訊來源新增至時間軸時，一律設定媒體時間。 否則，可能會發生轉譯問題。 停止時間必須大於開始時間。

若要從影片來源使用仍然的框架，請將停止時間設定為比開始時間更多的小數數量，例如100毫微秒。 將其設定為相同的值會導致轉譯錯誤。

如果時間軸的持續時間不符合媒體持續時間，則來源會據以伸展或縮小。 這會使剪輯的播放速度比撰寫的速率慢或更快。  (音調變化將會在音訊來源中發生。如需詳細資訊，請參閱[DirectShow 編輯服務的時間](time-in-directshow-editing-services.md)) 。

您可以藉由呼叫 [**SetMediaLength**](iamtimelinesrc-setmedialength.md) 方法來指定原始程式檔的持續時間。 如果您設定超過持續時間的媒體停止時間，DES 會截斷停止時間。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineSrc 介面**](iamtimelinesrc.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




