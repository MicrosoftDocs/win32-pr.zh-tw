---
title: 'ID3DX11Effect GetConstantBufferByName 方法 (D3dx11effect .h) '
description: 依名稱取得常數緩衝區。
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- GetConstantBufferByName 方法 Direct3D 11
- GetConstantBufferByName 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetConstantBufferByName 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa01d20bfeebfa3f689a58aae5c5face8b879e3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854056"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a>ID3DX11Effect：： GetConstantBufferByName 方法

依名稱取得常數緩衝區。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* 
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

常數緩衝區名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

名稱所表示之常數緩衝區的指標。 請參閱 [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)。

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

 

