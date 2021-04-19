---
description: 使用 ID3DX10Mesh：： CommitToDevice) ，從已認可至裝置 (的裝置移除網格資料。
ms.assetid: 60eee1f8-f04b-4f33-8f86-0564d0334f97
title: 'ID3DX10Mesh：:D iscard 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Discard
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f861de8eefff603954e896a1b6684afc8806764f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991466"
---
# <a name="id3dx10meshdiscard-method"></a>ID3DX10Mesh：:D iscard 方法

使用 [**ID3DX10Mesh：： CommitToDevice**](id3dx10mesh-committodevice.md)) ，從已認可至裝置 (的裝置移除網格資料。

## <a name="syntax"></a>語法


```C++
HRESULT Discard(
  [in] D3DX10_MESH_DISCARD_FLAGS dwDiscard
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwDiscard* \[在\]
</dt> <dd>

類型： **[ **D3DX10 \_ 網格 \_ 捨棄 \_ 旗標**](d3dx10-mesh-discard-flags.md)**

指定要從裝置捨棄哪些網格資料片段。 請參閱 [**D3DX10 \_ 網格 \_ 捨棄 \_ 旗標**](d3dx10-mesh-discard-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




