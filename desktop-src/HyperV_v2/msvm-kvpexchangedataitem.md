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
# <a name="msvm_kvpexchangedataitem-class"></a><span data-ttu-id="7adf0-103">Msvm \_ KvpExchangeDataItem 類別</span><span class="sxs-lookup"><span data-stu-id="7adf0-103">Msvm\_KvpExchangeDataItem class</span></span>

<span data-ttu-id="7adf0-104">代表索引鍵/值組。</span><span class="sxs-lookup"><span data-stu-id="7adf0-104">Represents a key/value pair.</span></span>

<span data-ttu-id="7adf0-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7adf0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7adf0-106">語法</span><span class="sxs-lookup"><span data-stu-id="7adf0-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="7adf0-107">成員</span><span class="sxs-lookup"><span data-stu-id="7adf0-107">Members</span></span>

<span data-ttu-id="7adf0-108">**Msvm \_ KvpExchangeDataItem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7adf0-108">The **Msvm\_KvpExchangeDataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="7adf0-109">屬性</span><span class="sxs-lookup"><span data-stu-id="7adf0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7adf0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7adf0-110">Properties</span></span>

<span data-ttu-id="7adf0-111">**Msvm \_ KvpExchangeDataItem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7adf0-111">The **Msvm\_KvpExchangeDataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7adf0-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="7adf0-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7adf0-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7adf0-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7adf0-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7adf0-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7adf0-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="7adf0-115">A short description of the object.</span></span> <span data-ttu-id="7adf0-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="7adf0-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7adf0-117">**資料**</span><span class="sxs-lookup"><span data-stu-id="7adf0-117">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7adf0-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7adf0-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7adf0-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7adf0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7adf0-120">限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="7adf0-120">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="7adf0-121">索引鍵/值組的值部分。</span><span class="sxs-lookup"><span data-stu-id="7adf0-121">The value portion of the key/value pair.</span></span>

</dd> <dt>

<span data-ttu-id="7adf0-122">**說明**</span><span class="sxs-lookup"><span data-stu-id="7adf0-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7adf0-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7adf0-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7adf0-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7adf0-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7adf0-125">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="7adf0-125">A description of the object.</span></span> <span data-ttu-id="7adf0-126">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="7adf0-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7adf0-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7adf0-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7adf0-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7adf0-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7adf0-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7adf0-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7adf0-130">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="7adf0-130">A display name for the object.</span></span> <span data-ttu-id="7adf0-131">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="7adf0-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7adf0-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7adf0-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7adf0-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7adf0-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7adf0-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7adf0-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7adf0-135">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="7adf0-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7adf0-136">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="7adf0-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7adf0-137">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="7adf0-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7adf0-138">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7adf0-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7adf0-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7adf0-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7adf0-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7adf0-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7adf0-141">限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="7adf0-141">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="7adf0-142">索引鍵/值組的索引鍵部分。</span><span class="sxs-lookup"><span data-stu-id="7adf0-142">The key portion of the key/value pair.</span></span>



