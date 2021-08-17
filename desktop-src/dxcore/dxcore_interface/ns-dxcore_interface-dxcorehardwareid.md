---
title: DXCoreHardwareID
description: 代表介面卡的 PnP 硬體識別碼部分。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68cdb130dd6f0c0338e5b94da2f68c58f98bb91d404871e18ac82e817881117c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118625"
---
# <a name="dxcorehardwareid-structure"></a>DXCoreHardwareID 結構

代表介面卡的 PnP 硬體識別碼部分。

## <a name="syntax"></a>語法

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a>成員

### <a name="vendorid"></a>vendorId

類型： **uint32_t \***

介面卡硬體廠商的 PCI 識別碼。

### <a name="deviceid"></a>deviceId

類型： **uint32_t \***

介面卡硬體裝置的 PCI 識別碼。

### <a name="subsysid"></a>subSysId

類型： **uint32_t \***

介面卡硬體子系統的 PCI 識別碼。

### <a name="revision"></a>revision

類型： **uint32_t \***

介面卡修訂編號的 PCI 識別碼。

## <a name="see-also"></a>另請參閱

[DXCore 參考](../dxcore-reference.md)， [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)