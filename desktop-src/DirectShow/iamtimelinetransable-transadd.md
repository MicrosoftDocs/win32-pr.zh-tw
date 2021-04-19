---
description: TransAdd 方法會將轉換新增至物件。 物件可以有多個轉換，但是不能在時間內重迭。 轉換必須落在物件的時間界限內。
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: 'IAMTimelineTransable：： TransAdd 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2636922549635c4a1c5e6e0b36f308f62328dc60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984443"
---
# <a name="iamtimelinetransabletransadd-method"></a>IAMTimelineTransable：： TransAdd 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`TransAdd`方法會將轉換新增至物件。 物件可以有多個轉換，但是不能在時間內重迭。 轉換必須落在物件的時間界限內。

## <a name="syntax"></a>語法


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTrans* 
</dt> <dd>

要加入之轉換的 [**IAMTimelineObj**](iamtimelineobj.md) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                   | Description                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無法插入轉換。<br/>              |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | *pTrans* 不是轉換的指標。<br/> |



 

## <a name="remarks"></a>備註

如果轉換與現有的轉換重迭，則方法會傳回 E \_ INVALIDARG。

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

[**IAMTimelineTransable 介面**](iamtimelinetransable.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




