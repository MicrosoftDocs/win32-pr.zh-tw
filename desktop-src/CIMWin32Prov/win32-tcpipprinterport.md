---
description: Win32 \_ TCPIPPrinterPort&\# 32;WMI 類別代表 TCP/IP 服務存取點。
ms.assetid: b1be18b6-47de-461c-a90b-c7e0537130ef
ms.tgt_platform: multiple
title: Win32_TCPIPPrinterPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TCPIPPrinterPort
- Win32_TCPIPPrinterPort.Caption
- Win32_TCPIPPrinterPort.Description
- Win32_TCPIPPrinterPort.InstallDate
- Win32_TCPIPPrinterPort.Status
- Win32_TCPIPPrinterPort.CreationClassName
- Win32_TCPIPPrinterPort.Name
- Win32_TCPIPPrinterPort.SystemCreationClassName
- Win32_TCPIPPrinterPort.SystemName
- Win32_TCPIPPrinterPort.Type
- Win32_TCPIPPrinterPort.ByteCount
- Win32_TCPIPPrinterPort.HostAddress
- Win32_TCPIPPrinterPort.PortNumber
- Win32_TCPIPPrinterPort.Protocol
- Win32_TCPIPPrinterPort.Queue
- Win32_TCPIPPrinterPort.SNMPCommunity
- Win32_TCPIPPrinterPort.SNMPDevIndex
- Win32_TCPIPPrinterPort.SNMPEnabled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a0b0f0cb73cc60ff117399a636b0ab8542fac6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972347"
---
# <a name="win32_tcpipprinterport-class"></a><span data-ttu-id="e352b-103">Win32 \_ TCPIPPrinterPort 類別</span><span class="sxs-lookup"><span data-stu-id="e352b-103">Win32\_TCPIPPrinterPort class</span></span>

<span data-ttu-id="e352b-104">**Win32 \_ TCPIPPrinterPort** [WMI 類別](../wmisdk/retrieving-a-class.md)代表 tcp/ip 服務存取點。</span><span class="sxs-lookup"><span data-stu-id="e352b-104">The **Win32\_TCPIPPrinterPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a TCP/IP service access point.</span></span>

<span data-ttu-id="e352b-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e352b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e352b-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e352b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e352b-107">語法</span><span class="sxs-lookup"><span data-stu-id="e352b-107">Syntax</span></span>

``` syntax
class Win32_TCPIPPrinterPort : CIM_ServiceAccessPoint
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
  boolean  ByteCount;
  string   HostAddress;
  uint32   PortNumber;
  uint32   Protocol;
  string   Queue;
  string   SNMPCommunity;
  uint32   SNMPDevIndex;
  boolean  SNMPEnabled;
};
```

## <a name="members"></a><span data-ttu-id="e352b-108">成員</span><span class="sxs-lookup"><span data-stu-id="e352b-108">Members</span></span>

<span data-ttu-id="e352b-109">**Win32 \_ TCPIPPrinterPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e352b-109">The **Win32\_TCPIPPrinterPort** class has these types of members:</span></span>

