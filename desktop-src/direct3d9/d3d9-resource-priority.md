---
description: 用來設定 SetPriority 中資源優先權的常數。
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: 'D3D9_RESOURCE_PRIORITY (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D9_RESOURCE_PRIORITY_MINIMUM
- D3D9_RESOURCE_PRIORITY_LOW
- D3D9_RESOURCE_PRIORITY_NORMAL
- D3D9_RESOURCE_PRIORITY_HIGH
- D3D9_RESOURCE_PRIORITY_MAXIMUM
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1ae5a54c7645db63b1023c3571f8181f4ee2daec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196209"
---
# <a name="d3d9_resource_priority"></a>D3D9 \_ 資源 \_ 優先順序

用來設定 [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority)中資源優先權的常數。



| 常數/值                                                                                                                                                                                                                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <dt>**D3D9 \_資源 \_ 優先順序 \_ 最小**</dt> <dt>0x28000000</dt> </dl> | 資源可能會有最低的優先順序。 這個常數會將資源標示為未使用和收回。 當另一個資源需要資源所佔用的記憶體空間時，就應該立即收回資源。<br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <dt>**D3D9 \_資源 \_ 優先順序 \_ 低**</dt> <dt>0x50000000</dt> </dl>             | 已排程低優先順序的資源。 資源的位置並不重要，而且作業系統會執行最少的工作來尋找資源的位置。 將資源標示為低優先順序，可讓其他更重要的資源佔用更快速的記憶體。<br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <dt>**D3D9 \_資源 \_ 優先順序 \_ 一般**</dt> <dt>0x78000000</dt> </dl>    | 資源會以一般優先順序排程。 資源的位置對於效能而言很重要，但並不重要。 作業系統應嘗試將標示為 normal 的資源放在資源的慣用位置，而非低優先順序的資源中。 一般而言，紋理會標示為一般。<br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <dt>**D3D9 \_資源 \_ 優先順序 \_ 高**</dt> <dt>0xa0000000</dt> </dl>          | 已排程高優先順序的資源。 資源的位置對於效能而言是不可或缺的。 作業系統一律會嘗試將標示為「高」的資源放在資源的慣用位置，而非低優先順序或一般優先順序的資源。 通常，轉譯目標會標示為高。<br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <dt>**D3D9 \_資源 \_ 優先順序 \_ 最大**</dt> <dt>0xc8000000</dt> </dl> | 資源的最高優先順序可能。 這個常數會將資源的優先順序標示為已軟釘選。 只有在沒有其他方法可解決 DMA 緩衝區的記憶體需求時，才會從記憶體中收回已進行軟釘釘的資源。 作業系統會嘗試將 DMA 緩衝區分割成其大小下限，並收回未釘選且未在收回已軟釘選資源之前未進行軟釘選的所有其他資源。 <br/> |



## <a name="remarks"></a>備註

排程器會將 **D3D9 \_ 資源 \_ 優先順序 \_ 下限** 和 **D3D9 \_ 資源 \_ 優先順序 \_ 最大** 值以外的值視為提示。

您可以使用本主題稍早所定義之值以外的優先權層級。 例如，將具有優先權層級0x78000001 的資源標記為，表示資源優先順序稍微高於一般。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
