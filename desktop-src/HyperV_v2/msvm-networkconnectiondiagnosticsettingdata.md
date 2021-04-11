---
description: 表示用來測試虛擬機器的網路連線能力的設定。
ms.assetid: d719d9c9-7ca9-40a0-ada8-185b8cd44c22
title: Msvm_NetworkConnectionDiagnosticSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticSettingData
- Msvm_NetworkConnectionDiagnosticSettingData.IsSender
- Msvm_NetworkConnectionDiagnosticSettingData.SenderIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverMac
- Msvm_NetworkConnectionDiagnosticSettingData.IsolationId
- Msvm_NetworkConnectionDiagnosticSettingData.SequenceNumber
- Msvm_NetworkConnectionDiagnosticSettingData.PayloadSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec0df1957df6c925cf12ce363c89a0bdad52d3e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027458"
---
# <a name="msvm_networkconnectiondiagnosticsettingdata-class"></a><span data-ttu-id="41119-103">Msvm \_ NetworkConnectionDiagnosticSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="41119-103">Msvm\_NetworkConnectionDiagnosticSettingData class</span></span>

<span data-ttu-id="41119-104">表示用來測試虛擬機器的網路連線能力的設定。</span><span class="sxs-lookup"><span data-stu-id="41119-104">Represents the settings used to test the network connectivity of a virtual machine.</span></span> <span data-ttu-id="41119-105">由 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)方法所使用。</span><span class="sxs-lookup"><span data-stu-id="41119-105">Used by the [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="41119-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="41119-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="41119-107">語法</span><span class="sxs-lookup"><span data-stu-id="41119-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticSettingData : CIM_SettingData
{
  boolean IsSender;
  string  SenderIP;
  string  ReceiverIP;
  string  ReceiverMac;
  uint32  IsolationId;
  uint32  SequenceNumber;
  uint32  PayloadSize;
};
```

## <a name="members"></a><span data-ttu-id="41119-108">成員</span><span class="sxs-lookup"><span data-stu-id="41119-108">Members</span></span>

<span data-ttu-id="41119-109">**Msvm \_ NetworkConnectionDiagnosticSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="41119-109">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="41119-110">屬性</span><span class="sxs-lookup"><span data-stu-id="41119-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41119-111">屬性</span><span class="sxs-lookup"><span data-stu-id="41119-111">Properties</span></span>

<span data-ttu-id="41119-112">**Msvm \_ NetworkConnectionDiagnosticSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="41119-112">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41119-113">**IsolationId**</span><span class="sxs-lookup"><span data-stu-id="41119-113">**IsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41119-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41119-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41119-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41119-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="41119-116">隔離識別碼。</span><span class="sxs-lookup"><span data-stu-id="41119-116">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="41119-117">**IsSender**</span><span class="sxs-lookup"><span data-stu-id="41119-117">**IsSender**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41119-118">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="41119-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41119-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41119-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="41119-120">指出是否要在傳送者端或接收者叫用此方法。</span><span class="sxs-lookup"><span data-stu-id="41119-120">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="41119-121">**PayloadSize**</span><span class="sxs-lookup"><span data-stu-id="41119-121">**PayloadSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41119-122">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41119-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41119-123">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41119-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="41119-124">承載大小。</span><span class="sxs-lookup"><span data-stu-id="41119-124">The payload size.</span></span>

</dd> <dt>

<span data-ttu-id="41119-125">**ReceiverIP**</span><span class="sxs-lookup"><span data-stu-id="41119-125">**ReceiverIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41119-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="41119-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41119-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41119-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="41119-128">接收者 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="41119-128">The receiver IP address.</span></span>

</dd> <dt>

<span data-ttu-id="41119-129">**ReceiverMac**</span><span class="sxs-lookup"><span data-stu-id="41119-129">**ReceiverMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41119-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="41119-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41119-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41119-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="41119-132">接收者 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="41119-132">The receiver MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="41119-133">**SenderIP**</span><span class="sxs-lookup"><span data-stu-id="41119-133">**SenderIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41119-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="41119-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41119-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41119-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="41119-136">寄件者 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="41119-136">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="41119-137">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="41119-137">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41119-138">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41119-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41119-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41119-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="41119-140">序號。</span><span class="sxs-lookup"><span data-stu-id="41119-140">The sequence number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41119-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="41119-141">Requirements</span></span>



| <span data-ttu-id="41119-142">需求</span><span class="sxs-lookup"><span data-stu-id="41119-142">Requirement</span></span> | <span data-ttu-id="41119-143">值</span><span class="sxs-lookup"><span data-stu-id="41119-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41119-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41119-144">Minimum supported client</span></span><br/> | <span data-ttu-id="41119-145">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41119-145">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="41119-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41119-146">Minimum supported server</span></span><br/> | <span data-ttu-id="41119-147">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="41119-147">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="41119-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="41119-148">Namespace</span></span><br/>                | <span data-ttu-id="41119-149">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="41119-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="41119-150">MOF</span><span class="sxs-lookup"><span data-stu-id="41119-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41119-151"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="41119-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41119-152">DLL</span><span class="sxs-lookup"><span data-stu-id="41119-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41119-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41119-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="41119-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41119-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41119-155">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="41119-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




