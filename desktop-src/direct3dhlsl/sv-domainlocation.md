---
title: SV_DomainLocation
description: 定義要評估之目前網域點的輪廓上的位置。
ms.assetid: 907f568c-7c45-41e5-96c4-6e6b816a4a53
keywords:
- SV_DomainLocation HLSL
topic_type:
- apiref
api_name:
- SV_DomainLocation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc39a71bcbfb6f3719ecfc7d0abe463a1fd127e4
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827047"
---
# <a name="sv_domainlocation"></a>SV \_ DomainLocation

定義要評估之目前網域點的輪廓上的位置。

## <a name="type"></a>類型



| 類型       | 輸入拓撲               |
|--------|----------------|
| float2 | 四個修補程式     |
| float3 | 三個修補程式      |
| float2 | 等值 線        |



 

## <a name="remarks"></a>備註

此為必要的系統值。

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      | x      |          |       |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[語意](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




