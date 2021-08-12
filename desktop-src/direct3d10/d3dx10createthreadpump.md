---
description: 建立執行緒抽取。
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: 'D3DX10CreateThreadPump 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateThreadPump
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 99b5766625f2a269d1fb36e9e808c206d0e3040419f505622ccfe1e27ca4bcdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541054"
---
# <a name="d3dx10createthreadpump-function"></a>D3DX10CreateThreadPump 函式

建立執行緒抽取。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX10ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cIoThreads* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要建立的 i/o 執行緒數目。 如果指定0，Direct3D 將會根據硬體設定嘗試計算最佳的執行緒數目。

</dd> <dt>

*cProcThreads* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要建立的進程執行緒數目。 如果指定0，Direct3D 將會根據硬體設定嘗試計算最佳的執行緒數目。

</dd> <dt>

*ppThreadPump* \[擴展\]
</dt> <dd>

類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***

建立的執行緒抽取。 請參閱 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

執行緒抽取是非常耗費資源的物件。 每個應用程式只應建立一個執行緒抽取。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
