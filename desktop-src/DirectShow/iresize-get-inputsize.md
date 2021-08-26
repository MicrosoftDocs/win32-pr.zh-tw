---
description: Get \_ InputSize 方法會傳回檔整器篩選的目前輸入大小。
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'IResize：： get_InputSize 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3b862237f8c51bdf6c22ca9acb667199fadee33b37e425efabfe25bdb8a20dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078928"
---
# <a name="iresizeget_inputsize-method"></a>IResize：： get \_ InputSize 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會傳回 `get_InputSize` 調整器篩選的目前輸入大小。

## <a name="syntax"></a>語法


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*piHeight* \[擴展\]
</dt> <dd>

接收影片高度（以圖元為單位）。

</dd> <dt>

*piWidth* \[擴展\]
</dt> <dd>

接收影片寬度（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果篩選的輸入 pin 未連接，則傳回錯誤碼。 否則，會傳回影片的寬度和高度，如輸入釘選的媒體類型所指定。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | DirectX 9.0 或更新版本<br/>                                                         |
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> <dt>

[**IResize 介面**](iresize.md)
</dt> </dl>

 

 




