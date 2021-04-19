---
description: 建立新的網格，並將其填入先前載入之網格的資料。
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'ID3DX10Mesh：： CloneMesh 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0f007475ea9f6aeaa6dc0c01bbd721c4a5103adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991971"
---
# <a name="id3dx10meshclonemesh-method"></a>ID3DX10Mesh：： CloneMesh 方法

建立新的網格，並將其填入先前載入之網格的資料。

## <a name="syntax"></a>語法


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要套用至新網格的建立旗標。 請參閱 [**D3DX10 \_ 網格**](d3dx10-mesh.md)。

</dd> <dt>

*pPosSemantic* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

位置資料的語義名稱。

</dd> <dt>

*pDesc* \[在\]
</dt> <dd>

Type： **Const [**D3D10 \_ INPUT \_ ELEMENT \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

D3D10 \_ 輸入 \_ 元素 \_ DESC 結構的陣列，描述傳回之網格的頂點格式。 請參閱 [**D3D10 \_ 輸入 \_ 元素 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)。

</dd> <dt>

*DeclCount* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

PDesc 陣列中的元素數目。

</dd> <dt>

*ppCloneMesh* \[擴展\]
</dt> <dd>

類型： **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

新的網格。

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

 

 
