---
title: 'ID3DX11EffectPass ComputeStateBlockMask 方法 (D3dx11effect .h) '
description: 產生遮罩以允許/防止狀態變更。
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- ComputeStateBlockMask 方法 Direct3D 11
- ComputeStateBlockMask 方法 Direct3D 11，ID3DX11EffectPass 介面
- ID3DX11EffectPass 介面 Direct3D 11，ComputeStateBlockMask 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17198c076d200631142207189059ada425e9ec1ddf6e3c8a8d40499e40aa21a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535054"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a>ID3DX11EffectPass：： ComputeStateBlockMask 方法

產生遮罩以允許/防止狀態變更。

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





