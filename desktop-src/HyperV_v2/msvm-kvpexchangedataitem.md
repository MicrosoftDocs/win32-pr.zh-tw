---
description: 代表索引鍵/值組。
ms.assetid: B13E9C5F-5B13-4EE5-AE5F-F51B61BDB9B7
title: Msvm_KvpExchangeDataItem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeDataItem
- Msvm_KvpExchangeDataItem.InstanceID
- Msvm_KvpExchangeDataItem.Caption
- Msvm_KvpExchangeDataItem.Description
- Msvm_KvpExchangeDataItem.ElementName
- Msvm_KvpExchangeDataItem.Source
- Msvm_KvpExchangeDataItem.Name
- Msvm_KvpExchangeDataItem.Data
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 540c54a694dab1c80a32f9648a90c5b5bf1e48a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983893"
---
# <a name="msvm_kvpexchangedataitem-class"></a>Msvm \_ KvpExchangeDataItem 類別

代表索引鍵/值組。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_KvpExchangeDataItem : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Key-Value Pair Exchange Data Item";
  string Description = "Microsoft Key-Value Pair Exchange Data Item";
  string ElementName = "Key-Value Pair Exchange Data Item";
  uint16 Source;
  string Name;
  string Data;
};
```

## <a name="members"></a>成員

**Msvm \_ KvpExchangeDataItem** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ KvpExchangeDataItem** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**資料**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) 
</dt> </dl>

索引鍵/值組的值部分。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

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

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) 
</dt> </dl>

索引鍵/值組的索引鍵部分。



| Key                                                                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"CSDVersion"</dt> </dl>                 | 字串，代表在來賓系統上安裝的最新 service pack。 例如，"Service Pack 2"。 如果未安裝 service pack，此字串會是空的。<br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>FullyQualifiedDomainName</dt> </dl>   | 字串，代表可唯一識別本機電腦的完整 DNS 名稱。 此名稱是 DNS 主機名稱與 DNS 功能變數名稱的組合，其使用的格式為 *主機* 名。*DomainName*。 如果本機電腦是叢集中的節點，則此值為叢集虛擬伺服器的完整 DNS 名稱。 當 *NameType* 參數為 "ComputerNameDnsFullyQualified" 時，此值會符合 [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa)函數所傳回的名稱。<br/> |
| <dl> <dt>"IntegrationServicesVersion"</dt> </dl> | 字串，代表目前安裝在來賓虛擬機器中的 Integration Services 版本 (例如 "6.1.7000.0" ) 。<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>"NetworkAddressIPv4"</dt> </dl>         | 字串，包含目前指派給來賓虛擬機器的 IPv4 地址清單（以分號分隔）。 每當來賓虛擬機器上發生 TCP/IP 設定變更時，就會自動更新此清單。 每個位址都以小數點十進位標記法表示。 <br/>                                                                                                                                                                                                                         |
| <dl> <dt>"NetworkAddressIPv6"</dt> </dl>         | 字串，包含目前指派給來賓虛擬機器的 IPv6 地址清單（以分號分隔）。 每當來賓虛擬機器上發生 TCP/IP 設定變更時，就會自動更新此清單。 每個位址都以冒號-十六進位標記法表示。 IPv4 和 IPv6 清單不保證隨時都處於同步。<br/>                                                                                                                                             |
| <dl> <dt>"OSBuildNumber"</dt> </dl>              | 字串，代表作業系統的組建編號。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"OSEditionId"</dt> </dl>                | 代表來賓虛擬機器作業系統之版本 (SKU) 的字串。 如需可能值的清單，請參閱 [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) 函數。<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>OSName</dt> </dl>                     | 表示作業系統名稱的字串。 此值來自下列登錄專案： **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**<br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <dt>OSMajorVersion</dt> </dl>             | 表示作業系統主要版本號碼的字串。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>OSMinorVersion</dt> </dl>             | 字串，代表作業系統的次要版本號碼。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>"OSPlatformId"</dt> </dl>               | 表示作業系統平臺的字串。 **資料** 屬性的可能值為 "1"，表示不支援的 windows 系統，"2" 表示支援的 windows 系統。<br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>OSVersion</dt> </dl>                  | 表示作業系統版本的字串。 此字串的格式為 *MajorVersion*。*MinorVersion*。*BuildNumber*。 例如，適用于 Windows Server 2003 的 "5.2.3790"。<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>ProcessorArchitecture</dt> </dl>      | 表示作業系統處理器架構的字串。 如需值的清單，請參閱 [**系統 \_ 資訊**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)結構的 **wProcessorArchitecture** 成員。<br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>ProductType</dt> </dl>                | 表示產品類型的字串。 如需值的清單，請參閱 [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)結構的 **wProductType** 成員。<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"RDPAddressIPv4"</dt> </dl>             | 字串，包含來賓虛擬機器 RDP 堆疊目前正在接聽的 IPv4 地址清單（以分號分隔）。 如果 RDP 堆疊目前不在執行中，則字串會是空的。 當 TCP/IP 設定變更影響來賓虛擬機器上的 RDP 堆疊時，此清單會自動更新。 每個位址都以小數點十進位標記法表示。<br/>                                                                                                                   |
| <dl> <dt>"RDPAddressIPv6"</dt> </dl>             | 字串，包含來賓虛擬機器 RDP 堆疊目前正在接聽的 IPv6 地址清單（以分號分隔）。 如果 RDP 堆疊目前不在執行中，則字串會是空的。 當 TCP/IP 設定變更影響來賓虛擬機器上的 RDP 堆疊時，此清單會自動更新。 每個位址都以冒號-十六進位標記法表示。<br/>                                                                                                             |
| <dl> <dt>"ServicePackMajor"</dt> </dl>           | 字串，代表安裝在系統上的最新 service pack 的主要版本號碼。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"ServicePackMinor"</dt> </dl>           | 字串，代表安裝在系統上的最新 service pack 的次要版本號碼。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"SuiteMask"</dt> </dl>                  | 表示系統上可用之產品套件的字串。 這個字串是 [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)結構之 **wSuiteMask** 成員的任何值的組合。<br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**來源**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資料的來源。



| 值                                                                        | 意義                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 主機推送時的 "HostExchangeItems"。<br/>                                                                                                                                                                                      |
| <dl> <dt>1</dt> </dl> | 由來賓虛擬機器推送時為 "GuestExchangeItems"。<br/>                                                                                                                                                                    |
| <dl> <dt>2</dt> </dl> | 當來賓虛擬機器自動填入時，為 "GuestIntrinsicExchangeItems"。<br/>                                                                                                                                          |
| <dl> <dt>4</dt> </dl> | 表示專案僅限主機，而且不會與來賓虛擬機器共用。 搭配 [**Msvm \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md)類別的 **HostOnlyItems** 屬性使用。 <br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ KvpExchangeDataItem** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> <dt>

[**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

