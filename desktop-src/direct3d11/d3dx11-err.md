---
title: 'D3DX11_ERR 列舉 (D3DX11 .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 錯誤會以負數值表示，而且無法合併。
ms.assetid: d042621d-a20b-4945-b6aa-714a451aa88a
keywords:
- D3DX11_ERR 列舉 Direct3D 11
- LPD3DX11_ERR 列舉指標 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_ERR
api_location:
- D3DX11.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d80b906b5b95693458eeea353f40fe446a22e8e33a6011b7851cf6d9663b3ed4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729318"
---
# <a name="d3dx11_err-enumeration"></a>D3DX11 \_ ERR 列舉

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。

 

錯誤會以負數值表示，而且無法合併。 以下是 D3DX 公用程式程式庫隨附的方法可傳回的值清單。 如需每個可傳回值的清單，請參閱個別的方法描述。 這些清單不一定完整。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_ERR { 
  D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX11_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX11_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX11_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX11_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX11_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX11_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX11_ERR, *LPD3DX11_ERR;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11 \_ ERR \_ 無法 \_ 修改 \_ 索引 \_ 緩衝區**
</dt> <dd>

無法修改索引緩衝區。

</dd> <dt>

<span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11 \_ 錯誤 \_ 無效 \_ 網格**
</dt> <dd>

網格無效。

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11 \_ ERR \_ 無法 \_ \_ 進行 ATTR 排序**
</dt> <dd>

屬性排序 (D3DXMESHOPT \_ ATTRSORT) 不支援做為優化技術。

</dd> <dt>

<span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**\_ \_ \_ 不支援 D3DX11 錯誤的外觀 \_**
</dt> <dd>

不支援 [外觀]。

</dd> <dt>

<span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11 \_ 錯誤 \_ 太 \_ 多 \_ 影響**
</dt> <dd>

指定了太多影響。

</dd> <dt>

<span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11 \_ 錯誤 \_ 的 \_ 資料無效**
</dt> <dd>

資料無效。

</dd> <dt>

<span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**D3DX11 \_ 錯誤 \_ 載入 \_ 網格 \_ \_ 沒有任何 \_ 資料**
</dt> <dd>

網格沒有任何資料。

</dd> <dt>

<span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11 \_ 錯誤的 \_ 重複 \_ 命名 \_ 片段**
</dt> <dd>

具有該名稱的片段已經存在。

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11 \_ ERR \_ 無法 \_ 移除 \_ 最後一個 \_ 專案**
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
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX11。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





