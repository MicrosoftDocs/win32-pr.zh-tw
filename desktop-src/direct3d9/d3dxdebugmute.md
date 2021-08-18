---
description: 開啟或關閉所有 D3DX 的調試輸出。
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: 'D3DXDebugMute 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDebugMute
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2bde5446e6e41568c1f9d6aa8408dacc276ab82112a176cf8a038536dd4d992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045076"
---
# <a name="d3dxdebugmute-function"></a>D3DXDebugMute 函式

開啟或關閉所有 D3DX 的調試輸出。

## <a name="syntax"></a>語法


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*靜音* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

若 **為 TRUE**，則會停止偵錯工具輸出;如果 **為 FALSE**，則表示已啟用偵錯工具輸出。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

傳回前一個靜音值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
