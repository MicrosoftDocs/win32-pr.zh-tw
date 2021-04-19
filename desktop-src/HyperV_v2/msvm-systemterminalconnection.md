---
description: 將虛擬機器與終端機連線建立關聯。
ms.assetid: 31979FB8-3870-44D9-9720-AD99237C5268
title: Msvm_SystemTerminalConnection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemTerminalConnection
- Msvm_SystemTerminalConnection.Antecedent
- Msvm_SystemTerminalConnection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 368c25b8505ec7ddd29da3b95d95fc842602119e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973016"
---
# <a name="msvm_systemterminalconnection-class"></a>Msvm \_ SystemTerminalConnection 類別

將虛擬機器與終端機連線建立關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemTerminalConnection : CIM_HostedDependency
{
  Msvm_ComputerSystem     REF Antecedent;
  Msvm_TerminalConnection REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ SystemTerminalConnection** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ SystemTerminalConnection** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_**](msvm-computersystem.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Antecedent」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

連接所連接的虛擬機器。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ TerminalConnection**](msvm-terminalconnection.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

虛擬機器的連接。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ SystemTerminalConnection** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ HostedDependency**](cim-hosteddependency.md)
</dt> <dt>

[**CIM \_ HostedDependency**](/previous-versions//cc136861(v=vs.85))
</dt> <dt>

[影片類別](video-classes.md)
</dt> </dl>

 

