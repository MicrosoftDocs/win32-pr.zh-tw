---
description: 複製或複製動畫控制器。
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: 'ID3DXAnimationController：： CloneAnimationController 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5afb99126967163318c82bac6b8cac655fec65e8a28e4cdb349c7f2b1c679435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522779"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a>ID3DXAnimationController：： CloneAnimationController 方法

複製或複製動畫控制器。

## <a name="syntax"></a>語法


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MaxNumAnimationOutputs* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

控制器可支援的動畫輸出數目上限。

</dd> <dt>

*MaxNumAnimationSets* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

控制器可支援的動畫組數目上限。

</dd> <dt>

*MaxNumTracks* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

控制器可支援的最大追蹤數目。

</dd> <dt>

*MaxNumEvents* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

控制器可支援的事件數目上限。

</dd> <dt>

*ppAnimController* \[在\]
</dt> <dd>

類型： **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

複製之 [**ID3DXAnimationController**](id3dxanimationcontroller.md) 動畫控制器指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
