---
title: ReplicationProvider1 類別
description: 提供者實例的基類。
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- ReplicationProvider1 類別 Active Directory
- ReplicationProvider1 類別 Active Directory，說明
topic_type:
- apiref
api_name:
- ReplicationProvider1
- ReplicationProvider1.ClientLoadableCLSID
- ReplicationProvider1.CLSID
- ReplicationProvider1.Concurrency
- ReplicationProvider1.DefaultMachineName
- ReplicationProvider1.Enabled
- ReplicationProvider1.ImpersonationLevel
- ReplicationProvider1.InitializationReentrancy
- ReplicationProvider1.InitializationTimeoutInterval
- ReplicationProvider1.InitializeAsAdminFirst
- ReplicationProvider1.Name
- ReplicationProvider1.OperationTimeoutInterval
- ReplicationProvider1.PerLocaleInitialization
- ReplicationProvider1.PerUserInitialization
- ReplicationProvider1.Pure
- ReplicationProvider1.SecurityDescriptor
- ReplicationProvider1.SupportsExplicitShutdown
- ReplicationProvider1.SupportsExtendedStatus
- ReplicationProvider1.SupportsQuotas
- ReplicationProvider1.SupportsSendStatus
- ReplicationProvider1.SupportsShutdown
- ReplicationProvider1.SupportsThrottling
- ReplicationProvider1.UnloadTimeout
- ReplicationProvider1.Version
- ReplicationProvider1.HostingModel
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3e8ca70d2bb5f37303c20117ddba59db6950d1dda58779179c6ef08c95abc4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025126"
---
# <a name="replicationprovider1-class"></a>ReplicationProvider1 類別

提供者實例的基類。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class ReplicationProvider1 : __Win32Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy = 0;
  datetime InitializationTimeoutInterval;
  boolean  InitializeAsAdminFirst;
  string   Name;
  datetime OperationTimeoutInterval;
  boolean  PerLocaleInitialization = FALSE;
  boolean  PerUserInitialization = FALSE;
  boolean  Pure = TRUE;
  string   SecurityDescriptor;
  boolean  SupportsExplicitShutdown;
  boolean  SupportsExtendedStatus;
  boolean  SupportsQuotas;
  boolean  SupportsSendStatus;
  boolean  SupportsShutdown;
  boolean  SupportsThrottling;
  datetime UnloadTimeout;
  uint32   Version;
  string   HostingModel;
};
```

## <a name="members"></a>成員

**ReplicationProvider1** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ReplicationProvider1** 類別具有這些屬性。

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

WMI 用來判斷是否要將高效能提供者載入至用戶端進程或 WMI 進程的類別識別碼。 如果提供者和用戶端都位於相同的電腦上，WMI 會使用 **ClientLoadableCLSID** 做為類別識別碼，將處理常式載入至用戶端。 當提供者和用戶端位於不同的電腦上時，WMI 會將提供者載入至 WMI。 WMI 也會使用 **ClientLoadableCLSID** 來支援重新整理作業。

如需詳細資訊，請參閱 [註冊 High-Performance 提供者。](/windows/desktop/WmiSdk/registering-a-high-performance-provider)

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

**GUID** ，表示提供者 COM 物件 (**CLSID**) 的類別識別碼。 這個 COM 物件必須包含 [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) 介面的實作為。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**並行**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

識別要啟動提供者的電腦。 如果提供者在本機電腦上執行，則為 **Null**。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，則會啟用此實例，並可用來完成用戶端要求。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "HostingModel" ) 
</dt> </dl>

包含提供者的裝載模型。

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

保留的。 預設值為零 (0)。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

提供序列化相關資訊的一組旗標。 預設值為零 (0)。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

此提供者的所有初始化都必須序列化。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

在相同的命名空間中，此提供者的所有初始化都必須序列化。

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

不需要初始化序列化。

</dd> </dl>

</dd> <dt>

**InitializationTimeoutInterval**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

**Windows Server 2003：** 這個屬性已停用。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

提供者名稱。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，當使用者使用不同的地區設定連接到相同的命名空間時，就會為每個地區設定初始化提供者。 預設值為 **FALSE**。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，則會為每個 NT LAN Manager 初始化一次提供者 (NTLM) 使用者來對提供者提出要求。 如果 **為 FALSE** (預設) ，則提供者會針對所有使用者初始化一次。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**純**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，當 WMI 呼叫其主要介面的 **發行** 方法時，提供者同意在所有未完成的介面點上呼叫 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ，以準備卸載。 必須保持 WMI 用戶端無法作為提供者的提供者，應該將 **純** 設定為 **FALSE**。 預設設定為 **TRUE**。 如需詳細資訊，請參閱本主題的「備註」一節。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

安全描述項定義語言中的安全描述項 (SD)  (SDDL) ，可決定可成功呼叫 IWbemDecoupledRegistrar 的一組使用者 [**：向**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) 低耦合提供者註冊。 如需詳細資訊，請參閱 Windows SDK 的安全性一節中的「[安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language)」主題。 此安全描述項僅供低耦合提供者使用，且不會影響其他提供者。 如需詳細資訊，請參閱 [將提供者併入應用程式](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application)。

WMI 會針對使用 [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) 和 [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) 介面的低耦合提供者執行存取檢查。 如果安全描述項為 **Null**，則只有在 LocalSystem、NetworkService、LocalService 帳戶下執行的應用程式或服務可以執行低耦合提供者。

下列字串顯示只有內建系統管理員才能執行的低耦合提供者。」O:BAG：不正確： (A;; 0x1;;;BA) 」

如需設定 **SecurityDescriptor** 屬性的詳細資訊，請參閱 [維護 WMI 安全性](/windows/desktop/WmiSdk/maintaining-wmi-security)。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

[日期和時間格式](/windows/desktop/WmiSdk/date-and-time-format) ，指定 WMI 允許提供者在卸載之前保持閒置的時間長度。 一般而言，提供者會要求 WMI 等待時間不超過五分鐘。

針對目前版本的 WMI，會忽略這個屬性的值。 WMI 會根據根命名空間內部類別中的超時值來卸載提供者 \\ 。 建議提供者設定 **UnloadTimeout**。 如需詳細資訊，請參閱卸載 [提供者](/windows/desktop/WmiSdk/unloading-a-provider)。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

提供者的版本。 支援的版本為1和2。 第2版可針對所有相關聯的屬性註冊增強有效性檢查，特別是 [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) 屬性。

這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。

</dd> </dl>

## <a name="remarks"></a>備註

此類別的實例代表 Active Directory 網域服務的 WMI 提供者。 預設值如下：

-   Name = "ReplProv1"
-   ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"
-   HostingModel = "NetworkServiceHost"

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.dll mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

