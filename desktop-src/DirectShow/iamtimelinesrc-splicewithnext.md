---
description: SpliceWithNext 方法會將來源物件加入至另一個來源物件。
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: 'IAMTimelineSrc：： SpliceWithNext 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1ffde9c7bb0416f2b296f7a7c347a058734430be33ef4ecde59e7e39cd6e845f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154829"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a>IAMTimelineSrc：： SpliceWithNext 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會將 `SpliceWithNext` 來源物件聯結至另一個來源物件。

## <a name="syntax"></a>語法


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNext* 
</dt> <dd>

要聯結至目前來源之來源物件的 [**IAMTimelineObj**](iamtimelineobj.md) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的傳回值包括下列各項：



| 傳回碼                                                                                   | 描述                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效引數。<br/>                                             |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | *PNext* 參數所指定的物件不是來源物件。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | **Null** 指標引數。<br/>                                    |



 

## <a name="remarks"></a>備註

目前已執行，這個方法會捨棄對 *pNext* 的任何影響。

若要讓這個方法成功， *pNext* 必須是目前來源物件的相符框架，定義如下：

-   它必須共用相同的原始檔。
-   媒體開始時間必須等於目前來源的媒體停止時間。
-   播放速率必須相同。 播放速率是媒體持續時間除以時間軸持續時間。

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

 

 




