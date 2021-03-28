---
title: 'ID3DX11EffectVariable IsValid 方法 (D3dx11effect .h) '
description: 比較資料類型與儲存的資料。
ms.assetid: 3384afa3-6ae5-4c7c-b95d-4fe3c87cc2fe
keywords:
- IsValid 方法 Direct3D 11
- IsValid 方法 Direct3D 11、ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，IsValid 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5136005e675a6f5e54cc3863ef2d80ffadfb7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992349"
---
# <a name="id3dx11effectvariableisvalid-method"></a>ID3DX11EffectVariable：： IsValid 方法

比較資料類型與儲存的資料。

## <a name="syntax"></a>語法


```C++
BOOL IsValid();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

如果語法有效，則 **為 TRUE** ;否則 **為 FALSE**。

## <a name="remarks"></a>備註

這個方法會檢查資料類型是否符合將某個介面轉換成 (另一個介面之後所儲存的資料，) 使用任何 As 方法。

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

 

