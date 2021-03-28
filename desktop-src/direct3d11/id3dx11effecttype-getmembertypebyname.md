---
title: 'ID3DX11EffectType GetMemberTypeByName 方法 (D3dx11effect .h) '
description: 依名稱取得成員類型。
ms.assetid: 0c5a732b-7c3a-41da-b7de-dc464eed814a
keywords:
- GetMemberTypeByName 方法 Direct3D 11
- GetMemberTypeByName 方法 Direct3D 11，ID3DX11EffectType 介面
- ID3DX11EffectType 介面 Direct3D 11，GetMemberTypeByName 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e573bcdc2dc4470e87539a307cdc38b71a6320ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992174"
---
# <a name="id3dx11effecttypegetmembertypebyname-method"></a>ID3DX11EffectType：： GetMemberTypeByName 方法

依名稱取得成員類型。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectType* GetMemberTypeByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* 
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

成員的名稱。

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

 

