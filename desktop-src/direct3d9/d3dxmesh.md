---
description: D3DXMESH 列舉旗標，用來指定網格的建立選項。
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: 'D3DXMESH 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESH
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6b83389ae4d92027245877e24e01621f0d93f123dee9ff4f040586b3e7c5111d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525267"
---
# <a name="d3dxmesh-enumeration"></a>D3DXMESH 列舉

用來指定網格之建立選項的旗標。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXMESH { 
  D3DXMESH_32BIT                  = 0x001,
  D3DXMESH_DONOTCLIP              = 0x002,
  D3DXMESH_POINTS                 = 0x004,
  D3DXMESH_RTPATCHES              = 0x008,
  D3DXMESH_NPATCHES               = 0x4000,
  D3DXMESH_VB_SYSTEMMEM           = 0x010,
  D3DXMESH_VB_MANAGED             = 0x020,
  D3DXMESH_VB_WRITEONLY           = 0x040,
  D3DXMESH_VB_DYNAMIC             = 0x080,
  D3DXMESH_VB_SOFTWAREPROCESSING  = 0x8000,
  D3DXMESH_IB_SYSTEMMEM           = 0x100,
  D3DXMESH_IB_MANAGED             = 0x200,
  D3DXMESH_IB_WRITEONLY           = 0x400,
  D3DXMESH_IB_DYNAMIC             = 0x800,
  D3DXMESH_IB_SOFTWAREPROCESSING  = 0x10000,
  D3DXMESH_VB_SHARE               = 0x1000,
  D3DXMESH_USEHWONLY              = 0x2000,
  D3DXMESH_SYSTEMMEM              = 0x110,
  D3DXMESH_MANAGED                = 0x220,
  D3DXMESH_WRITEONLY              = 0x440,
  D3DXMESH_DYNAMIC                = 0x880,
  D3DXMESH_SOFTWAREPROCESSING     = 0x18000
} D3DXMESH, *LPD3DXMESH;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32 位**
</dt> <dd>

網格有32位的索引，而不是16位的索引。 請參閱＜備註＞。

</dd> <dt>

<span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**
</dt> <dd>

針對頂點和索引緩衝區使用 [**D3DUSAGE \_ DONOTCLIP**](d3dusage.md) usage 旗標。

</dd> <dt>

<span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH \_ 點**
</dt> <dd>

針對頂點和索引緩衝區使用 [**D3DUSAGE \_ 點**](d3dusage.md) 使用方式旗標。

</dd> <dt>

<span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**
</dt> <dd>

針對頂點和索引緩衝區使用 [**D3DUSAGE \_ RTPATCHES**](d3dusage.md) usage 旗標。

</dd> <dt>

<span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ NPATCHES**
</dt> <dd>

指定此旗標會讓網格的頂點和索引緩衝區以 [**D3DUSAGE \_ NPATCHES**](d3dusage.md) 旗標建立。 如果要使用 Direct3D 以 N 修補程式增強功能來呈現網格物件，則這是必要的。

</dd> <dt>

<span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**
</dt> <dd>

針對頂點緩衝區使用 [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) usage 旗標。

</dd> <dt>

<span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ VB \_ 受控**
</dt> <dd>

針對頂點緩衝區使用 [**D3DPOOL \_ 受控**](./d3dpool.md) 使用旗標。

</dd> <dt>

<span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**
</dt> <dd>

針對頂點緩衝區使用 [**D3DUSAGE \_ WRITEONLY**](d3dusage.md) 使用旗標。

</dd> <dt>

<span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ 動態**
</dt> <dd>

針對頂點緩衝區使用 [**D3DUSAGE \_ 動態**](d3dusage.md) 使用旗標。

</dd> <dt>

<span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**
</dt> <dd>

針對頂點緩衝區使用 [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) usage 旗標。

</dd> <dt>

<span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**
</dt> <dd>

使用索引緩衝區的 [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) usage 旗標。

</dd> <dt>

<span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ 管理**
</dt> <dd>

使用索引緩衝區的 [**D3DPOOL \_ 受控**](./d3dpool.md) 使用旗標。

</dd> <dt>

<span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**
</dt> <dd>

使用索引緩衝區的 [**D3DUSAGE \_ WRITEONLY**](d3dusage.md) 使用旗標。

</dd> <dt>

<span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ 動態**
</dt> <dd>

使用索引緩衝區的 [**D3DUSAGE \_ 動態**](d3dusage.md) 使用旗標。

</dd> <dt>

<span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB \_ SOFTWAREPROCESSING**
</dt> <dd>

使用索引緩衝區的 [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) usage 旗標。

</dd> <dt>

<span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH \_ VB \_ 共用**
</dt> <dd>

強制複製的網格共用頂點緩衝區。

</dd> <dt>

<span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**
</dt> <dd>

只使用硬體處理。 若為混合模式裝置，此旗標將會導致系統使用硬體 (（如果硬體) 支援）或預設為軟體處理。

</dd> <dt>

<span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**
</dt> <dd>

相當於同時指定 D3DXMESH \_ VB \_ SYSTEMMEM 和 D3DXMESH \_ IB \_ SYSTEMMEM。

</dd> <dt>

<span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH \_ 受控**
</dt> <dd>

相當於指定 D3DXMESH \_ VB \_ managed 和 D3DXMESH \_ IB \_ managed。

</dd> <dt>

<span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**
</dt> <dd>

相當於同時指定 D3DXMESH \_ VB \_ WRITEONLY 和 D3DXMESH \_ IB \_ WRITEONLY。

</dd> <dt>

<span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ 動態**
</dt> <dd>

相當於同時指定 D3DXMESH \_ VB \_ 動態和 D3DXMESH \_ IB \_ 動態。

</dd> <dt>

<span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ SOFTWAREPROCESSING**
</dt> <dd>

相當於同時指定 D3DXMESH \_ VB \_ SOFTWAREPROCESSING 和 D3DXMESH \_ IB \_ SOFTWAREPROCESSING。

</dd> </dl>

## <a name="remarks"></a>備註

32位網格 (D3DXMESH 32 位 \_) 理論上可支援 (2 ^ 32) -1 臉部和頂點。 不過，為在32位作業系統上大的網狀架構配置記憶體並不實用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
