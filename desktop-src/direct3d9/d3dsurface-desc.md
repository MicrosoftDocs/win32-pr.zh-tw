---
description: 描述表面。
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: 'D3DSURFACE_DESC 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b18c9cd3428463f82a6e243a57ade3fffd650bb35f2c73234b725fa5bf0607eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300230"
---
# <a name="d3dsurface_desc-structure"></a>D3DSURFACE \_ DESC 結構

描述表面。

## <a name="syntax"></a>語法


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**格式**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

[D3DFORMAT](d3dformat.md)列舉型別的成員，描述介面格式。

</dd> <dt>

**類型**
</dt> <dd>

類型： **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

[**D3DRESOURCETYPE**](./d3dresourcetype.md)列舉型別的成員，將此資源識別為介面。

</dd> <dt>

**使用量**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

可能是 D3DUSAGE \_ DEPTHSTENCIL 或 D3DUSAGE \_ RENDERTARGET 值。 如需詳細資訊，請參閱 [**D3DUSAGE**](d3dusage.md)。

</dd> <dt>

**集區**
</dt> <dd>

類型： **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

[**D3DPOOL**](./d3dpool.md)列舉型別的成員，指定配置給這個介面的記憶體類別。

</dd> <dt>

**MultiSampleType**
</dt> <dd>

類型： **[ **D3DMULTISAMPLE \_ 類型**](./d3dmultisample-type.md)**

</dd> <dd>

[**D3DMULTISAMPLE \_ 型**](./d3dmultisample-type.md)別列舉型別的成員，指定介面所支援的完整場景取樣層級。

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

品質層級。 有效範圍介於零到1之間，且小於 [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)所使用的 pQualityLevels 所傳回的層級。 傳遞較大的值會傳回錯誤，D3DERR \_ INVALIDCALL。 配對轉譯目標、深度樣板表面和多級取樣類型的 MultisampleQuality 值必須全部相符。

</dd> <dt>

**寬度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

介面的寬度（以圖元為單位）。

</dd> <dt>

**高度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

介面的高度（以圖元為單位）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
