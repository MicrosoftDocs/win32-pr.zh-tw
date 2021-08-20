---
description: SetCutsOnly 方法會指定是否將轉換轉譯為剪下。 如果是的話，轉換會在剪點立即進行。 如果轉換需要很長的時間才能轉譯，您可能會想要以剪下的速度預覽。
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: 'IAMTimelineTrans：： SetCutsOnly 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3b008e0aef31548dcba71f3b2a2940009c0cd0c71786bd9bd733c206c1d68ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154723"
---
# <a name="iamtimelinetranssetcutsonly-method"></a>IAMTimelineTrans：： SetCutsOnly 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetCutsOnly`方法會指定轉換是否會轉譯為剪下。 如果是的話，轉換會在剪點立即進行。 如果轉換需要很長的時間才能轉譯，您可能會想要以剪下的速度預覽。

## <a name="syntax"></a>語法


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Val* 
</dt> <dd>

指定是否要將轉換轉譯為剪下。 若 **為 TRUE**，則轉換會轉譯為瞬間剪下。 如果 **為 FALSE**，則轉換會轉譯為正常持續時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

將轉換轉譯為剪下與交換輸入不相容。  (請參閱 [**IAMTimelineTrans：： SetSwapInputs**](iamtimelinetrans-setswapinputs.md)) 。如果您呼叫的 `SetCutsOnly` 值為 **TRUE**，它會暫時覆寫 **SetSwapInputs** 設定。 僅限剪設定適用于預覽，不過，這項限制不會影響檔案輸出，只要記得 `SetCutsOnly` 在寫入檔案之前，先使用值 **FALSE** 來呼叫。

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

[**IAMTimelineTrans 介面**](iamtimelinetrans.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




