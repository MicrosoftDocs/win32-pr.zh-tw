---
title: 'ID3DX11Effect GetDesc 方法 (D3dx11effect .h) '
description: 取得效果描述。
ms.assetid: ca684786-c813-48d1-acad-e78aafd1c0db
keywords:
- GetDesc 方法 Direct3D 11
- GetDesc 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetDesc 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587cde43ec2d9136bab5884691c99321d1492835
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992346"
---
# <a name="id3dx11effectgetdesc-method"></a>ID3DX11Effect：： GetDesc 方法

取得效果描述。

## <a name="syntax"></a>語法


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_DESC *pDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDesc* 
</dt> <dd>

類型： **[ **D3DX11 \_ 效果 \_ DESC**](d3dx11-effect-desc.md)\***

效果描述的指標 (查看 [**D3DX11 \_ 效果 \_ DESC**](d3dx11-effect-desc.md)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

效果描述包含效果的基本資訊，例如它所包含的技巧，以及它所需的常數緩衝區資源。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





