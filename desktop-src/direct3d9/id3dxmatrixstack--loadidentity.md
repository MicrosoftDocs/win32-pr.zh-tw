---
description: ID3DXMATRIXStack：： LoadIdentity 方法 (D3dx9math .h) -在目前的矩陣中載入身分識別。
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: 'ID3DXMATRIXStack：： LoadIdentity 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadIdentity
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 046267b11f1a2aa977eda7f5fe461e5c44a2cf59e1f50ae291cf714f063088c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847738"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a>ID3DXMATRIXStack：： LoadIdentity 方法 (D3dx9math .h) 

在目前的矩陣中載入識別。

## <a name="syntax"></a>語法


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

身分識別矩陣是矩陣，其中所有係數都是0.0，但 \[ 1、1 \] \[ 2、2 \] \[ 3、3 \] \[ 4、4 \] 係數會設定為1.0。 識別矩陣的特殊之處，就是當它套用至頂點時，不會變更。 身分識別矩陣可作為矩陣的起點，以修改頂點值以建立旋轉、轉譯，以及可由4x4 矩陣表示的任何其他轉換。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::LoadMatrix**](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




