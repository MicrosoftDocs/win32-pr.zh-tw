---
description: 錯誤會以負數值表示，而且無法合併。
ms.assetid: 2318278e-e1e1-4cd8-a5ce-5c99f3bc47ba
title: 'D3DXERR 列舉 (D3dx9) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXERR
api_type:
- HeaderDef
api_location:
- d3dx9.h
ms.openlocfilehash: 0d4ef0fddf70effd63a0fcdc42b46889a879c13a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196261"
---
# <a name="d3dxerr-enumeration"></a>D3DXERR 列舉

錯誤會以負數值表示，而且無法合併。 以下是 D3DX 公用程式程式庫隨附的方法可傳回的值清單。 如需每個可傳回值的清單，請參閱個別的方法描述。 這些清單不一定完整。

## <a name="syntax"></a>Syntax


```C++
enum _D3DXERR {
  D3DXERR_CANNOTMODIFYINDEXBUFFER, 
  D3DXERR_INVALIDMESH, 
  D3DXERR_CANNOTATTRSORT, 
  D3DXERR_SKINNINGNOTSUPPORTED, 
  D3DXERR_TOOMANYINFLUENCES, 
  D3DXERR_INVALIDDATA, 
  D3DXERR_LOADEDMESHASNODATA, 
  D3DXERR_DUPLICATENAMEDFRAGMENT, 
  D3DXERR_CANNOTREMOVELASTITEM 

};
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR \_ CANNOTMODIFYINDEXBUFFER**
</dt> <dd>

無法修改索引緩衝區。

</dd> <dt>

<span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR \_ INVALIDMESH**
</dt> <dd>

網格無效。

</dd> <dt>

<span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR \_ CANNOTATTRSORT**
</dt> <dd>

屬性排序 (D3DXMESHOPT \_ ATTRSORT) 不支援做為優化技術。

</dd> <dt>

<span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR \_ SKINNINGNOTSUPPORTED**
</dt> <dd>

不支援 [外觀]。

</dd> <dt>

<span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR \_ TOOMANYINFLUENCES**
</dt> <dd>

指定了太多影響。

</dd> <dt>

<span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR \_ INVALIDDATA**
</dt> <dd>

資料無效。

</dd> <dt>

<span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR \_ LOADEDMESHASNODATA**
</dt> <dd>

網格沒有任何資料。

</dd> <dt>

<span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR \_ DUPLICATENAMEDFRAGMENT**
</dt> <dd>

具有該名稱的片段已經存在。

</dd> <dt>

<span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR \_ CANNOTREMOVELASTITEM**
</dt> <dd>

無法刪除最後一個專案。

</dd> </dl>

## <a name="remarks"></a>備註

設備碼 \_ FACDD 可用來產生錯誤碼，如下列宏所示。


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




