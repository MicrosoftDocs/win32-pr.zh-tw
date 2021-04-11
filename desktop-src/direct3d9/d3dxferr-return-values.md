---
description: 用來處理 DirectX. x 檔案的方法除了標準的 COM 傳回值之外，還可以傳回下列值。
ms.assetid: b1d04fab-25cb-431d-942e-74092bc9c5c2
title: 'D3DXFERR 傳回值 (D3dx9xof) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFERR
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: cab1cc5e70b6204c832fd9fe5b0fecac4276f578
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116228"
---
# <a name="d3dxferr-return-values"></a>D3DXFERR 傳回值

用來處理 DirectX. x 檔案的方法除了標準的 COM 傳回值之外，還可以傳回下列值。

<dl> <dt>

<span id="D3DXFERR_BADARRAYSIZE"></span><span id="d3dxferr_badarraysize"></span>**D3DXFERR \_ BADARRAYSIZE**
</dt> <dd>

陣列超過允許的大小。

</dd> <dt>

<span id="D3DXFERR_BADCACHEFILE"></span><span id="d3dxferr_badcachefile"></span>**D3DXFERR \_ BADCACHEFILE**
</dt> <dd>

無法讀取快取檔案。

</dd> <dt>

<span id="D3DXFERR_BADDataReference"></span><span id="d3dxferr_baddatareference"></span><span id="D3DXFERR_BADDATAREFERENCE"></span>**D3DXFERR \_ BADDataReference**
</dt> <dd>

無法取出範本成員資料。

</dd> <dt>

<span id="D3DXFERR_BADFILE"></span><span id="d3dxferr_badfile"></span>**D3DXFERR \_ BADFILE**
</dt> <dd>

檔案讀取或寫入作業失敗。

</dd> <dt>

<span id="D3DXFERR_BADFILEFLOATSIZE"></span><span id="d3dxferr_badfilefloatsize"></span>**D3DXFERR \_ BADFILEFLOATSIZE**
</dt> <dd>

檔案不是預期的大小。

</dd> <dt>

<span id="D3DXFERR_BADFILETYPE"></span><span id="d3dxferr_badfiletype"></span>**D3DXFERR \_ BADFILETYPE**
</dt> <dd>

檔案的格式無效。

</dd> <dt>

<span id="D3DXFERR_BADFILEVERSION"></span><span id="d3dxferr_badfileversion"></span>**D3DXFERR \_ BADFILEVERSION**
</dt> <dd>

檔案的格式版本無效。

</dd> <dt>

<span id="D3DXFERR_BADOBJECT"></span><span id="d3dxferr_badobject"></span>**D3DXFERR \_ BADOBJECT**
</dt> <dd>

無法讀取或寫入物件的資料。

</dd> <dt>

<span id="D3DXFERR_BADRESOURCE"></span><span id="d3dxferr_badresource"></span>**D3DXFERR \_ BADRESOURCE**
</dt> <dd>

資源上的作業失敗。

</dd> <dt>

<span id="D3DXFERR_BADTYPE"></span><span id="d3dxferr_badtype"></span>**D3DXFERR \_ BADTYPE**
</dt> <dd>

檔案不符合已知的範本類型。

</dd> <dt>

<span id="D3DXFERR_BADVALUE"></span><span id="d3dxferr_badvalue"></span>**D3DXFERR \_ BADVALUE**
</dt> <dd>

變數超出預期的範圍;通常會在物件指標無效時傳回。

</dd> <dt>

<span id="D3DXFERR_FILENOTFOUND"></span><span id="d3dxferr_filenotfound"></span>**D3DXFERR \_ FILENOTFOUND**
</dt> <dd>

找不到指定檔案的有效控制碼。

</dd> <dt>

<span id="D3DXFERR_NOMOREDATA"></span><span id="d3dxferr_nomoredata"></span>**D3DXFERR \_ NOMOREDATA**
</dt> <dd>

指標位移延伸超過緩衝區的結尾。

</dd> <dt>

<span id="D3DXFERR_NOMOREOBJECTS"></span><span id="d3dxferr_nomoreobjects"></span>**D3DXFERR \_ NOMOREOBJECTS**
</dt> <dd>

沒有其他可用的子物件。

</dd> <dt>

<span id="D3DXFERR_NOTDONEYET"></span><span id="d3dxferr_notdoneyet"></span>**D3DXFERR \_ NOTDONEYET**
</dt> <dd>

資料類型不符合允許的類型。

</dd> <dt>

<span id="D3DXFERR_NOTFOUND"></span><span id="d3dxferr_notfound"></span>**D3DXFERR \_ NOTFOUND**
</dt> <dd>

在指定的參數中找不到物件。

</dd> <dt>

<span id="D3DXFERR_PARSEERROR"></span><span id="d3dxferr_parseerror"></span>**D3DXFERR \_ PARSEERROR**
</dt> <dd>

資料流程無法剖析。

</dd> <dt>

<span id="D3DXFERR_RESOURCENOTFOUND"></span><span id="d3dxferr_resourcenotfound"></span>**D3DXFERR \_ RESOURCENOTFOUND**
</dt> <dd>

找不到指定資源的有效控制碼。

</dd> </dl>

## <a name="remarks"></a>備註

. X 檔案錯誤設備程式碼 \_ FACD3DXF 可用來產生錯誤碼。 例如：


```
#define _FACD3DXF           0x876
#define D3DXFERR_BADOBJECT  MAKE_HRESULT( 1, _FACD3DXF, 900 )
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9xof。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX X 檔案常數](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> </dl>

 

 




