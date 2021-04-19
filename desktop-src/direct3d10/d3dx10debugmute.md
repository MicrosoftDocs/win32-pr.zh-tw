---
description: 啟用或停用 debug 訊息。
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: 'D3DX10DebugMute 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DebugMute
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f331e3f074a4b77a1f1a7f1a8117cf660940f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989213"
---
# <a name="d3dx10debugmute-function"></a>D3DX10DebugMute 函式

啟用或停用 debug 訊息。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*靜音* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

設定為 **TRUE** 以啟用 debug 訊息;設定為 **FALSE** 以停用 debug 訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

使用此函式可在 debug 期間停用 D3DX10 Api 的錯誤訊息;使用此函式應該受到 D3D10 \_ DEBUG 編譯器參數的保護。


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



Debug 組建的預設狀態為 **TRUE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
