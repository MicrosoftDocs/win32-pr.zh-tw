---
description: Get \_ Size 方法會傳回目前的輸出大小和延展模式。
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: 'IResize：： get_Size 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 747ca8d7fd839321a9dbf4403c503652b932403e49bb964ae6148da2f49c5ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818209"
---
# <a name="iresizeget_size-method"></a>IResize：： get \_ Size 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會傳回 `get_Size` 目前的輸出大小和延展模式。

## <a name="syntax"></a>語法


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
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

</dd> <dt>

*pFlag* \[擴展\]
</dt> <dd>

接收指定延展模式的旗標。 請參閱重 [**設大小旗標**](resize-flags.md) 的可能值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果輸出類型尚未設定，則篩選準則應該會傳回預設值。 這些值可在設計階段任意選擇。

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

 

 




