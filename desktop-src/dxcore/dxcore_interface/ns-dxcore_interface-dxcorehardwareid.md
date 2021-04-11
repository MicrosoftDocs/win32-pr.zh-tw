---
title: DXCoreHardwareID
description: 代表介面卡的 PnP 硬體識別碼部分。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092797"
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