---
title: 'ID3DX11EffectVariable GetMemberByIndex 方法 (D3dx11effect .h) '
description: 依索引取得結構成員。
ms.assetid: 256f65aa-5f49-4b83-8dde-ddb6b31c581a
keywords:
- GetMemberByIndex 方法 Direct3D 11
- GetMemberByIndex 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，GetMemberByIndex 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4be490251a83907dcd16231d62d492caf05768f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992258"
---
# <a name="id3dx11effectvariablegetmemberbyindex-method"></a>ID3DX11EffectVariable：： GetMemberByIndex 方法

依索引取得結構成員。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectVariable* GetMemberByIndex(
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

類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。

## <a name="remarks"></a>備註

如果效果變數是結構，請使用這個方法來依索引查閱成員。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