| <span data-ttu-id="7adf0-143">Key</span><span class="sxs-lookup"><span data-stu-id="7adf0-143">Key</span></span>                                                                                                     | <span data-ttu-id="7adf0-144">描述</span><span class="sxs-lookup"><span data-stu-id="7adf0-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7adf0-145"><dt>"CSDVersion"</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-145"><dt>"CSDVersion"</dt></span></span> </dl>                 | <span data-ttu-id="7adf0-146">字串，代表在來賓系統上安裝的最新 service pack。</span><span class="sxs-lookup"><span data-stu-id="7adf0-146">A string that represents the latest service pack installed on the guest system.</span></span> <span data-ttu-id="7adf0-147">例如，"Service Pack 2"。</span><span class="sxs-lookup"><span data-stu-id="7adf0-147">For example, "Service Pack 2".</span></span> <span data-ttu-id="7adf0-148">如果未安裝 service pack，此字串會是空的。</span><span class="sxs-lookup"><span data-stu-id="7adf0-148">If no service pack has been installed, this string is empty.</span></span><br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="7adf0-149"><dt>FullyQualifiedDomainName</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-149"><dt>"FullyQualifiedDomainName"</dt></span></span> </dl>   | <span data-ttu-id="7adf0-150">字串，代表可唯一識別本機電腦的完整 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="7adf0-150">A string that represents the fully qualified DNS name that uniquely identifies the local computer.</span></span> <span data-ttu-id="7adf0-151">此名稱是 DNS 主機名稱與 DNS 功能變數名稱的組合，其使用的格式為 *主機* 名。*DomainName*。</span><span class="sxs-lookup"><span data-stu-id="7adf0-151">This name is a combination of the DNS host name and the DNS domain name, using the format *HostName*.*DomainName*.</span></span> <span data-ttu-id="7adf0-152">如果本機電腦是叢集中的節點，則此值為叢集虛擬伺服器的完整 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="7adf0-152">If the local computer is a node in a cluster, this value is the fully qualified DNS name of the cluster virtual server.</span></span> <span data-ttu-id="7adf0-153">當 *NameType* 參數為 "ComputerNameDnsFullyQualified" 時，此值會符合 [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa)函數所傳回的名稱。</span><span class="sxs-lookup"><span data-stu-id="7adf0-153">This value matches the name returned by the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function when the *NameType* parameter is "ComputerNameDnsFullyQualified".</span></span><br/> |
| <dl> <span data-ttu-id="7adf0-154"><dt>"IntegrationServicesVersion"</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-154"><dt>"IntegrationServicesVersion"</dt></span></span> </dl> | <span data-ttu-id="7adf0-155">字串，代表目前安裝在來賓虛擬機器中的 Integration Services 版本 (例如 "6.1.7000.0" ) 。</span><span class="sxs-lookup"><span data-stu-id="7adf0-155">A string representing the version of the Integration Services currently installed in the guest virtual machine (for example, "6.1.7000.0").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="7adf0-156"><dt>"NetworkAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-156"><dt>"NetworkAddressIPv4"</dt></span></span> </dl>         | <span data-ttu-id="7adf0-157">字串，包含目前指派給來賓虛擬機器的 IPv4 地址清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="7adf0-157">A string that contains a semicolon-delimited list of the IPv4 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="7adf0-158">每當來賓虛擬機器上發生 TCP/IP 設定變更時，就會自動更新此清單。</span><span class="sxs-lookup"><span data-stu-id="7adf0-158">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="7adf0-159">每個位址都以小數點十進位標記法表示。</span><span class="sxs-lookup"><span data-stu-id="7adf0-159">Each address is represented in dot-decimal notation.</span></span> <br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="7adf0-160"><dt>"NetworkAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-160"><dt>"NetworkAddressIPv6"</dt></span></span> </dl>         | <span data-ttu-id="7adf0-161">字串，包含目前指派給來賓虛擬機器的 IPv6 地址清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="7adf0-161">A string that contains a semicolon-delimited list of the IPv6 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="7adf0-162">每當來賓虛擬機器上發生 TCP/IP 設定變更時，就會自動更新此清單。</span><span class="sxs-lookup"><span data-stu-id="7adf0-162">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="7adf0-163">每個位址都以冒號-十六進位標記法表示。</span><span class="sxs-lookup"><span data-stu-id="7adf0-163">Each address is represented in colon-hexadecimal notation.</span></span> <span data-ttu-id="7adf0-164">IPv4 和 IPv6 清單不保證隨時都處於同步。</span><span class="sxs-lookup"><span data-stu-id="7adf0-164">The IPv4 and IPv6 lists are not guaranteed to be in sync at all times.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="7adf0-165"><dt>"OSBuildNumber"</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-165"><dt>"OSBuildNumber"</dt></span></span> </dl>              | <span data-ttu-id="7adf0-166">字串，代表作業系統的組建編號。</span><span class="sxs-lookup"><span data-stu-id="7adf0-166">A string that represents the build number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="7adf0-167"><dt>"OSEditionId"</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-167"><dt>"OSEditionId"</dt></span></span> </dl>                | <span data-ttu-id="7adf0-168">代表來賓虛擬機器作業系統之版本 (SKU) 的字串。</span><span class="sxs-lookup"><span data-stu-id="7adf0-168">A string representing the edition (SKU) of the guest virtual machine operating system.</span></span> <span data-ttu-id="7adf0-169">如需可能值的清單，請參閱 [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="7adf0-169">For a list of possible values, see the [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="7adf0-170"><dt>OSName</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-170"><dt>"OSName"</dt></span></span> </dl>                     | <span data-ttu-id="7adf0-171">表示作業系統名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="7adf0-171">A string that represents the name of the operating system.</span></span> <span data-ttu-id="7adf0-172">此值來自下列登錄專案： **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**</span><span class="sxs-lookup"><span data-stu-id="7adf0-172">This value comes from the following registry entry: **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**ProductName**</span></span><br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="7adf0-173"><dt>OSMajorVersion</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-173"><dt>"OSMajorVersion"</dt></span></span> </dl>             | <span data-ttu-id="7adf0-174">表示作業系統主要版本號碼的字串。</span><span class="sxs-lookup"><span data-stu-id="7adf0-174">A string that represents the major version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="7adf0-175"><dt>OSMinorVersion</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-175"><dt>"OSMinorVersion"</dt></span></span> </dl>             | <span data-ttu-id="7adf0-176">字串，代表作業系統的次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7adf0-176">A string that represents the minor version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="7adf0-177"><dt>"OSPlatformId"</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-177"><dt>"OSPlatformId"</dt></span></span> </dl>               | <span data-ttu-id="7adf0-178">表示作業系統平臺的字串。</span><span class="sxs-lookup"><span data-stu-id="7adf0-178">A string that represents the operating system platform.</span></span> <span data-ttu-id="7adf0-179">**資料** 屬性的可能值為 "1"，表示不支援的 windows 系統，"2" 表示支援的 windows 系統。</span><span class="sxs-lookup"><span data-stu-id="7adf0-179">The possible values of the **Data** property are "1" to indicate an unsupported Windows system and "2" to indicate a supported Windows system.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="7adf0-180"><dt>OSVersion</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-180"><dt>"OSVersion"</dt></span></span> </dl>                  | <span data-ttu-id="7adf0-181">表示作業系統版本的字串。</span><span class="sxs-lookup"><span data-stu-id="7adf0-181">A string that represents the operating system version.</span></span> <span data-ttu-id="7adf0-182">此字串的格式為 *MajorVersion*。*MinorVersion*。*BuildNumber*。</span><span class="sxs-lookup"><span data-stu-id="7adf0-182">The format of this string is *MajorVersion*.*MinorVersion*.*BuildNumber*.</span></span> <span data-ttu-id="7adf0-183">例如，適用于 Windows Server 2003 的 "5.2.3790"。</span><span class="sxs-lookup"><span data-stu-id="7adf0-183">For example, "5.2.3790" for Windows Server 2003.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="7adf0-184"><dt>ProcessorArchitecture</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-184"><dt>"ProcessorArchitecture"</dt></span></span> </dl>      | <span data-ttu-id="7adf0-185">表示作業系統處理器架構的字串。</span><span class="sxs-lookup"><span data-stu-id="7adf0-185">A string that represents the processor architecture of the operating system.</span></span> <span data-ttu-id="7adf0-186">如需值的清單，請參閱 [**系統 \_ 資訊**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)結構的 **wProcessorArchitecture** 成員。</span><span class="sxs-lookup"><span data-stu-id="7adf0-186">For a list of values, see the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="7adf0-187"><dt>ProductType</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-187"><dt>"ProductType"</dt></span></span> </dl>                | <span data-ttu-id="7adf0-188">表示產品類型的字串。</span><span class="sxs-lookup"><span data-stu-id="7adf0-188">A string that represents the product type.</span></span> <span data-ttu-id="7adf0-189">如需值的清單，請參閱 [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)結構的 **wProductType** 成員。</span><span class="sxs-lookup"><span data-stu-id="7adf0-189">For a list of values, see the **wProductType** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="7adf0-190"><dt>"RDPAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-190"><dt>"RDPAddressIPv4"</dt></span></span> </dl>             | <span data-ttu-id="7adf0-191">字串，包含來賓虛擬機器 RDP 堆疊目前正在接聽的 IPv4 地址清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="7adf0-191">A string that contains a semicolon-delimited list of the IPv4 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="7adf0-192">如果 RDP 堆疊目前不在執行中，則字串會是空的。</span><span class="sxs-lookup"><span data-stu-id="7adf0-192">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="7adf0-193">當 TCP/IP 設定變更影響來賓虛擬機器上的 RDP 堆疊時，此清單會自動更新。</span><span class="sxs-lookup"><span data-stu-id="7adf0-193">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="7adf0-194">每個位址都以小數點十進位標記法表示。</span><span class="sxs-lookup"><span data-stu-id="7adf0-194">Each address is represented in dot-decimal notation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="7adf0-195"><dt>"RDPAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-195"><dt>"RDPAddressIPv6"</dt></span></span> </dl>             | <span data-ttu-id="7adf0-196">字串，包含來賓虛擬機器 RDP 堆疊目前正在接聽的 IPv6 地址清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="7adf0-196">A string that contains a semicolon-delimited list of the IPv6 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="7adf0-197">如果 RDP 堆疊目前不在執行中，則字串會是空的。</span><span class="sxs-lookup"><span data-stu-id="7adf0-197">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="7adf0-198">當 TCP/IP 設定變更影響來賓虛擬機器上的 RDP 堆疊時，此清單會自動更新。</span><span class="sxs-lookup"><span data-stu-id="7adf0-198">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="7adf0-199">每個位址都以冒號-十六進位標記法表示。</span><span class="sxs-lookup"><span data-stu-id="7adf0-199">Each address is represented in colon-hexadecimal notation.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="7adf0-200"><dt>"ServicePackMajor"</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-200"><dt>"ServicePackMajor"</dt></span></span> </dl>           | <span data-ttu-id="7adf0-201">字串，代表安裝在系統上的最新 service pack 的主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7adf0-201">A string that represents the major version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="7adf0-202"><dt>"ServicePackMinor"</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-202"><dt>"ServicePackMinor"</dt></span></span> </dl>           | <span data-ttu-id="7adf0-203">字串，代表安裝在系統上的最新 service pack 的次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7adf0-203">A string that represents the minor version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="7adf0-204"><dt>"SuiteMask"</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-204"><dt>"SuiteMask"</dt></span></span> </dl>                  | <span data-ttu-id="7adf0-205">表示系統上可用之產品套件的字串。</span><span class="sxs-lookup"><span data-stu-id="7adf0-205">A string that represents the product suites available on the system.</span></span> <span data-ttu-id="7adf0-206">這個字串是 [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)結構之 **wSuiteMask** 成員的任何值的組合。</span><span class="sxs-lookup"><span data-stu-id="7adf0-206">This string is a combination of any of the values of the **wSuiteMask** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="7adf0-207">**來源**</span><span class="sxs-lookup"><span data-stu-id="7adf0-207">**Source**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7adf0-208">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7adf0-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7adf0-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7adf0-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7adf0-210">資料的來源。</span><span class="sxs-lookup"><span data-stu-id="7adf0-210">The source of the data.</span></span>



