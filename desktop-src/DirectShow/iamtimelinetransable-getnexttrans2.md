---
description: GetNextTrans2 方法會抓取在指定時間或之後出現的第一個轉換。 這個方法相當於 IAMTimelineTransable：： GetNextTrans，但會接受 REFTIME 值。
ms.assetid: e6910e94-f289-4a5d-9976-1e8f7373c882
title: 'IAMTimelineTransable：： GetNextTrans2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c5f79ff20507247fbcac3badceaf2c3e28f0303
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997035"
---
# <a name="iamtimelinetransablegetnexttrans2-method"></a>IAMTimelineTransable：： GetNextTrans2 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`GetNextTrans2`方法會抓取在指定時間或之後出現的第一個轉換。 這個方法相當於 [**IAMTimelineTransable：： GetNextTrans**](iamtimelinetransable-getnexttrans.md)，但會接受 [**REFTIME**](reftime.md) 值。

## <a name="syntax"></a>語法


```C++
HRESULT GetNextTrans2(
  [out] IAMTimelineObj **ppTrans,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppTrans* \[擴展\]
</dt> <dd>

接收轉換物件之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。

</dd> <dt>

*接腳* 
</dt> <dd>

指定時間（以秒為單位）之變數的指標。 在輸入時，這個值會指定要從中尋找轉換的時間。 在輸出時，如果已抓取轉換，此值會設定為轉換的停止時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果方法會抓取轉換，則傳回 [確定]， \_ 如果找不到轉換，則傳回 FALSE。 否則，會傳回 **HRESULT** 值，指出失敗的原因。

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

[**IAMTimelineTransable 介面**](iamtimelinetransable.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




