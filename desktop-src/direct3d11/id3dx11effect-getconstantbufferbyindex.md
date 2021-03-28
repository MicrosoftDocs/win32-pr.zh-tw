---
title: 'ID3DX11Effect GetConstantBufferByIndex 方法 (D3dx11effect .h) '
description: 依索引取得常數緩衝區。
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- GetConstantBufferByIndex 方法 Direct3D 11
- GetConstantBufferByIndex 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetConstantBufferByIndex 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbc44b2d9ceea1bcfbf854a8d3c6998d03e3eec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974660"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a>ID3DX11Effect：： GetConstantBufferByIndex 方法

依索引取得常數緩衝區。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByIndex(
   UINT Index
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Index* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

以零為基底的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

指向 [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)的指標。

## <a name="remarks"></a>備註

包含將由應用程式讀取/寫入之變數的效果，必須至少有一個常數緩衝區。 為了達到最佳效能，效果應該根據更新的頻率，將變數組織成一或多個常數緩衝區。

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

 

