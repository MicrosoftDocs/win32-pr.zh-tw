---
title: 'ID3DX11EffectType GetMemberTypeByIndex 方法 (D3dx11effect .h) '
description: 依索引取得成員類型。
ms.assetid: 6421f08f-0236-4d8f-b3c2-ef7ec5ffe2a1
keywords:
- GetMemberTypeByIndex 方法 Direct3D 11
- GetMemberTypeByIndex 方法 Direct3D 11，ID3DX11EffectType 介面
- ID3DX11EffectType 介面 Direct3D 11，GetMemberTypeByIndex 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5023e064539f57af9998c788385f2a1316433f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514637"
---
# <a name="id3dx11effecttypegetmembertypebyindex-method"></a>ID3DX11EffectType：： GetMemberTypeByIndex 方法

依索引取得成員類型。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectType* GetMemberTypeByIndex(
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

類型： **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***

[**ID3DX11EffectType**](id3dx11effecttype.md)的指標。

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

 

