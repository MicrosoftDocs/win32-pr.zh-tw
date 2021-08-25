---
title: 'ID3DX11EffectVectorVariable 介面 (D3dx11effect .h) '
description: 向量變數介面會存取四個元件的向量。
ms.assetid: 191d373b-0562-4d7b-ac3f-cd24abf259bc
keywords:
- ID3DX11EffectVectorVariable 介面 Direct3D 11
- ID3DX11EffectVectorVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9343659ac249153805e3dfc4c97595957dfbe52bf7be5c498d81f357c66db8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851538"
---
# <a name="id3dx11effectvectorvariable-interface"></a>ID3DX11EffectVectorVariable 介面

向量變數介面會存取四個元件的向量。

## <a name="members"></a>成員

**ID3DX11EffectVectorVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。 **ID3DX11EffectVectorVariable** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11EffectVectorVariable** 介面具有這些方法。



| 方法                                                                         | 描述                                                                         |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**GetBoolVector**](id3dx11effectvectorvariable-getboolvector.md)             | 取得包含布林資料的四個元件向量。<br/>                  |
| [**GetBoolVectorArray**](id3dx11effectvectorvariable-getboolvectorarray.md)   | 取得四個元件向量的陣列，其中包含布林資料。<br/>        |
| [**GetFloatVector**](id3dx11effectvectorvariable-getfloatvector.md)           | 取得包含浮點數據的四個元件向量。<br/>           |
| [**GetFloatVectorArray**](id3dx11effectvectorvariable-getfloatvectorarray.md) | 取得包含浮點數據之四個元件向量的陣列。<br/> |
| [**GetIntVector**](id3dx11effectvectorvariable-getintvector.md)               | 取得包含整數資料的四個元件向量。<br/>                  |
| [**GetIntVectorArray**](id3dx11effectvectorvariable-getintvectorarray.md)     | 取得四個元件向量的陣列，其中包含整數資料。<br/>        |
| [**SetBoolVector**](id3dx11effectvectorvariable-setboolvector.md)             | 設定包含布林資料的四個元件向量。<br/>                  |
| [**SetBoolVectorArray**](id3dx11effectvectorvariable-setboolvectorarray.md)   | 設定包含布林資料之四個元件向量的陣列。<br/>        |
| [**SetFloatVector**](id3dx11effectvectorvariable-setfloatvector.md)           | 設定包含浮點數據的四個元件向量。<br/>           |
| [**SetFloatVectorArray**](id3dx11effectvectorvariable-setfloatvectorarray.md) | 設定包含浮點數據之四個元件向量的陣列。<br/> |
| [**SetIntVector**](id3dx11effectvectorvariable-setintvector.md)               | 設定包含整數資料的四個元件向量。<br/>                  |
| [**SetIntVectorArray**](id3dx11effectvectorvariable-setintvectorarray.md)     | 設定包含整數資料之四個元件向量的陣列。<br/>        |



 

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

 

 





