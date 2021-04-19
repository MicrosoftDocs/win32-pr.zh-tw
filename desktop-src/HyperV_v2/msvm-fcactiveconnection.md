---
description: 將交換器埠連接到埠所連接的光纖通道端點。
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Msvm_FcActiveConnection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcActiveConnection
- Msvm_FcActiveConnection.Antecedent
- Msvm_FcActiveConnection.Dependent
- Msvm_FcActiveConnection.TrafficType
- Msvm_FcActiveConnection.OtherTrafficDescription
- Msvm_FcActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e29330e073266f2f2a8749ec3c70d9e26b35ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998251"
---
# <a name="msvm_fcactiveconnection-class"></a><span data-ttu-id="35436-103">Msvm \_ FcActiveConnection 類別</span><span class="sxs-lookup"><span data-stu-id="35436-103">Msvm\_FcActiveConnection class</span></span>

<span data-ttu-id="35436-104">將交換器埠連接到埠所連接的光纖通道端點。</span><span class="sxs-lookup"><span data-stu-id="35436-104">Connects a switch port to the Fibre Channel endpoint to which the port is connected.</span></span> <span data-ttu-id="35436-105">此物件的存在表示交換器埠和光纖通道端點會主動連線，而且與光纖通道端點相關聯的光纖通道埠可透過交換器埠與網路通訊。</span><span class="sxs-lookup"><span data-stu-id="35436-105">The existence of this object means that the switch port and the Fibre Channel endpoint are actively connected, and the Fibre Channel port associated with the Fibre Channel endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="35436-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="35436-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35436-107">語法</span><span class="sxs-lookup"><span data-stu-id="35436-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcActiveConnection : CIM_ActiveConnection
{
  Msvm_FcEndpoint REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
  uint16              TrafficType;
  string              OtherTrafficDescription;
  boolean             IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="35436-108">成員</span><span class="sxs-lookup"><span data-stu-id="35436-108">Members</span></span>

<span data-ttu-id="35436-109">**Msvm \_ FcActiveConnection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="35436-109">The **Msvm\_FcActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="35436-110">屬性</span><span class="sxs-lookup"><span data-stu-id="35436-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35436-111">屬性</span><span class="sxs-lookup"><span data-stu-id="35436-111">Properties</span></span>

<span data-ttu-id="35436-112">**Msvm \_ FcActiveConnection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="35436-112">The **Msvm\_FcActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35436-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="35436-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35436-114">資料類型： **Msvm \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="35436-114">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="35436-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35436-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35436-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="35436-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="35436-117">代表服務存取點的 [**Msvm \_ FcEndpoint**](msvm-fcendpoint.md) 類別實例的參考， (設定為通訊或正在主動與相依 SAP 進行通訊的 sap) 。</span><span class="sxs-lookup"><span data-stu-id="35436-117">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="35436-118">在單向連接中，此 SAP 是正在傳輸的。</span><span class="sxs-lookup"><span data-stu-id="35436-118">In a unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="35436-119">**依賴**</span><span class="sxs-lookup"><span data-stu-id="35436-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35436-120">資料類型： **Msvm \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="35436-120">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="35436-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35436-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35436-122">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="35436-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="35436-123">[**Msvm \_ FcEndpoint**](msvm-fcendpoint.md)類別實例的參考，代表已設定為要進行通訊或正在主動與之前的 SAP 通訊的 sap。</span><span class="sxs-lookup"><span data-stu-id="35436-123">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="35436-124">在單向連接中，此 SAP 是接收的。</span><span class="sxs-lookup"><span data-stu-id="35436-124">In a unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="35436-125">**IsUnidirectional**</span><span class="sxs-lookup"><span data-stu-id="35436-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35436-126">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="35436-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35436-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35436-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35436-128">如果這個屬性為 **True**，則這個連接是單向的。否則，此連接是雙向的。</span><span class="sxs-lookup"><span data-stu-id="35436-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="35436-129">當連接為單向時，「說話者」應定義為前一個 **參考。**</span><span class="sxs-lookup"><span data-stu-id="35436-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="35436-130">在雙向連接中，所選存取點是否為 **Antecedent** 或 **相依** 的，並不重要。</span><span class="sxs-lookup"><span data-stu-id="35436-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="35436-131">這個屬性繼承自 [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="35436-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="35436-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="35436-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35436-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35436-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35436-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35436-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35436-135">這個屬性繼承自 [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="35436-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35436-136">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="35436-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35436-137">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="35436-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35436-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35436-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35436-139">這個屬性繼承自 [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="35436-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35436-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="35436-140">Requirements</span></span>



| <span data-ttu-id="35436-141">需求</span><span class="sxs-lookup"><span data-stu-id="35436-141">Requirement</span></span> | <span data-ttu-id="35436-142">值</span><span class="sxs-lookup"><span data-stu-id="35436-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35436-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35436-143">Minimum supported client</span></span><br/> | <span data-ttu-id="35436-144">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35436-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="35436-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35436-145">Minimum supported server</span></span><br/> | <span data-ttu-id="35436-146">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35436-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35436-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="35436-147">Namespace</span></span><br/>                | <span data-ttu-id="35436-148">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="35436-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="35436-149">MOF</span><span class="sxs-lookup"><span data-stu-id="35436-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35436-150"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="35436-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35436-151">DLL</span><span class="sxs-lookup"><span data-stu-id="35436-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35436-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35436-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

