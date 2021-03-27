---
title: 'ID3DX11EffectType IsValid 方法 (D3dx11effect .h) '
description: 測試效果類型是否有效。
ms.assetid: 3c1d93a0-92a1-4969-a561-5156e2cd2f3b
keywords:
- IsValid 方法 Direct3D 11
- IsValid 方法 Direct3D 11、ID3DX11EffectType 介面
- ID3DX11EffectType 介面 Direct3D 11，IsValid 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectType.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9254513622ff7c0705c01b0ee15262126c096ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696600"
---
# <a name="id3dx11effecttypeisvalid-method"></a>ID3DX11EffectType：： IsValid 方法

測試效果類型是否有效。

## <a name="syntax"></a>語法


```C++
BOOL IsValid();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

如果有效，則為 **TRUE** ;否則 **為 FALSE**。

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

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

