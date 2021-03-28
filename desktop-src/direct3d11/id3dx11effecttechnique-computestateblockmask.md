---
title: 'ID3DX11EffectTechnique ComputeStateBlockMask 方法 (D3dx11effect .h) '
description: 計算狀態欄塊遮罩以允許/防止狀態變更。
ms.assetid: 4fd6061d-6ca5-4e3f-b031-fae98f3de057
keywords:
- ComputeStateBlockMask 方法 Direct3D 11
- ComputeStateBlockMask 方法 Direct3D 11，ID3DX11EffectTechnique 介面
- ID3DX11EffectTechnique 介面 Direct3D 11，ComputeStateBlockMask 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d15a159c15f35d530559b4ad6d84dd815e5964a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196203"
---
# <a name="id3dx11effecttechniquecomputestateblockmask-method"></a>ID3DX11EffectTechnique：： ComputeStateBlockMask 方法

計算狀態欄塊遮罩以允許/防止狀態變更。

## <a name="syntax"></a>語法


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStateBlockMask* 
</dt> <dd>

類型： **[ **D3DX11 \_ 狀態 \_ 區塊 \_ 遮罩**](d3dx11-state-block-mask.md)\***

狀態欄塊遮罩的指標 (參閱 [**D3DX11 \_ 狀態 \_ 區塊 \_ 遮罩**](d3dx11-state-block-mask.md)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。

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

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

 





