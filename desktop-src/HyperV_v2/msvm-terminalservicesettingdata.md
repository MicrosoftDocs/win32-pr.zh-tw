---
description: 代表主機上虛擬電腦終端機服務的設定。
ms.assetid: 1f8d0718-09da-4231-95eb-cc63b6f324dd
title: Msvm_TerminalServiceSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalServiceSettingData
- Msvm_TerminalServiceSettingData.InstanceID
- Msvm_TerminalServiceSettingData.Caption
- Msvm_TerminalServiceSettingData.Description
- Msvm_TerminalServiceSettingData.ElementName
- Msvm_TerminalServiceSettingData.ListenerPort
- Msvm_TerminalServiceSettingData.DisableSelfSignedCertificateGeneration
- Msvm_TerminalServiceSettingData.AuthCertificateHash
- Msvm_TerminalServiceSettingData.TrustedIssuerCertificateHashes
- Msvm_TerminalServiceSettingData.AllowedHashAlgorithms
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3ec87429a70236d1e35b593c959880fa0937c3fc44daf22e834290158e83aab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146697"
---
# <a name="msvm_terminalservicesettingdata-class"></a>Msvm \_ TerminalServiceSettingData 類別

代表主機上虛擬電腦終端機服務的設定。 無法直接修改這個類別的屬性。 用戶端必須呼叫 [**Msvm \_ TerminalService. ModifyServiceSettings**](modifyservicesettings-msvm-terminalservice.md) 方法來修改任何這些屬性。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Hyper-V Terminal Service Settings";
  string  Description = "Settings for the Hyper-V Terminal Service";
  string  ElementName = "Hyper-V Terminal Service Settings";
  uint32  ListenerPort;
  boolean DisableSelfSignedCertificateGeneration;
  uint8   AuthCertificateHash[];
  string  TrustedIssuerCertificateHashes[];
  string  AllowedHashAlgorithms[];
};
```

## <a name="members"></a>成員

**Msvm \_ TerminalServiceSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ TerminalServiceSettingData** 類別具有這些屬性。

<dl> <dt>

**AllowedHashAlgorithms**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

驗證同盟驗證權杖簽章所接受的雜湊演算法清單。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**AuthCertificateHash**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要用於遠端驗證之憑證的雜湊。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**DisableSelfSignedCertificateGeneration**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

停用自我簽署憑證產生。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**ListenerPort**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將在其上進行初始遠端會話連接的網路埠。

</dd> <dt>

**TrustedIssuerCertificateHashes**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

驗證同盟驗證權杖簽章的受信任簽發者憑證雜湊清單。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

