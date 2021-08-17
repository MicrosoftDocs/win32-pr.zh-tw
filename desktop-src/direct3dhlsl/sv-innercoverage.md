---
title: SV_InnerCoverage
description: SV \_ InputCoverage 代表低估的保守式點陣化資訊， (也就是是否保證可以完全涵蓋) 的圖元。
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172ee60cb85e69568c8cb226aa19fa325686726f42fc27c7aa21231b1a55ef28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724376"
---
# <a name="sv_innercoverage"></a>SV \_ InnerCoverage

SV \_ InputCoverage 代表低估的保守式點陣化資訊， (也就是是否保證可以完全涵蓋) 的圖元。

## <a name="type"></a>類型



| 類型     |
|------|
| uint |



 

## <a name="remarks"></a>備註

第3層支援需要此系統產生的值，且僅適用于該層。 此輸入與 SV \_ 涵蓋範圍互斥-兩者皆無法使用。

若要存取 SV \_ InnerCoverage，必須將它宣告為一個圖元著色器輸入暫存器中的單一元件。 宣告上的插補模式必須是常數 (插補不會套用) 。

您可以在 D3D 11.3 和 D3D12 中使用保守的點陣化功能。 請參閱：

-   [D3D 11.3 保守柵格化](/windows/desktop/direct3d11/conservative-rasterization)
-   [D3D12 保守的點陣化](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[著色器模型5.1 系統值](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
