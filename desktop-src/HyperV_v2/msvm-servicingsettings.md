---
description: 包含在服務作業期間使用的設定。
ms.assetid: 17dc3c97-232c-4ac4-988c-84c3061b4133
title: Msvm_ServicingSettings 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServicingSettings
- Msvm_ServicingSettings.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16033583a012c71ef2150ff68dc06564e149de84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469221"
---
# <a name="msvm_servicingsettings-class"></a>Msvm \_ ServicingSettings 類別

包含在服務作業期間使用的設定。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Singleton, AMENDMENT]
class Msvm_ServicingSettings
{
  string Version;
};
```

## <a name="members"></a>成員

**Msvm \_ ServicingSettings** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ServicingSettings** 類別具有這些屬性。

<dl> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含類別定義的版本。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




