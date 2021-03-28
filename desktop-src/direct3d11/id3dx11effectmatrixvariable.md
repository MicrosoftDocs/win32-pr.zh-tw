---
title: 'ID3DX11EffectMatrixVariable 介面 (D3dx11effect .h) '
description: 矩陣變數介面會存取矩陣。
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- ID3DX11EffectMatrixVariable 介面 Direct3D 11
- ID3DX11EffectMatrixVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5c4c89a231d429fc0a1f8fecbcbb4d06db35cb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974621"
---
# <a name="id3dx11effectmatrixvariable-interface"></a>ID3DX11EffectMatrixVariable 介面

矩陣變數介面會存取矩陣。

## <a name="members"></a>成員

**ID3DX11EffectMatrixVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。 **ID3DX11EffectMatrixVariable** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11EffectMatrixVariable** 介面具有這些方法。



| 方法                                                                                 | 描述                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**GetMatrix**](id3dx11effectmatrixvariable-getmatrix.md)                             | 取得矩陣。<br/>                                          |
| [**GetMatrixArray**](id3dx11effectmatrixvariable-getmatrixarray.md)                   | 取得矩陣的陣列。<br/>                              |
| [**GetMatrixTranspose**](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | 調換和取得浮點數矩陣。<br/>             |
| [**GetMatrixTransposeArray**](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | 調換和取得浮點數矩陣的陣列。<br/> |
| [**SetMatrix**](id3dx11effectmatrixvariable-setmatrix.md)                             | 設定浮點數矩陣。<br/>                           |
| [**SetMatrixArray**](id3dx11effectmatrixvariable-setmatrixarray.md)                   | 設定浮點數矩陣的陣列。<br/>               |
| [**SetMatrixTranspose**](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | 變換並設定浮點數矩陣。<br/>             |
| [**SetMatrixTransposeArray**](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | 變換並設定浮點數矩陣的陣列。<br/> |



 

## <a name="remarks"></a>備註

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[效果11介面](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