-   [<span data-ttu-id="e352b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e352b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e352b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e352b-111">Properties</span></span>

<span data-ttu-id="e352b-112">**Win32 \_ TCPIPPrinterPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e352b-112">The **Win32\_TCPIPPrinterPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e352b-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="e352b-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-114">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e352b-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e352b-116">若 **為 TRUE**，則電腦會先計算檔中的位元組數，然後再將其傳送至印表機，而印表機則會回報實際讀取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e352b-116">If **TRUE**, the computer counts the bytes in a document before sending them to the printer and the printer reports back the number of bytes actually read.</span></span> <span data-ttu-id="e352b-117">當列印輸出中偵測到遺漏的位元組時，就會使用這項功能進行診斷。</span><span class="sxs-lookup"><span data-stu-id="e352b-117">This capability is used for diagnostics when missing bytes are detected in the print output.</span></span>

</dd> <dt>

<span data-ttu-id="e352b-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="e352b-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e352b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e352b-121">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="e352b-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e352b-122">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="e352b-122">A short textual description of the object.</span></span>

<span data-ttu-id="e352b-123">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e352b-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e352b-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e352b-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e352b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e352b-127">限定詞： [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="e352b-127">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e352b-128">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="e352b-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e352b-129">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="e352b-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e352b-130">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。</span><span class="sxs-lookup"><span data-stu-id="e352b-130">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="e352b-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="e352b-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e352b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e352b-134">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="e352b-134">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e352b-135">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="e352b-135">A textual description of the object.</span></span>

<span data-ttu-id="e352b-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e352b-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e352b-137">**HostAddress**</span><span class="sxs-lookup"><span data-stu-id="e352b-137">**HostAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e352b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e352b-140">裝置或列印伺服器的位址。</span><span class="sxs-lookup"><span data-stu-id="e352b-140">Address of the device or print server.</span></span>

</dd> <dt>

<span data-ttu-id="e352b-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e352b-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-142">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="e352b-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e352b-144">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="e352b-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e352b-145">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="e352b-145">Indicates when the object was installed.</span></span> <span data-ttu-id="e352b-146">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="e352b-146">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e352b-147">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e352b-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e352b-148">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e352b-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e352b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e352b-151">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="e352b-151">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e352b-152">可唯一識別服務存取點，並提供所管理功能的指示。</span><span class="sxs-lookup"><span data-stu-id="e352b-152">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="e352b-153">此功能在物件的 Description 屬性中有更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="e352b-153">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="e352b-154">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。</span><span class="sxs-lookup"><span data-stu-id="e352b-154">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="e352b-155">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="e352b-155">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-156">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e352b-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e352b-158">埠監視器用來與裝置通訊的 TCP 埠數目。</span><span class="sxs-lookup"><span data-stu-id="e352b-158">Number of the TCP ports used by the port monitor to communicate with the device.</span></span>

</dd> <dt>

<span data-ttu-id="e352b-159">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="e352b-159">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-160">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e352b-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e352b-162">使用的列印通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e352b-162">Printing protocol used.</span></span> <span data-ttu-id="e352b-163">某些印表機只支援 LPR。</span><span class="sxs-lookup"><span data-stu-id="e352b-163">Some printers support only LPR.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="e352b-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="e352b-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="e352b-165">RAW</span><span class="sxs-lookup"><span data-stu-id="e352b-165">RAW</span></span>

<span data-ttu-id="e352b-166">直接列印到裝置或列印伺服器。</span><span class="sxs-lookup"><span data-stu-id="e352b-166">Printing directly to a device or print server.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="e352b-167"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="e352b-167"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="e352b-168">Lpr</span><span class="sxs-lookup"><span data-stu-id="e352b-168">LPR</span></span>

<span data-ttu-id="e352b-169">舊版通訊協定，最終會以 RAW 取代。</span><span class="sxs-lookup"><span data-stu-id="e352b-169">Legacy protocol, which is eventually replaced by RAW.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e352b-170">**佇列**</span><span class="sxs-lookup"><span data-stu-id="e352b-170">**Queue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e352b-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e352b-173">與 LPR 通訊協定搭配使用時，伺服器上的列印佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="e352b-173">Name of the print queue on the server when used with the LPR protocol.</span></span>

</dd> <dt>

<span data-ttu-id="e352b-174">**SNMPCommunity**</span><span class="sxs-lookup"><span data-stu-id="e352b-174">**SNMPCommunity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e352b-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e352b-177">裝置的安全性層級值。</span><span class="sxs-lookup"><span data-stu-id="e352b-177">Security level value for the device.</span></span>

<span data-ttu-id="e352b-178">範例：「公用」</span><span class="sxs-lookup"><span data-stu-id="e352b-178">Example: "public'"</span></span>

</dd> <dt>

<span data-ttu-id="e352b-179">**SNMPDevIndex**</span><span class="sxs-lookup"><span data-stu-id="e352b-179">**SNMPDevIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-180">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e352b-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e352b-182">此裝置的 snmp 索引號碼，適用于 SNMP 代理程式。</span><span class="sxs-lookup"><span data-stu-id="e352b-182">SNMP index number of this device for the SNMP agent.</span></span>

</dd> <dt>

<span data-ttu-id="e352b-183">**SNMPEnabled**</span><span class="sxs-lookup"><span data-stu-id="e352b-183">**SNMPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-184">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e352b-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e352b-186">若 **為 TRUE**，則此印表機支援 [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (簡易的網路管理通訊協定) ，而且可以從裝置提供豐富的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="e352b-186">If **TRUE**, this printer supports [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Simple Network Management Protocol) and can provide rich status information from the device.</span></span>

</dd> <dt>

<span data-ttu-id="e352b-187">**狀態**</span><span class="sxs-lookup"><span data-stu-id="e352b-187">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e352b-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e352b-190">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="e352b-190">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e352b-191">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="e352b-191">String that indicates the current status of the object.</span></span> <span data-ttu-id="e352b-192">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="e352b-192">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e352b-193">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="e352b-193">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e352b-194">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="e352b-194">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e352b-195">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="e352b-195">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e352b-196">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="e352b-196">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e352b-197">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="e352b-197">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e352b-198">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e352b-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e352b-199">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="e352b-199">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e352b-200">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="e352b-200">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e352b-201">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="e352b-201">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e352b-202">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="e352b-202">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e352b-203">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="e352b-203">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e352b-204">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="e352b-204">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e352b-205">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="e352b-205">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e352b-206">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="e352b-206">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e352b-207">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="e352b-207">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e352b-208">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="e352b-208">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e352b-209">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="e352b-209">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e352b-210">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="e352b-210">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e352b-211">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="e352b-211">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e352b-212">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e352b-212">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e352b-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e352b-215">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="e352b-215">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e352b-216">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="e352b-216">The scoping system's creation class name.</span></span>

<span data-ttu-id="e352b-217">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。</span><span class="sxs-lookup"><span data-stu-id="e352b-217">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="e352b-218">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e352b-218">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e352b-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e352b-221">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**Name**") 、 [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="e352b-221">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e352b-222">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="e352b-222">The scoping system's name.</span></span>

<span data-ttu-id="e352b-223">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。</span><span class="sxs-lookup"><span data-stu-id="e352b-223">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="e352b-224">**型別**</span><span class="sxs-lookup"><span data-stu-id="e352b-224">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e352b-225">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e352b-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e352b-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e352b-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e352b-227">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="e352b-227">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e352b-228">SAP 的類型，例如 [已連接] 或 [已重新導向]。</span><span class="sxs-lookup"><span data-stu-id="e352b-228">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="e352b-229">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。</span><span class="sxs-lookup"><span data-stu-id="e352b-229">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="e352b-230">**寫入** (1) </span><span class="sxs-lookup"><span data-stu-id="e352b-230">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="e352b-231">**閱讀** (2) </span><span class="sxs-lookup"><span data-stu-id="e352b-231">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="e352b-232">重新 **導向** (4) </span><span class="sxs-lookup"><span data-stu-id="e352b-232">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="e352b-233">**Net \_附加** (8) </span><span class="sxs-lookup"><span data-stu-id="e352b-233">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e352b-234">**未知** 的 (16) </span><span class="sxs-lookup"><span data-stu-id="e352b-234">**unknown** (16)</span></span>


<span data-ttu-id="e352b-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e352b-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e352b-236">備註</span><span class="sxs-lookup"><span data-stu-id="e352b-236">Remarks</span></span>

<span data-ttu-id="e352b-237">**Win32 \_ TCPIPPrinterPort** 類別衍生自 cim [**\_ ServiceAccessPoint**](cim-serviceaccesspoint.md) ，它衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e352b-237">The **Win32\_TCPIPPrinterPort** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="e352b-238">需要有 **SeLoadDriverPrivilege** 許可權，才能刪除這個 WMI 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="e352b-238">The **SeLoadDriverPrivilege** privilege is required to delete an instance of this WMI class.</span></span> <span data-ttu-id="e352b-239">下列腳本程式碼片段示範如何建立使用此許可權的 WMI 連接。</span><span class="sxs-lookup"><span data-stu-id="e352b-239">The following script snippet demonstrates how to make a connection to WMI that uses this privilege.</span></span>

`Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate, (LoadDriver)}")`

## <a name="examples"></a><span data-ttu-id="e352b-240">範例</span><span class="sxs-lookup"><span data-stu-id="e352b-240">Examples</span></span>

<span data-ttu-id="e352b-241">下列 PowerShell 範例會移除印表機和相關聯的 TCPIP 印表機埠。</span><span class="sxs-lookup"><span data-stu-id="e352b-241">The following PowerShell sample removes a printer and the associated TCPIP printer port.</span></span>


```PowerShell
function Remove-PrinterAndPort{
    Param( $printername )
   $printer=gwmi win32_Printer -filter "name='HPDJ600'"
   $printer.Delete()
   $port=gwmi win32_tcpipprinterport -filter "name='$($printer.portname)'" -enableall
   $port.Delete()
}
```



## <a name="requirements"></a><span data-ttu-id="e352b-242">規格需求</span><span class="sxs-lookup"><span data-stu-id="e352b-242">Requirements</span></span>



| <span data-ttu-id="e352b-243">需求</span><span class="sxs-lookup"><span data-stu-id="e352b-243">Requirement</span></span> | <span data-ttu-id="e352b-244">值</span><span class="sxs-lookup"><span data-stu-id="e352b-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e352b-245">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e352b-245">Minimum supported client</span></span><br/> | <span data-ttu-id="e352b-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e352b-246">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="e352b-247">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e352b-247">Minimum supported server</span></span><br/> | <span data-ttu-id="e352b-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e352b-248">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="e352b-249">命名空間</span><span class="sxs-lookup"><span data-stu-id="e352b-249">Namespace</span></span><br/>                | <span data-ttu-id="e352b-250">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e352b-250">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="e352b-251">MOF</span><span class="sxs-lookup"><span data-stu-id="e352b-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e352b-252"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e352b-252"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="e352b-253">DLL</span><span class="sxs-lookup"><span data-stu-id="e352b-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e352b-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e352b-254"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e352b-255">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e352b-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e352b-256">**CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="e352b-256">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dt>

[<span data-ttu-id="e352b-257">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="e352b-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
