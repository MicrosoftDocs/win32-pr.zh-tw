---
description: GetStartStop 方法會抓取物件的開始和停止時間（相對於物件的父系）。
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: 'IAMTimelineObj：： GetStartStop 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d808d7ac2ee3b6c1cbeddc39c730fc38b7032bde86ce726af03379d71241679c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400784"
---
# <a name="iamtimelineobjgetstartstop-method"></a>IAMTimelineObj：： GetStartStop 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `GetStartStop` 物件的開始和停止時間（相對於物件的父系）。

## <a name="syntax"></a>語法


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStart* 
</dt> <dd>

接收開始時間，以 100-毫微秒單位表示。

</dd> <dt>

*pStop* 
</dt> <dd>

接收停止時間，以 100-毫微秒單位表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

組合、群組和曲目的開始時間一律為0。

在轉譯期間，DES 會將物件的開始和停止時間四捨五入至最接近的框架界限。 不過，DES 不會覆寫物件的時間。 如果您變更群組畫面播放速率，則永遠會從原始時間計算舍入的時間。 如需詳細資訊，請[DirectShow 編輯服務的時間](time-in-directshow-editing-services.md)。

若要判斷轉譯專案中的開始和停止時間，請將傳回的值傳遞 `GetStartStop` 給 [**IAMTimelineObj：： FixTimes**](iamtimelineobj-fixtimes.md) 方法。

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

[**IAMTimelineObj 介面**](iamtimelineobj.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




