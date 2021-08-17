---
description: 定義可啟用使用者定義裁剪平面的位模式。 在設定 D3DRS CLIPPLANEENABLE 轉譯狀態的值時，會定義這些宏的便利性 \_ 。
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: 'D3DCLIPPLANEn 宏 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 315f1cdd8f8835b869f04edd9869243f3e05a9c2c9a08a41eeffc014727b3fc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805465"
---
# <a name="d3dclipplanen-macro"></a>D3DCLIPPLANEn 宏

定義可啟用使用者定義裁剪平面的位模式。 在設定 D3DRS CLIPPLANEENABLE 轉譯狀態的值時，會定義這些宏的便利性 \_ 。

## <a name="syntax"></a>語法


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a>參數

這個宏沒有任何參數。

## <a name="return-value"></a>傳回值

這個宏不會傳回值。

## <a name="remarks"></a>備註

當 D3DRS CLIPPLANEENABLE 轉譯狀態中設定的值 \_ 包含一或多個設定的位 (也就是不是 0) 時，會啟用使用者定義的裁剪平面。 轉譯狀態的值並不重要;系統不會將值轉譯為數字。 相反地，此值會啟用對應位已設定的裁剪平面。 Bit 0 控制第一個裁剪平面的狀態 (在索引 0) 、位1第二個平面等等。

您可以使用邏輯 OR 運算來結合這些宏所建立的位模式，以同時啟用多個裁剪平面。 從組合中省略上述其中一個宏，實際上會停用該索引的裁剪平面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[巨集](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




