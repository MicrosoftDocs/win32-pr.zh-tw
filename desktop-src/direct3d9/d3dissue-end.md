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
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323011"
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

 

 
