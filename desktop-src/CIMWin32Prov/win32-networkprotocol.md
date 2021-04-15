---
description: Win32 \_ NetworkProtocol&\# 8194;WMI 類別代表 Win32 電腦系統上的通訊協定和其網路特性。
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Win32_NetworkProtocol 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468481"
---
# <a name="win32_networkprotocol-class"></a><span data-ttu-id="c808e-103">Win32 \_ NetworkProtocol 類別</span><span class="sxs-lookup"><span data-stu-id="c808e-103">Win32\_NetworkProtocol class</span></span>

<span data-ttu-id="c808e-104">**Win32 \_ NetworkProtocol** [WMI 類別](../wmisdk/retrieving-a-class.md)代表 win32 電腦系統上的通訊協定和其網路特性。</span><span class="sxs-lookup"><span data-stu-id="c808e-104">The **Win32\_NetworkProtocol** [WMI class](../wmisdk/retrieving-a-class.md) represents a protocol and its network characteristics on a Win32 computer system.</span></span>

<span data-ttu-id="c808e-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c808e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c808e-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="c808e-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c808e-107">語法</span><span class="sxs-lookup"><span data-stu-id="c808e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a><span data-ttu-id="c808e-108">成員</span><span class="sxs-lookup"><span data-stu-id="c808e-108">Members</span></span>

<span data-ttu-id="c808e-109">**Win32 \_ NetworkProtocol** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c808e-109">The **Win32\_NetworkProtocol** class has these types of members:</span></span>

-   [<span data-ttu-id="c808e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c808e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c808e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c808e-111">Properties</span></span>

<span data-ttu-id="c808e-112">**Win32 \_ NetworkProtocol** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c808e-112">The **Win32\_NetworkProtocol** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c808e-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="c808e-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c808e-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-116">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="c808e-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-117">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="c808e-117">A short textual description of the object.</span></span>

<span data-ttu-id="c808e-118">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c808e-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c808e-119">**ConnectionlessService**</span><span class="sxs-lookup"><span data-stu-id="c808e-119">**ConnectionlessService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-120">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-122">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP1 \_ 無連接」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP1\_CONNECTIONLESS")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-123">通訊協定支援不需連線的服務。</span><span class="sxs-lookup"><span data-stu-id="c808e-123">Protocol supports connectionless service.</span></span> <span data-ttu-id="c808e-124">不需連線的 (資料包) 服務會描述通訊協定或傳輸，其中的資料封包會彼此獨立地路由傳送，而且可能會遵循不同的路由，並以與其傳送的不同順序送達。</span><span class="sxs-lookup"><span data-stu-id="c808e-124">A connectionless (datagram) service describes a communications protocol or transport in which data packets are routed independently of each other and may follow different routes and arrive in a different order from that in which they were sent.</span></span> <span data-ttu-id="c808e-125">相反地，連接導向的服務會提供虛擬電路，資料封包會以傳輸的相同順序接收。</span><span class="sxs-lookup"><span data-stu-id="c808e-125">Conversely, a connection-oriented service provides a virtual circuit through which data packets are received in the same order they were transmitted.</span></span> <span data-ttu-id="c808e-126">如果電腦之間的連接失敗，就會通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="c808e-126">If the connection between computers fails, the application is notified.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-127">**說明**</span><span class="sxs-lookup"><span data-stu-id="c808e-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c808e-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-130">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="c808e-130">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-131">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="c808e-131">A textual description of the object.</span></span>

<span data-ttu-id="c808e-132">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c808e-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c808e-133">**GuaranteesDelivery**</span><span class="sxs-lookup"><span data-stu-id="c808e-133">**GuaranteesDelivery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-136">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 保證 \_ 傳遞」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_DELIVERY")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-137">通訊協定支援傳遞資料封包。</span><span class="sxs-lookup"><span data-stu-id="c808e-137">Protocol supports delivery of data packets.</span></span> <span data-ttu-id="c808e-138">如果此旗標為 **FALSE**，則不確定傳送的所有資料都會到達預期的目的地。</span><span class="sxs-lookup"><span data-stu-id="c808e-138">If this flag is **FALSE**, it is uncertain that all of the data sent will reach the intended destination.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-139">**GuaranteesSequencing**</span><span class="sxs-lookup"><span data-stu-id="c808e-139">**GuaranteesSequencing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-140">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-142">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 保證 \_ 順序」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_ORDER")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-143">通訊協定可確保資料會依照傳送的順序抵達。</span><span class="sxs-lookup"><span data-stu-id="c808e-143">Protocol ensures that data will arrive in the order in which it was sent.</span></span> <span data-ttu-id="c808e-144">請注意，這個特性不會確保資料的傳遞，而只是其順序。</span><span class="sxs-lookup"><span data-stu-id="c808e-144">Be aware that this characteristic does not ensure delivery of the data, only its order.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c808e-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-146">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c808e-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-148">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="c808e-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-149">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="c808e-149">Indicates when the object was installed.</span></span> <span data-ttu-id="c808e-150">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="c808e-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c808e-151">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c808e-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c808e-152">**MaximumAddressSize**</span><span class="sxs-lookup"><span data-stu-id="c808e-152">**MaximumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-153">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c808e-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-155">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| iMaxSockAddr」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「字元」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMaxSockAddr"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-156">通訊協定支援的通訊端位址最大長度。</span><span class="sxs-lookup"><span data-stu-id="c808e-156">Maximum length of a socket address supported by the protocol.</span></span> <span data-ttu-id="c808e-157">通訊端位址可以是 () 的 URL， `www.microsoft.com` 或 () 的 IP 位址等專案 `130.215.24.1` 。</span><span class="sxs-lookup"><span data-stu-id="c808e-157">Socket addresses may be items such as a URL (`www.microsoft.com`) or an IP address (`130.215.24.1`).</span></span>

