---
description: EnableTransitions 方法會啟用或停用時間軸中的所有轉換。
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'IAMTimeline：： EnableTransitions 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987064"
---
# <a name="iamtimelineenabletransitions-method"></a>IAMTimeline：： EnableTransitions 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`EnableTransitions`方法會啟用或停用時間軸中的所有轉換。 如果轉換已停用，則轉譯引擎會將它們視為剪下;也就是說，轉譯的輸出會立即從一個播放軌跳到下一個曲目。 預設的剪點是過渡期間的一半。 您可以在轉換上呼叫 [**IAMTimelineTrans：： SetCutPoint**](iamtimelinetrans-setcutpoint.md) 方法來變更剪下點。 停用的轉換不會從時間軸中移除。

## <a name="syntax"></a>語法


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fEnabled* 
</dt> <dd>

指定是否要啟用或停用轉換的布林值。 若 **為 TRUE**，則會啟用轉換。 如果 **為 FALSE**，則會停用轉換。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimeline 介面**](iamtimeline.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




