---
description: 提供有關虛擬機器之網路連線能力的資訊。
ms.assetid: 59503c1b-203b-46ec-8a65-f21a746f170f
title: Msvm_NetworkConnectionDiagnosticInformation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticInformation
- Msvm_NetworkConnectionDiagnosticInformation.RoundTripTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 416392702e5bc06e54fe5a23b6784b87e98b7027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945210"
---
# <a name="msvm_networkconnectiondiagnosticinformation-class"></a><span data-ttu-id="2db81-103">Msvm \_ NetworkConnectionDiagnosticInformation 類別</span><span class="sxs-lookup"><span data-stu-id="2db81-103">Msvm\_NetworkConnectionDiagnosticInformation class</span></span>

<span data-ttu-id="2db81-104">提供有關虛擬機器之網路連線能力的資訊。</span><span class="sxs-lookup"><span data-stu-id="2db81-104">Provides information about the network connectivity for a virtual machine.</span></span>

<span data-ttu-id="2db81-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2db81-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2db81-106">語法</span><span class="sxs-lookup"><span data-stu-id="2db81-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticInformation
{
  uint32 RoundTripTime;
};
```

## <a name="members"></a><span data-ttu-id="2db81-107">成員</span><span class="sxs-lookup"><span data-stu-id="2db81-107">Members</span></span>

<span data-ttu-id="2db81-108">**Msvm \_ NetworkConnectionDiagnosticInformation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2db81-108">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="2db81-109">屬性</span><span class="sxs-lookup"><span data-stu-id="2db81-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2db81-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2db81-110">Properties</span></span>

<span data-ttu-id="2db81-111">**Msvm \_ NetworkConnectionDiagnosticInformation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2db81-111">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2db81-112">**RoundTripTime**</span><span class="sxs-lookup"><span data-stu-id="2db81-112">**RoundTripTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2db81-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2db81-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2db81-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2db81-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2db81-115">Ping 要求的來回行程時間。</span><span class="sxs-lookup"><span data-stu-id="2db81-115">The round trip time for the ping request.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2db81-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2db81-116">Requirements</span></span>



| <span data-ttu-id="2db81-117">需求</span><span class="sxs-lookup"><span data-stu-id="2db81-117">Requirement</span></span> | <span data-ttu-id="2db81-118">值</span><span class="sxs-lookup"><span data-stu-id="2db81-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2db81-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2db81-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2db81-120">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2db81-120">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2db81-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2db81-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2db81-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2db81-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2db81-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="2db81-123">Namespace</span></span><br/>                | <span data-ttu-id="2db81-124">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="2db81-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2db81-125">MOF</span><span class="sxs-lookup"><span data-stu-id="2db81-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2db81-126"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2db81-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2db81-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2db81-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2db81-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2db81-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