</dd> <dt>

<span data-ttu-id="c808e-158">**MaximumMessageSize**</span><span class="sxs-lookup"><span data-stu-id="c808e-158">**MaximumMessageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-159">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c808e-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-161">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwMessageSize」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「字元」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwMessageSize"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-162">通訊協定支援的訊息大小上限。</span><span class="sxs-lookup"><span data-stu-id="c808e-162">Maximum message size supported by the protocol.</span></span> <span data-ttu-id="c808e-163">這是可由主機傳送或接收之訊息的大小上限。</span><span class="sxs-lookup"><span data-stu-id="c808e-163">This is the maximum size of a message that can be sent from or received by the host.</span></span> <span data-ttu-id="c808e-164">對於不支援訊息框架的通訊協定，可傳送至指定位址之訊息的實際大小上限可能會小於此值。</span><span class="sxs-lookup"><span data-stu-id="c808e-164">For protocols that do not support message framing, the actual maximum size of a message that can be sent to a given address may be less than this value.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-165">**MessageOriented**</span><span class="sxs-lookup"><span data-stu-id="c808e-165">**MessageOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-166">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-168">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 訊息 \_ 導向」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_MESSAGE\_ORIENTED")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-169">通訊協定為訊息導向。</span><span class="sxs-lookup"><span data-stu-id="c808e-169">Protocol is message-oriented.</span></span> <span data-ttu-id="c808e-170">訊息導向的通訊協定會使用資料的封包來傳輸資訊。</span><span class="sxs-lookup"><span data-stu-id="c808e-170">A message-oriented protocol uses packets of data to transfer information.</span></span> <span data-ttu-id="c808e-171">相反地，資料流程導向的通訊協定會以連續的位元組資料流程來傳送資料。</span><span class="sxs-lookup"><span data-stu-id="c808e-171">Conversely, stream-oriented protocols transfer data as a continuous stream of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-172">**MinimumAddressSize**</span><span class="sxs-lookup"><span data-stu-id="c808e-172">**MinimumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-173">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c808e-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-175">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| iMinSockAddr」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「字元」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMinSockAddr "), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-176">通訊協定所支援之通訊端位址的最小長度。</span><span class="sxs-lookup"><span data-stu-id="c808e-176">Minimum length of a socket address supported by the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-177">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c808e-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c808e-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-180">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Name" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| lpProtocol" ) </span><span class="sxs-lookup"><span data-stu-id="c808e-180">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|lpProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-181">通訊協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="c808e-181">Name for the protocol.</span></span>

<span data-ttu-id="c808e-182">範例： "TCP/IP"</span><span class="sxs-lookup"><span data-stu-id="c808e-182">Example: "TCP/IP"</span></span>

</dd> <dt>

