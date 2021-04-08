---
description: 在 WMI 中註冊提供者實體執行的相關資訊。 預設會載入未設定 HostingModel 屬性的提供者，以便在 Wmiprvse.exe 進程中以 NetworkServiceHostOrSelfHost 的形式執行。
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: __Win32Provider 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0240c459ea2d09013379bfd7c3190ce691cf4cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945118"
---
# <a name="__win32provider-class"></a>\_\_Win32Provider 類別

**\_ \_ Win32Provider** 系統類別會在 WMI 中註冊提供者實體執行的相關資訊。 預設會載入未設定 **HostingModel** 屬性的提供者，以便在 Wmiprvse.exe 進程中以 **NetworkServiceHostOrSelfHost** 的形式執行。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __Win32Provider : __Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  string   HostingModel;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy;
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
};
```

## <a name="members"></a>成員

**\_ \_ Win32Provider** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ Win32Provider** 類別具有這些屬性。

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

WMI 用來判斷是否要將高效能提供者載入至用戶端進程或 WMI 進程的類別識別碼。 如果提供者和用戶端都位於相同的電腦上，WMI 會使用 **ClientLoadableCLSID** 做為類別識別碼，將處理常式載入至用戶端。 當提供者和用戶端位於不同的電腦上時，WMI 會將提供者載入至 WMI。 WMI 也會使用 **ClientLoadableCLSID** 來支援重新整理作業。

如需詳細資訊，請參閱 [註冊 High-Performance 提供者。](registering-a-high-performance-provider.md)

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

**GUID** ，表示提供者 COM 物件 (**CLSID**) 的類別識別碼。 這個 COM 物件必須包含 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面的實作為。

</dd> <dt>

**並行**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

識別要啟動提供者的電腦。 如果提供者在本機電腦上執行，則為 **Null**。

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，則會啟用此實例，並可用來完成用戶端要求。

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

這個屬性是由 [**MSFT \_ 提供者**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) **HostingGroup** 和 **HostingSpecification** 屬性中的值所組成。 這個屬性的值會指定 WMI 如何載入提供者，以及其執行所在的安全性帳戶。 如需設定 **HostingModel** 屬性的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md) ，以及 [註冊提供者](registering-a-provider.md)。

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

保留的。 預設值為零 (0)。

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

提供序列化相關資訊的一組旗標。 預設值為零 (0)。

<dt>

0
</dt> <dd>

此提供者的所有初始化都必須序列化。

</dd> <dt>

1
</dt> <dd>

在相同的命名空間中，此提供者的所有初始化都必須序列化。

</dd> <dt>

2
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

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

TBD

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](standard-qualifiers.md)
</dt> </dl>

提供者名稱。

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，當使用者使用不同的地區設定連接到相同的命名空間時，就會為每個地區設定初始化提供者。 預設值為 **FALSE**。

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，則會為每個 NT LAN Manager 初始化一次提供者 (NTLM) 使用者來對提供者提出要求。 如果 **為 FALSE** (預設) ，則提供者會針對所有使用者初始化一次。

</dd> <dt>

**純**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，當 WMI 呼叫其主要介面的 **發行** 方法時，提供者同意在所有未完成的介面點上呼叫 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ，以準備卸載。 必須保持 WMI 用戶端無法作為提供者的提供者，應該將 **純** 設定為 **FALSE**。 預設設定為 **TRUE**。 如需詳細資訊，請參閱本主題的「備註」一節。

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

安全描述項定義語言中的安全描述項 (SD)  (SDDL) ，可決定可成功呼叫 IWbemDecoupledRegistrar 的一組使用者 [**：向**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) 低耦合提供者註冊。 如需詳細資訊，請參閱 Windows SDK 的安全性一節中的「 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language) 」主題。 此安全描述項僅供低耦合提供者使用，且不會影響其他提供者。 如需詳細資訊，請參閱 [將提供者併入應用程式](incorporating-a-provider-in-an-application.md)。

WMI 會針對使用 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 和 [**IWbemObjectSink**](iwbemobjectsink.md) 介面的低耦合提供者執行存取檢查。 如果安全描述項為 **Null**，則只有在 LocalSystem、NetworkService、LocalService 帳戶下執行的應用程式或服務可以執行低耦合提供者。

下列字串顯示只有內建系統管理員才能執行的低耦合提供者。」O:BAG：不正確： (A;; 0x1;;;BA) 」

如需設定 **SecurityDescriptor** 屬性的詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

[日期和時間格式](date-and-time-format.md) ，指定 WMI 允許提供者在卸載之前保持閒置的時間長度。 一般而言，提供者會要求 WMI 等待時間不超過五分鐘。

針對目前版本的 WMI，會忽略這個屬性的值。 WMI 會根據根命名空間內部類別中的超時值來卸載提供者 \\ 。 建議提供者設定 **UnloadTimeout**。 如需詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

提供者的版本。 支援的版本為1和2。 第2版可針對所有相關聯的屬性註冊增強有效性檢查，特別是 [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) 屬性。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ Win32Provider** 類別衍生自 [**\_ \_ Provider**](--provider.md)。

大部分的提供者可以接受 **InitializationReentrancy** 屬性的預設值。 但是，如果提供者可以針對個別使用者支援同時初始化，則這個屬性可以設定為 1 (一個) 。 如果需要序列化初始化， **InitializationReentrancy** 會維持 0 (零) 。 在這兩個實例中， **PerUserInitialization** 會設定為 **TRUE**。

純粹提供者或提供者將 **純** 虛擬屬性設定為 **TRUE**，只存在於來自應用程式和 WMI 的服務要求。 大部分的提供者都是純服務提供者。 Nonpure 提供者是例外狀況。 Nonpure 提供者在完成服務要求之後，會轉換成用戶端的角色。

Nonpure 提供者的範例是開始發出查詢的推播提供者，並在完成初始化之後發出 WMI 要求。 除了在初始化時以資料更新 CIM 存放庫，推送提供者沒有任何責任。 更新存放庫之後，推播提供者可以等候卸載，或轉換為用戶端的角色。 等候卸載的推播提供者是純粹的提供者。 參與用戶端活動的推送提供者為 nonpure。

WMI 必須能夠區分純的提供者與非單純的提供者，讓它能夠判斷何時可以安全地關閉。 WMI 必須等待所有涉及非純提供者的作業完成，才能安全地關閉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_提供者**](/windows/desktop/WmiSdk/--provider)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[註冊提供者](registering-a-provider.md)
</dt> </dl>

 

