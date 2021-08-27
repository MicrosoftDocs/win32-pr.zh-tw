---
description: GetNextTrans 方法會抓取在指定時間或之後出現的第一個轉換。
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'IAMTimelineTransable：： GetNextTrans 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 892f8e0f4af39250d62da9ed662c22867f98ebfc32baeaa0f341ead2eef665a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131078"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a>IAMTimelineTransable：： GetNextTrans 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`GetNextTrans`方法會抓取在指定時間或之後出現的第一個轉換。

## <a name="syntax"></a>語法


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
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

變數的指標，此變數會以 100-毫微秒單位來指定時間。 在輸入時，這個值會指定要從中尋找轉換的時間。 在輸出時，如果已抓取轉換，此值會設定為轉換的停止時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果方法會抓取轉換，則傳回 [確定]， \_ 如果找不到轉換，則傳回 FALSE。 否則，會傳回 **HRESULT** 值，指出失敗的原因。

## <a name="remarks"></a>備註

如果轉換跨越指定的時間，轉換的開始時間可能會小於您在外接 *引線* 中指定的時間。

如果方法傳回 S \_ OK，則傳回的 [**IAMTimelineObj**](iamtimelineobj.md) 介面具有未處理的參考計數。 使用完畢後，請務必釋放介面。

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

[**IAMTimelineTransable 介面**](iamtimelinetransable.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




