---
title: 'ID3DX11EffectScalarVariable 介面 (D3dx11effect .h) '
description: 效果純量變數介面會存取純量值。
ms.assetid: 52e3b856-aa1b-4ed2-b140-7ae96ec1c94b
keywords:
- ID3DX11EffectScalarVariable 介面 Direct3D 11
- ID3DX11EffectScalarVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a33445045d463591659902a4d599deddb3b33f092ef646df736d72db501fde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408148"
---
# <a name="id3dx11effectscalarvariable-interface"></a>ID3DX11EffectScalarVariable 介面

效果純量變數介面會存取純量值。

## <a name="members"></a>成員

**ID3DX11EffectScalarVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。 **ID3DX11EffectScalarVariable** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11EffectScalarVariable** 介面具有這些方法。



| 方法                                                             | 描述                                          |
|:-------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBool**](id3dx11effectscalarvariable-getbool.md)             | 取得布林值變數。<br/>                   |
| [**GetBoolArray**](id3dx11effectscalarvariable-getboolarray.md)   | 取得布林值變數的陣列。<br/>        |
| [**GetFloat**](id3dx11effectscalarvariable-getfloat.md)           | 取得浮點數變數。<br/>            |
| [**GetFloatArray**](id3dx11effectscalarvariable-getfloatarray.md) | 取得浮點數變數的陣列。<br/> |
| [**GetInt**](id3dx11effectscalarvariable-getint.md)               | 取得整數變數。<br/>                  |
| [**GetIntArray**](id3dx11effectscalarvariable-getintarray.md)     | 取得整數變數的陣列。<br/>        |
| [**SetBool**](id3dx11effectscalarvariable-setbool.md)             | 設定布林值變數。<br/>                   |
| [**SetBoolArray**](id3dx11effectscalarvariable-setboolarray.md)   | 設定布林值變數的陣列。<br/>        |
| [**SetFloat**](id3dx11effectscalarvariable-setfloat.md)           | 設定浮點變數。<br/>            |
| [**SetFloatArray**](id3dx11effectscalarvariable-setfloatarray.md) | 設定浮點變數的陣列。<br/> |
| [**SetInt**](id3dx11effectscalarvariable-setint.md)               | 設定整數變數。<br/>                  |
| [**SetIntArray**](id3dx11effectscalarvariable-setintarray.md)     | 設定整數變數的陣列。<br/>        |



 

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

 

 





