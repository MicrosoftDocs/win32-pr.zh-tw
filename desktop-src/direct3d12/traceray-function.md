---
description: 在加速結構中將光線傳送到搜尋中。
ms.assetid: ''
title: TraceRay 函式
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TraceRay
api_type:
- NA
ms.openlocfilehash: 4e22a26d7bd2fd91029c106133667bce98c163d90d99f0700dac7f2bdf0796fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027978"
---
# <a name="traceray-function"></a>TraceRay 函式

在加速結構中將光線傳送到搜尋中。

## <a name="syntax"></a>Syntax
此內建函式定義相當於下列函式範本：

```
Template<payload_t>
void TraceRay(RaytracingAccelerationStructure AccelerationStructure,
              uint RayFlags,
              uint InstanceInclusionMask,
              uint RayContributionToHitGroupIndex,
              uint MultiplierForGeometryContributionToHitGroupIndex,
              uint MissShaderIndex,
              RayDesc Ray,
              inout payload_t Payload);

```



## <a name="parameters"></a>參數

`AccelerationStructure`

要使用的最上層加速結構。 指定 Null 加速結構會強制遺漏。

`RayFlags`

[Ray_flag](ray_flag.md)值的有效組合。 系統只會傳播定義的光線旗標，也就是 [RayFlags](rayflags.md) 著色器內建可看見。

`InstanceInclusionMask`

不帶正負號的整數，也就是用來根據每個實例中的 InstanceMask 來包含或拒絕幾何實例的最下方8位。 例如：
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

不帶正負號的整數，指定要加入的位移，以針對點擊群組索引，在著色器資料表內進行計算。  只會使用此值的底部4位。

`MultiplierForGeometryContributionToHitGroupIndex`

不帶正負號的整數，指定要乘以 *GeometryContributionToHitGroupIndex* 的跨距，也就是以0為基底的索引，應用程式將幾何提供給其最底層的加速結構。 只會使用這個乘數值的下16位。

`MissShaderIndex`

不帶正負號的整數，指定著色器資料表內遺漏著色器的索引。

`Ray`

[**RayDesc**](raydesc.md) ，表示要追蹤的光線。

`Payload`

使用者定義的光線承載，可針對在 raytracing 期間叫用的著色器，同時存取輸入和輸出。  [**TraceRay**](traceray-function.md)完成後，呼叫端也可以存取承載。

## <a name="return-value"></a>傳回值

**void**

## <a name="remarks"></a>備註

您可以從下列 raytracing 著色器類型呼叫這個函數：

* [**最接近的點擊著色器**](closest-hit-shader.md)
* [**遺漏著色器**](miss-shader.md)
* [**光線產生著色器**](ray-generation-shader.md)



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




