---
description: 將相鄰資料新增至網格的索引緩衝區。 當網格要傳送至採用相鄰資料的幾何著色器時，網格的索引緩衝區必須包含相鄰資料。
ms.assetid: 8e587620-a4b6-4415-8fe7-9ec22f253b16
title: 'ID3DX10Mesh：： GenerateGSAdjacency 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateGSAdjacency
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3bd6fdcfac53ca4655cc85e0d4373ee862f92f9bad673ed5bb20210ab9b77ca1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566878"
---
# <a name="id3dx10meshgenerategsadjacency-method"></a>ID3DX10Mesh：： GenerateGSAdjacency 方法

將相鄰資料新增至網格的索引緩衝區。 當網格要傳送至採用相鄰資料的幾何著色器時，網格的索引緩衝區必須包含相鄰資料。

## <a name="syntax"></a>語法


```C++
HRESULT GenerateGSAdjacency();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




