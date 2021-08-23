---
title: 'ID3DX11EffectType GetMemberTypeBySemantic 方法 (D3dx11effect .h) '
description: 依語義取得成員類型。
ms.assetid: d5fea2d9-8d08-4e02-a9c6-dbcfaaf4a7d1
keywords:
- GetMemberTypeBySemantic 方法 Direct3D 11
- GetMemberTypeBySemantic 方法 Direct3D 11，ID3DX11EffectType 介面
- ID3DX11EffectType 介面 Direct3D 11，GetMemberTypeBySemantic 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e1add6ddc485f803512050795b9ba240f2a29d145fb01e864b88bc8ba84ee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532330"
---
# <a name="id3dx11effecttypegetmembertypebysemantic-method"></a>ID3DX11EffectType：： GetMemberTypeBySemantic 方法

依語義取得成員類型。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectType* GetMemberTypeBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*語義* 
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

語義。

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

 

