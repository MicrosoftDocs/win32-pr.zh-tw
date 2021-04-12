---
description: 此資料表會將 D3DVERTEXELEMENT9 宣告的成員對應至 FVF 碼。
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: 'Direct3D 宣告與 FVF 碼之間的對應 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4831af7b8c03ae4abd5ac2847351d2a6c921fb97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109153"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a>Direct3D 宣告與 FVF 碼之間的對應 (Direct3D 9) 

此資料表會將 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 宣告的成員對應至 FVF 碼。



| 資料類型             | 使用方式                      | 使用方式索引 | FVF                       |
|-----------------------|----------------------------|-------------|---------------------------|
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ 位置     | 0           | D3DFVF \_ XYZ               |
| D3DDECLTYPE \_ FLOAT4   | D3DDECLUSAGE \_ POSITIONT    | 0           | D3DFVF \_ XYZRHW            |
| D3DDECLTYPE \_ FLOATn   | D3DDECLUSAGE \_ BLENDWEIGHT  | 0           | D3DFVF \_ XYZBn             |
| D3DDECLTYPE \_ UBYTE4   | D3DDECLUSAGE \_ BLENDINDICES | 0           | D3DFVF \_ XYZB (nWeights + 1)  |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ 正常       | 0           | D3DFVF \_ 正常            |
| D3DDECLTYPE \_ FLOAT1   | D3DDECLUSAGE \_ PSIZE        | 0           | D3DFVF \_ PSIZE             |
| D3DDECLTYPE \_ D3DCOLOR | D3DDECLUSAGE \_ 色彩        | 0           | D3DFVF \_ 擴散           |
| D3DDECLTYPE \_ D3DCOLOR | D3DDECLUSAGE \_ 色彩        | 1           | D3DFVF \_ 反光          |
| D3DDECLTYPE \_ FLOATm   | D3DDECLUSAGE \_ TEXCOORD     | n           | D3DFVF \_ TEXCOORDSIZEm (n)   |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ 位置     | 1           | N/A                       |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ 正常       | 1           | N/A                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點宣告](vertex-declaration.md)
</dt> </dl>

 

 



