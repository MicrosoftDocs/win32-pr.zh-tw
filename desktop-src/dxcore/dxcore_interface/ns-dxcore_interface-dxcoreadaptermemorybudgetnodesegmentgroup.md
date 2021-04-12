---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: 描述介面卡的記憶體區段群組。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375601"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a>DXCoreAdapterMemoryBudgetNodeSegmentGroup 結構

描述介面卡的記憶體區段群組。

## <a name="syntax"></a>語法

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a>成員

### <a name="nodeindex"></a>nodeIndex

類型： **uint32_t**

指定要查詢其介面卡記憶體資訊的裝置實體介面卡。 若為單一介面卡操作，請將此設定為零。 如果有多個介面卡節點，請將此設定為節點的索引， (您要查詢其介面卡記憶體資訊之裝置的實體介面卡)  (查看 [多個介面卡系統](../../direct3d12/multi-engine.md)) 。

### <a name="segmentgroup"></a>segmentGroup

類型： **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**

指定您想要查詢的介面卡記憶體區段群組。

## <a name="see-also"></a>另請參閱

[DXCore 參考](../dxcore-reference.md)

[使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)

[多個介面卡系統](../../direct3d12/multi-engine.md)