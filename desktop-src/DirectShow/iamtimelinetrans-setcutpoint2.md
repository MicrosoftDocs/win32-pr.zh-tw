---
description: SetCutPoint2 方法會設定當轉換轉譯為剪下時，轉換從某個來源剪下的時間。 這個方法相當於 IAMTimelineTrans：： SetCutPoint，但會接受 REFTIME 值。
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: 'IAMTimelineTrans：： SetCutPoint2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 117ec522416f0d5722c8ef7aa17cd6e81720b4c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993962"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a>IAMTimelineTrans：： SetCutPoint2 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetCutPoint2`如果轉換是轉譯為剪下，則方法會設定轉換從某個來源減少到下一個來源的時間。 這個方法相當於 [**IAMTimelineTrans：： SetCutPoint**](iamtimelinetrans-setcutpoint.md)，但會接受 [**REFTIME**](reftime.md) 值。

## <a name="syntax"></a>語法


```C++
HRESULT SetCutPoint2(
   REFTIME TLTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TLTime* 
</dt> <dd>

相對於轉換開始的切割點（以秒為單位）。

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

[**IAMTimelineTrans 介面**](iamtimelinetrans.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




