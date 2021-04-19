---
description: 指定要執行的網格優化類型。
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: 'D3DXMESHOPT 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7d4f9f4ae36cec74ea86fcb50a194ac66d0add7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986090"
---
# <a name="d3dxmeshopt-enumeration"></a>D3DXMESHOPT 列舉

指定要執行的網格優化類型。

## <a name="syntax"></a>Syntax


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ COMPACT**
</dt> <dd>

重新排序臉部以移除未使用的頂點和臉部。

</dd> <dt>

<span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**
</dt> <dd>

重新排列臉部以針對較少的屬性套件組合狀態變更和增強的 ID3DXBaseMesh 進行優化 [**：:D rawsubset**](id3dxbasemesh--drawsubset.md) 效能。

</dd> <dt>

<span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**
</dt> <dd>

重新排列臉部以增加頂點快取的快取點擊率。

</dd> <dt>

<span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**
</dt> <dd>

重新排列臉部以將相鄰三角形的最大長度重新排序。

</dd> <dt>

<span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**
</dt> <dd>

僅將臉部優化;請勿將頂點優化。

</dd> <dt>

<span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**
</dt> <dd>

屬性排序時，請勿分割屬性群組之間共用的頂點。

</dd> <dt>

<span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ DEVICEINDEPENDENT**
</dt> <dd>

影響頂點快取大小。 使用此旗標可指定在舊版硬體上運作正常的預設頂點快取大小。

</dd> </dl>

## <a name="remarks"></a>備註

D3DXMESHOPT \_ STRIPREORDER 和 D3DXMESHOPT \_ VERTEXCACHE 優化旗標彼此互斥。

\_此列舉已移除 D3DXMESHOPT SHAREVB 旗標。 \_ \_ 在 [**D3DXMESH**](./d3dxmesh.md)中，請改用 D3DXMESH VB SHARE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
