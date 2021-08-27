---
title: DXCoreAdapterPreference
description: 定義常數，指定要當做清單排序準則使用的 DXCore 介面卡喜好設定。
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: a58f2c948751d5217a89e52bc862057ac6a67c85bdf2fabed96c2b5ad68364cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117728"
---
# <a name="dxcoreadapterpreference-enum"></a>DXCoreAdapterPreference 列舉

## <a name="description"></a>描述

定義常數，指定要當做清單排序準則使用的 DXCore 介面卡喜好設定。 您可以藉由將 **DXCoreAdapterPreference** 陣列傳遞至 [IDXCoreAdapterList：： sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md)，來排序 DXCore 介面卡清單。

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a>列舉欄位

### <a name="hardware"></a>硬體

指定硬體配接器 (的喜好設定，而不是) 的軟體配接器。

### <a name="minimumpower"></a>MinimumPower

指定最小的 GPU (的喜好設定，例如整合式圖形處理器或 iGPU) 。

### <a name="highperformance"></a>高效能

指定最高效能 GPU 的喜好設定，例如外部圖形處理器 (xGPU) （如果有的話），或離散圖形處理器 (dGPU) （如果有的話）。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapterList：： Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)