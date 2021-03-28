---
title: 'ID3DX11EffectVariable GetMemberByName 方法 (D3dx11effect .h) '
description: 依名稱取得結構成員。
ms.assetid: 09f7f2f8-f55f-411c-8130-6ae44015d58a
keywords:
- GetMemberByName 方法 Direct3D 11
- GetMemberByName 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，GetMemberByName 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9851a2f74502a79b5cc85c494e468c4a346798f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992385"
---
# <a name="id3dx11effectvariablegetmemberbyname-method"></a>ID3DX11EffectVariable：： GetMemberByName 方法

依名稱取得結構成員。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectVariable* GetMemberByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* 
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

成員名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。

## <a name="remarks"></a>備註

如果效果變數是結構，請使用這個方法來依名稱查詢成員。

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

 