<span data-ttu-id="c808e-183">**PseudoStreamOriented**</span><span class="sxs-lookup"><span data-stu-id="c808e-183">**PseudoStreamOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-184">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-186">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 虛擬 \_ 資料流程」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_PSEUDO\_STREAM")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-187">通訊協定是一種訊息導向的通訊協定，可接收所有接收作業的可變長度資料封包或資料流程處理資料。</span><span class="sxs-lookup"><span data-stu-id="c808e-187">Protocol is a message-oriented protocol that can receive variable-length data packets or streamed data for all receive operations.</span></span> <span data-ttu-id="c808e-188">當應用程式不希望通訊協定框架訊息，而且需要資料流程導向特性時，此選擇性功能就很有用。</span><span class="sxs-lookup"><span data-stu-id="c808e-188">This optional ability is useful when an application does not want the protocol to frame messages, and requires stream-oriented characteristics.</span></span> <span data-ttu-id="c808e-189">若 **為 TRUE**，表示通訊協定為虛擬資料流程導向。</span><span class="sxs-lookup"><span data-stu-id="c808e-189">If **TRUE**, the protocol is pseudo stream-oriented.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-190">**狀態**</span><span class="sxs-lookup"><span data-stu-id="c808e-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c808e-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-193">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="c808e-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-194">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="c808e-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="c808e-195">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="c808e-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c808e-196">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="c808e-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c808e-197">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="c808e-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c808e-198">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="c808e-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c808e-199">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="c808e-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c808e-200">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="c808e-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c808e-201">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c808e-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c808e-202">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="c808e-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c808e-203">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="c808e-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c808e-204">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c808e-205">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c808e-206">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c808e-207">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c808e-208">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c808e-209">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c808e-210">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c808e-211">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c808e-212">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="c808e-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c808e-213">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c808e-214">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-214">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c808e-215">**SupportsBroadcasting**</span><span class="sxs-lookup"><span data-stu-id="c808e-215">**SupportsBroadcasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-216">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-218">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 支援 \_ 廣播」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_BROADCAST")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-219">通訊協定支援在網路上廣播訊息的機制。</span><span class="sxs-lookup"><span data-stu-id="c808e-219">Protocol supports a mechanism for broadcasting messages across the network.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-220">**SupportsConnectData**</span><span class="sxs-lookup"><span data-stu-id="c808e-220">**SupportsConnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-221">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-223">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ CONNECT \_ 資料」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_CONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-224">通訊協定可讓資料透過網路連接。</span><span class="sxs-lookup"><span data-stu-id="c808e-224">Protocol allows data to be connected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-225">**SupportsDisconnectData**</span><span class="sxs-lookup"><span data-stu-id="c808e-225">**SupportsDisconnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-226">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-227">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-228">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 中斷連接 \_ 資料」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-228">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_DISCONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-229">通訊協定可讓網路上的資料中斷連線。</span><span class="sxs-lookup"><span data-stu-id="c808e-229">Protocol allows data to be disconnected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-230">**SupportsEncryption**</span><span class="sxs-lookup"><span data-stu-id="c808e-230">**SupportsEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-231">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-233">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 加密」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_ENCRYPTS")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-234">通訊協定支援資料加密。</span><span class="sxs-lookup"><span data-stu-id="c808e-234">Protocol supports data encryption.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-235">**SupportsExpeditedData**</span><span class="sxs-lookup"><span data-stu-id="c808e-235">**SupportsExpeditedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-236">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-238">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 快速 \_ 資料」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_EXPEDITED\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-239">通訊協定支援快速資料 (也稱為網路上) 的緊急資料。</span><span class="sxs-lookup"><span data-stu-id="c808e-239">Protocol supports expedited data (also known as urgent data) across the network.</span></span> <span data-ttu-id="c808e-240">加急資料可以略過流量控制，並優先于一般資料封包。</span><span class="sxs-lookup"><span data-stu-id="c808e-240">Expedited data can bypass flow control and receive priority over normal data packets.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-241">**SupportsFragmentation**</span><span class="sxs-lookup"><span data-stu-id="c808e-241">**SupportsFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-242">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-244">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 片段」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_FRAGMENTATION")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-245">通訊協定支援以片段傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="c808e-245">Protocol supports transmitting the data in fragments.</span></span> <span data-ttu-id="c808e-246">實體網路最大傳輸單位 (MTU) 會從應用程式隱藏。</span><span class="sxs-lookup"><span data-stu-id="c808e-246">Physical network maximum transfer unit (MTU) is hidden from applications.</span></span> <span data-ttu-id="c808e-247">每個媒體類型都有無法超過的框架大小上限。</span><span class="sxs-lookup"><span data-stu-id="c808e-247">Each media type has a maximum frame size that cannot be exceeded.</span></span> <span data-ttu-id="c808e-248">連結層會探索 MTU，並將其報告為使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c808e-248">The link layer discovers the MTU and reports it to the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-249">**SupportsGracefulClosing**</span><span class="sxs-lookup"><span data-stu-id="c808e-249">**SupportsGracefulClosing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-250">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-252">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 正常 \_ 關閉」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GRACEFUL\_CLOSE")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-253">通訊協定支援兩階段關閉作業，也稱為「正常關閉作業」。</span><span class="sxs-lookup"><span data-stu-id="c808e-253">Protocol supports two-phase close operations, also known as "graceful close operations".</span></span> <span data-ttu-id="c808e-254">如果沒有，通訊協定只支援 abortive 關閉作業。</span><span class="sxs-lookup"><span data-stu-id="c808e-254">If not, the protocol supports only abortive close operations.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-255">**SupportsGuaranteedBandwidth**</span><span class="sxs-lookup"><span data-stu-id="c808e-255">**SupportsGuaranteedBandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-256">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-258">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 頻寬 \_ 配置」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_BANDWIDTH\_ALLOCATION")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-259">通訊協定具有建立和維護頻寬的機制。</span><span class="sxs-lookup"><span data-stu-id="c808e-259">Protocol has a mechanism to establish and maintain a bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-260">**SupportsMulticasting**</span><span class="sxs-lookup"><span data-stu-id="c808e-260">**SupportsMulticasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-261">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-263">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 支援 \_ 多播」 ) </span><span class="sxs-lookup"><span data-stu-id="c808e-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_MULTICAST")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-264">通訊協定支援多播。</span><span class="sxs-lookup"><span data-stu-id="c808e-264">Protocol supports multicasting.</span></span>