| <span data-ttu-id="7adf0-211">值</span><span class="sxs-lookup"><span data-stu-id="7adf0-211">Value</span></span>                                                                        | <span data-ttu-id="7adf0-212">意義</span><span class="sxs-lookup"><span data-stu-id="7adf0-212">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7adf0-213"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-213"><dt>0</dt></span></span> </dl> | <span data-ttu-id="7adf0-214">主機推送時的 "HostExchangeItems"。</span><span class="sxs-lookup"><span data-stu-id="7adf0-214">"HostExchangeItems" when pushed by the host.</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="7adf0-215"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-215"><dt>1</dt></span></span> </dl> | <span data-ttu-id="7adf0-216">由來賓虛擬機器推送時為 "GuestExchangeItems"。</span><span class="sxs-lookup"><span data-stu-id="7adf0-216">"GuestExchangeItems" when pushed by the guest virtual machine.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="7adf0-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="7adf0-218">當來賓虛擬機器自動填入時，為 "GuestIntrinsicExchangeItems"。</span><span class="sxs-lookup"><span data-stu-id="7adf0-218">"GuestIntrinsicExchangeItems" when automatically populated by the guest virtual machine.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="7adf0-219"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-219"><dt>4</dt></span></span> </dl> | <span data-ttu-id="7adf0-220">表示專案僅限主機，而且不會與來賓虛擬機器共用。</span><span class="sxs-lookup"><span data-stu-id="7adf0-220">Indicates that the item is host-only and not shared with the guest virtual machine.</span></span> <span data-ttu-id="7adf0-221">搭配 [**Msvm \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md)類別的 **HostOnlyItems** 屬性使用。</span><span class="sxs-lookup"><span data-stu-id="7adf0-221">Used with the **HostOnlyItems** property of the [**Msvm\_KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md) class.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7adf0-222">備註</span><span class="sxs-lookup"><span data-stu-id="7adf0-222">Remarks</span></span>

