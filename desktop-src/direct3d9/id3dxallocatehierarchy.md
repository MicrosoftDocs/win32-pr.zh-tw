---
description: 此介面是由應用程式所執行，以配置或釋放框架和網狀架構的容器物件。 在載入和終結框架階層時，會呼叫此上的方法。
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: 'ID3DXAllocateHierarchy 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035422"
---
# <a name="id3dxallocatehierarchy-interface"></a>ID3DXAllocateHierarchy 介面

此介面是由應用程式所執行，以配置或釋放框架和網狀架構的容器物件。 在載入和終結框架階層時，會呼叫此上的方法。

## <a name="members"></a>成員

**ID3DXAllocateHierarchy** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXAllocateHierarchy** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXAllocateHierarchy** 介面具有這些方法。



| 方法                                                                       | 描述                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**CreateFrame**](id3dxallocatehierarchy--createframe.md)                   | 要求組態架構物件。<br/>            |
| [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md)   | 要求配置網格容器物件。<br/>   |
| [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md)                 | 要求解除配置框架物件。<br/>          |
| [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) | 要求解除配置網格容器物件。<br/> |



 

## <a name="remarks"></a>備註

LPD3DXALLOCATEHIERARCHY 型別定義為這個介面的指標。


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