</dd> <dt>

<span data-ttu-id="c808e-265">**SupportsQualityofService**</span><span class="sxs-lookup"><span data-stu-id="c808e-265">**SupportsQualityofService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c808e-266">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c808e-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c808e-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c808e-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c808e-268">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| WSAPROTOCOL \_ 資訊 \| dwServiceFlags1 \| XP1 \_ QOS 支援」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="c808e-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|WSAPROTOCOL\_INFO\|dwServiceFlags1\|XP1\_QOS\_SUPPORTED")</span></span>
</dt> </dl>

<span data-ttu-id="c808e-269">通訊協定可以支援服務品質 (QoS) 由基礎分層服務提供者或傳輸電訊廠商支援。</span><span class="sxs-lookup"><span data-stu-id="c808e-269">Protocol is capable of Quality of Service (QoS) support by the underlying layered service provider or transport carrier.</span></span> <span data-ttu-id="c808e-270">QoS 是元件的集合，可對透過網路傳輸的資料子集啟用區分和優先處理。</span><span class="sxs-lookup"><span data-stu-id="c808e-270">QoS is a collection of components that enable differentiation and preferential treatment for subsets of data transmitted over the network.</span></span> <span data-ttu-id="c808e-271">QoS 表示資料子集會在往返網路時取得較高優先順序或保證服務。</span><span class="sxs-lookup"><span data-stu-id="c808e-271">QoS means subsets of data get higher priority or guaranteed service when traversing a network.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c808e-272">備註</span><span class="sxs-lookup"><span data-stu-id="c808e-272">Remarks</span></span>

<span data-ttu-id="c808e-273">**Win32 \_ NetworkProtocol** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c808e-273">The **Win32\_NetworkProtocol** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c808e-274">範例</span><span class="sxs-lookup"><span data-stu-id="c808e-274">Examples</span></span>

<span data-ttu-id="c808e-275">下列 VBScript 程式碼範例示範如何從 **Win32 \_ NetworkProtocol** 的實例中取出執行中服務的清單。</span><span class="sxs-lookup"><span data-stu-id="c808e-275">The following VBScript code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



<span data-ttu-id="c808e-276">下列 Perl 程式碼範例示範如何從 **Win32 \_ NetworkProtocol** 的實例中取出執行中服務的清單。</span><span class="sxs-lookup"><span data-stu-id="c808e-276">The following Perl code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="c808e-277">規格需求</span><span class="sxs-lookup"><span data-stu-id="c808e-277">Requirements</span></span>



| <span data-ttu-id="c808e-278">需求</span><span class="sxs-lookup"><span data-stu-id="c808e-278">Requirement</span></span> | <span data-ttu-id="c808e-279">值</span><span class="sxs-lookup"><span data-stu-id="c808e-279">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c808e-280">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c808e-280">Minimum supported client</span></span><br/> | <span data-ttu-id="c808e-281">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c808e-281">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c808e-282">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c808e-282">Minimum supported server</span></span><br/> | <span data-ttu-id="c808e-283">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c808e-283">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c808e-284">命名空間</span><span class="sxs-lookup"><span data-stu-id="c808e-284">Namespace</span></span><br/>                | <span data-ttu-id="c808e-285">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c808e-285">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c808e-286">MOF</span><span class="sxs-lookup"><span data-stu-id="c808e-286">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c808e-287"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c808e-287"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c808e-288">DLL</span><span class="sxs-lookup"><span data-stu-id="c808e-288">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c808e-289"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c808e-289"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c808e-290">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c808e-290">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c808e-291">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="c808e-291">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="c808e-292">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="c808e-292">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
