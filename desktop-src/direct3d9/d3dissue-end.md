---
description: 此宏會建立問題用來發出查詢結束的值。
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: 'D3DISSUE_END (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 0c2e7a197612b56eb5ae966da3cd4cc224edd2bd07e3fded3d0b72907f717d5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987248"
---
# <a name="d3dissue_end"></a>D3DISSUE \_ 結束

此宏會建立 [**問題**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) 用來發出查詢結束的值。

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a>參數





 

## <a name="remarks"></a>備註

此宏會將查詢狀態變更為未收到信號。

D3DISSUE \_ END 對下列查詢類型有效。

-   D3DQUERYTYPE \_ VCACHE
-   D3DQUERYTYPE \_ ResourceManager
-   D3DQUERYTYPE \_ VERTEXSTATS
-   D3DQUERYTYPE \_ 事件
-   D3DQUERYTYPE \_ 遮蔽

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[巨集](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DISSUE \_ 開始**](d3dissue-begin.md)
</dt> <dt>

[**D3DQUERYTYPE**](./d3dquerytype.md)
</dt> </dl>

 

 
