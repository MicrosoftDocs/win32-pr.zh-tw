---
description: GetDefaultFPS 方法會抓取預設的輸出畫面播放速率（以每秒畫面格數 (FPS) ）。 群組會使用此值做為其預設的畫面播放速率。 若要設定群組的畫面播放速率，請在群組上呼叫 IAMTimelineGroup：： SetOutputFPS 方法。
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: 'IAMTimeline：： GetDefaultFPS 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 38f12abe47829544453d0aed9b8f08bffd2b5864f78fc35c873622d960387931
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107848"
---
# <a name="iamtimelinegetdefaultfps-method"></a>IAMTimeline：： GetDefaultFPS 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `GetDefaultFPS` 預設的輸出畫面播放速率（以每秒畫面格數 (FPS) ）。 群組會使用此值做為其預設的畫面播放速率。 若要設定群組的畫面播放速率，請在群組上呼叫 [**IAMTimelineGroup：： SetOutputFPS**](iamtimelinegroup-setoutputfps.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFPS* 
</dt> <dd>

接收預設畫面播放速率（以每秒畫面格數為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

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

[**IAMTimeline 介面**](iamtimeline.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




