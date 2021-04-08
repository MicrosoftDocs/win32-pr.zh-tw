---
title: Win32_TSVirtualDesktopServerSettings 類別
description: 包含 (RD 虛擬主機) server 的遠端桌面虛擬化主機的設定資訊。
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualDesktopServerSettings 類別遠端桌面服務
- Win32_TSVirtualDesktopServerSettings 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSVirtualDesktopServerSettings
- Win32_TSVirtualDesktopServerSettings.SessionBrokerName
- Win32_TSVirtualDesktopServerSettings.PolicySourceSessionBrokerName
- Win32_TSVirtualDesktopServerSettings.Concurrency
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39635aee7b32430ace0ead0e3b007051a3c049d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686349"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a>Win32 \_ TSVirtualDesktopServerSettings 類別

包含 (RD 虛擬主機) server 的遠端桌面虛擬化主機的設定資訊。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[singleton, dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVirtualDesktopServerSettings
{
  string SessionBrokerName;
  sint32 PolicySourceSessionBrokerName;
  uint32 Concurrency;
};
```

## <a name="members"></a>成員

**Win32 \_ TSVirtualDesktopServerSettings** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ TSVirtualDesktopServerSettings** 類別具有這些屬性。

<dl> <dt>

**並行**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

此虛擬桌面伺服器允許的並行布建要求數上限。

</dd> <dt>

**PolicySourceSessionBrokerName**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果設定為0，表示 **SessionBrokerName** 屬性是由伺服器設定;如果設定為1，表示 **SessionBrokerName** 屬性是由群組原則設定。

</dd> <dt>

**SessionBrokerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RD 虛擬主機伺服器之會話代理人的完整分辨名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                             |
| 命名空間<br/>                | 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





