---
description: 將虛擬機器中執行之應用程式的健全狀況狀態回報給在相同虛擬機器中執行的 Hyper-v 整合元件。
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: IVmApplicationHealthMonitor 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: ac9f6574dd8261a120e434cc0351fd07985c71a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982319"
---
# <a name="ivmapplicationhealthmonitor-interface"></a><span data-ttu-id="b5d4a-103">IVmApplicationHealthMonitor 介面</span><span class="sxs-lookup"><span data-stu-id="b5d4a-103">IVmApplicationHealthMonitor interface</span></span>

<span data-ttu-id="b5d4a-104">將虛擬機器中執行之應用程式的健全狀況狀態回報給在相同虛擬機器中執行的 Hyper-v 整合元件。</span><span class="sxs-lookup"><span data-stu-id="b5d4a-104">Reports the health status of an application that is running in a virtual machine to the Hyper-V integration components running in the same virtual machine.</span></span> <span data-ttu-id="b5d4a-105">在虛擬機器中執行之應用程式的狀態會反映在 \[ \] [**Msvm \_ HeartbeatComponent**](msvm-heartbeatcomponent.md)類別的 OperationalStatus 1 屬性值中。</span><span class="sxs-lookup"><span data-stu-id="b5d4a-105">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span> <span data-ttu-id="b5d4a-106">此介面也會提供一種方法，以重設所有在 Hyper-v 中累積的應用程式狀態。</span><span class="sxs-lookup"><span data-stu-id="b5d4a-106">This interface also provides a way to reset all of the application state accumulated in Hyper-V.</span></span>

<span data-ttu-id="b5d4a-107">此介面是由 Windows 8 Hyper-v 整合元件所執行。</span><span class="sxs-lookup"><span data-stu-id="b5d4a-107">This interface is implemented by the Windows 8 Hyper-V integration components.</span></span> <span data-ttu-id="b5d4a-108">藉由建立 **397A2e5f-348c-482d-b9a3-57d383b483cd** CLSID 的實例，即可取得這個介面的實例。</span><span class="sxs-lookup"><span data-stu-id="b5d4a-108">An instance of this interface is obtained by creating an instance of the **397a2e5f-348c-482d-b9a3-57d383b483cd** CLSID.</span></span>

## <a name="members"></a><span data-ttu-id="b5d4a-109">成員</span><span class="sxs-lookup"><span data-stu-id="b5d4a-109">Members</span></span>

<span data-ttu-id="b5d4a-110">**IVmApplicationHealthMonitor** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="b5d4a-110">The **IVmApplicationHealthMonitor** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b5d4a-111">**IVmApplicationHealthMonitor** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b5d4a-111">**IVmApplicationHealthMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="b5d4a-112">方法</span><span class="sxs-lookup"><span data-stu-id="b5d4a-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b5d4a-113">方法</span><span class="sxs-lookup"><span data-stu-id="b5d4a-113">Methods</span></span>

<span data-ttu-id="b5d4a-114">**IVmApplicationHealthMonitor** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b5d4a-114">The **IVmApplicationHealthMonitor** interface has these methods.</span></span>



| <span data-ttu-id="b5d4a-115">方法</span><span class="sxs-lookup"><span data-stu-id="b5d4a-115">Method</span></span>                                                                                   | <span data-ttu-id="b5d4a-116">描述</span><span class="sxs-lookup"><span data-stu-id="b5d4a-116">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5d4a-117">**ResetAllApplicationState**</span><span class="sxs-lookup"><span data-stu-id="b5d4a-117">**ResetAllApplicationState**</span></span>](ivmapplicationhealthmonitor-resetallapplicationstate.md) | <span data-ttu-id="b5d4a-118">重設虛擬機器中所有應用程式的健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="b5d4a-118">Resets the health state for all applications in a virtual machine.</span></span><br/>            |
| [<span data-ttu-id="b5d4a-119">**SetApplicationState**</span><span class="sxs-lookup"><span data-stu-id="b5d4a-119">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)           | <span data-ttu-id="b5d4a-120">設定在虛擬機器中執行之應用程式的健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="b5d4a-120">Sets the health state of an application that is running in a virtual machine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b5d4a-121">備註</span><span class="sxs-lookup"><span data-stu-id="b5d4a-121">Remarks</span></span>

<span data-ttu-id="b5d4a-122">若要使用這個程式設計項目，Windows 8 的整合元件必須安裝在執行應用程式的虛擬機器上。</span><span class="sxs-lookup"><span data-stu-id="b5d4a-122">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d4a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5d4a-123">Requirements</span></span>



| <span data-ttu-id="b5d4a-124">需求</span><span class="sxs-lookup"><span data-stu-id="b5d4a-124">Requirement</span></span> | <span data-ttu-id="b5d4a-125">值</span><span class="sxs-lookup"><span data-stu-id="b5d4a-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d4a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5d4a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d4a-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5d4a-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="b5d4a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5d4a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d4a-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5d4a-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                           |
| <span data-ttu-id="b5d4a-130">版本</span><span class="sxs-lookup"><span data-stu-id="b5d4a-130">Version</span></span><br/>                  | <span data-ttu-id="b5d4a-131">Windows 8 的整合元件</span><span class="sxs-lookup"><span data-stu-id="b5d4a-131">Integration components for Windows 8</span></span><br/>                                                                                                                                |
| <span data-ttu-id="b5d4a-132">Idl</span><span class="sxs-lookup"><span data-stu-id="b5d4a-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5d4a-133"><dt>VmApplicationHealthMonitor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5d4a-133"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="b5d4a-134">IID</span><span class="sxs-lookup"><span data-stu-id="b5d4a-134">IID</span></span><br/>                      | <span data-ttu-id="b5d4a-135">IID \_ IVmApplicationHealthMonitor 定義為267a0284-848f-447e-a096-5e10a1a76bca</span><span class="sxs-lookup"><span data-stu-id="b5d4a-135">IID\_IVmApplicationHealthMonitor is defined as 267a0284-848f-447e-a096-5e10a1a76bca</span></span><br/> <span data-ttu-id="b5d4a-136">物件識別碼定義為397a2e5f-348c-482d-b9a3-57d383b483cd</span><span class="sxs-lookup"><span data-stu-id="b5d4a-136">Object Identifier is defined as 397a2e5f-348c-482d-b9a3-57d383b483cd</span></span><br/> |



 

