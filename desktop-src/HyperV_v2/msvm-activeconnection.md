---
description: 將交換器埠連接到埠所連接的 LAN 端點。
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Msvm_ActiveConnection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ActiveConnection
- Msvm_ActiveConnection.Antecedent
- Msvm_ActiveConnection.Dependent
- Msvm_ActiveConnection.TrafficType
- Msvm_ActiveConnection.OtherTrafficDescription
- Msvm_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf682fac419658785cfe7594aa6fc17e4b2dd28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851191"
---
# <a name="msvm_activeconnection-class"></a><span data-ttu-id="5dccf-103">Msvm \_ ActiveConnection 類別</span><span class="sxs-lookup"><span data-stu-id="5dccf-103">Msvm\_ActiveConnection class</span></span>

<span data-ttu-id="5dccf-104">將交換器埠連接到埠所連接的 LAN 端點。</span><span class="sxs-lookup"><span data-stu-id="5dccf-104">Connects a switch port to the LAN endpoint to which the port is connected.</span></span> <span data-ttu-id="5dccf-105">此物件的存在表示交換器埠和 LAN 端點會主動連線，而且與 LAN 端點相關聯的乙太網路埠可透過交換器埠與網路通訊。</span><span class="sxs-lookup"><span data-stu-id="5dccf-105">The existence of this object means that the switch port and the LAN endpoint are actively connected and the Ethernet port associated with the LAN endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="5dccf-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5dccf-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dccf-107">語法</span><span class="sxs-lookup"><span data-stu-id="5dccf-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ActiveConnection : CIM_ActiveConnection
{
  Msvm_LANEndpoint REF Antecedent;
  CIM_LANEndpoint  REF Dependent;
  uint16               TrafficType;
  string               OtherTrafficDescription;
  boolean              IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="5dccf-108">成員</span><span class="sxs-lookup"><span data-stu-id="5dccf-108">Members</span></span>

<span data-ttu-id="5dccf-109">**Msvm \_ ActiveConnection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5dccf-109">The **Msvm\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="5dccf-110">屬性</span><span class="sxs-lookup"><span data-stu-id="5dccf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5dccf-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5dccf-111">Properties</span></span>

<span data-ttu-id="5dccf-112">**Msvm \_ ActiveConnection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5dccf-112">The **Msvm\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5dccf-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="5dccf-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dccf-114">資料類型： **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="5dccf-114">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="5dccf-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5dccf-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dccf-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="5dccf-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5dccf-117">代表服務存取點的 [**Msvm \_ LANEndpoint**](msvm-lanendpoint.md) 類別實例的參考， (設定為通訊或正在主動與相依 SAP 進行通訊的 sap) 。</span><span class="sxs-lookup"><span data-stu-id="5dccf-117">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="5dccf-118">在單向連接中，此 SAP 是正在傳輸的。</span><span class="sxs-lookup"><span data-stu-id="5dccf-118">In an unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="5dccf-119">**依賴**</span><span class="sxs-lookup"><span data-stu-id="5dccf-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dccf-120">資料類型： **[ **CIM \_ LANEndpoint**](cim-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="5dccf-120">Data type: **[**CIM\_LANEndpoint**](cim-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="5dccf-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5dccf-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dccf-122">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="5dccf-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5dccf-123">[**Msvm \_ LANEndpoint**](cim-lanendpoint.md)類別實例的參考，代表已設定為要進行通訊或正在主動與之前的 SAP 通訊的 sap。</span><span class="sxs-lookup"><span data-stu-id="5dccf-123">A reference to an instance of the [**Msvm\_LANEndpoint**](cim-lanendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="5dccf-124">在單向連接中，此 SAP 是接收的。</span><span class="sxs-lookup"><span data-stu-id="5dccf-124">In an unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="5dccf-125">**IsUnidirectional**</span><span class="sxs-lookup"><span data-stu-id="5dccf-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dccf-126">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5dccf-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5dccf-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5dccf-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dccf-128">如果這個屬性為 **True**，則這個連接是單向的。否則，此連接是雙向的。</span><span class="sxs-lookup"><span data-stu-id="5dccf-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="5dccf-129">當連接為單向時，「說話者」應定義為前一個 **參考。**</span><span class="sxs-lookup"><span data-stu-id="5dccf-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="5dccf-130">在雙向連接中，所選存取點是否為 **Antecedent** 或 **相依** 的，並不重要。</span><span class="sxs-lookup"><span data-stu-id="5dccf-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="5dccf-131">這個屬性繼承自 [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="5dccf-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5dccf-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="5dccf-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dccf-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5dccf-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dccf-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5dccf-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dccf-135">這個屬性繼承自 [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="5dccf-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5dccf-136">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="5dccf-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dccf-137">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5dccf-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5dccf-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5dccf-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dccf-139">這個屬性繼承自 [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="5dccf-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5dccf-140">備註</span><span class="sxs-lookup"><span data-stu-id="5dccf-140">Remarks</span></span>

<span data-ttu-id="5dccf-141">存取 **Msvm \_ ActiveConnection** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="5dccf-141">Access to the **Msvm\_ActiveConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5dccf-142">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="5dccf-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="5dccf-143">範例</span><span class="sxs-lookup"><span data-stu-id="5dccf-143">Examples</span></span>

<span data-ttu-id="5dccf-144">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="5dccf-144">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5dccf-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="5dccf-145">Requirements</span></span>



| <span data-ttu-id="5dccf-146">需求</span><span class="sxs-lookup"><span data-stu-id="5dccf-146">Requirement</span></span> | <span data-ttu-id="5dccf-147">值</span><span class="sxs-lookup"><span data-stu-id="5dccf-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dccf-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5dccf-148">Minimum supported client</span></span><br/> | <span data-ttu-id="5dccf-149">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5dccf-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5dccf-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5dccf-150">Minimum supported server</span></span><br/> | <span data-ttu-id="5dccf-151">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5dccf-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5dccf-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="5dccf-152">Namespace</span></span><br/>                | <span data-ttu-id="5dccf-153">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="5dccf-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5dccf-154">MOF</span><span class="sxs-lookup"><span data-stu-id="5dccf-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5dccf-155"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="5dccf-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5dccf-156">DLL</span><span class="sxs-lookup"><span data-stu-id="5dccf-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dccf-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5dccf-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5dccf-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5dccf-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dccf-159">**CIM \_ ActiveConnection**</span><span class="sxs-lookup"><span data-stu-id="5dccf-159">**CIM\_ActiveConnection**</span></span>](cim-activeconnection.md)
</dt> <dt>

<span data-ttu-id="5dccf-160">[**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5dccf-160">[**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85))</span></span>
</dt> </dl>

 

