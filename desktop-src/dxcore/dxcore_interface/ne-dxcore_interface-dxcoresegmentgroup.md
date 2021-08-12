---
title: DXCoreSegmentGroup
description: 定義常數，指定介面卡的記憶體區段群組。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2474f8084035ddb67f7081ea45cd1d1743c053415a7bbade68ecff3d4527636c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279620"
---
# <a name="dxcoresegmentgroup-enum"></a>DXCoreSegmentGroup 列舉

定義常數，指定介面卡的記憶體區段群組。

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a>常數

### <a name="local"></a>本機

指定視為介面卡區域的區段群組，並代表 GPU 可用的最快記憶體。 您的應用程式應該將本機區段群組的目標設為其工作集的目標大小。

### <a name="nonlocal"></a>外地

指定視為非本機的區段群組，且效能可能會比本機區段群組更慢。

## <a name="see-also"></a>另請參閱

[DXCore 參考](../dxcore-reference.md)， [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)