<span data-ttu-id="7adf0-223">存取 **Msvm \_ KvpExchangeDataItem** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="7adf0-223">Access to the **Msvm\_KvpExchangeDataItem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7adf0-224">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="7adf0-224">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7adf0-225">規格需求</span><span class="sxs-lookup"><span data-stu-id="7adf0-225">Requirements</span></span>



| <span data-ttu-id="7adf0-226">需求</span><span class="sxs-lookup"><span data-stu-id="7adf0-226">Requirement</span></span> | <span data-ttu-id="7adf0-227">值</span><span class="sxs-lookup"><span data-stu-id="7adf0-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7adf0-228">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7adf0-228">Minimum supported client</span></span><br/> | <span data-ttu-id="7adf0-229">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7adf0-229">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7adf0-230">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7adf0-230">Minimum supported server</span></span><br/> | <span data-ttu-id="7adf0-231">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7adf0-231">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7adf0-232">命名空間</span><span class="sxs-lookup"><span data-stu-id="7adf0-232">Namespace</span></span><br/>                | <span data-ttu-id="7adf0-233">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="7adf0-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7adf0-234">MOF</span><span class="sxs-lookup"><span data-stu-id="7adf0-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7adf0-235"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7adf0-236">DLL</span><span class="sxs-lookup"><span data-stu-id="7adf0-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7adf0-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7adf0-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7adf0-238">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7adf0-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adf0-239">**CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="7adf0-239">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> <dt>

[<span data-ttu-id="7adf0-240">**CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="7adf0-240">**CIM\_ManagedElement**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

