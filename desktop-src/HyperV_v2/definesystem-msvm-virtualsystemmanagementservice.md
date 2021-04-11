---
description: 建立新的虛擬機器實例。
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Msvm_VirtualSystemManagementService 類別的 DefineSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 965d24313607a767d546503d005a6493234b2f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193931"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="46f3d-103">Msvm VirtualSystemManagementService 類別的 DefineSystem 方法 \_</span><span class="sxs-lookup"><span data-stu-id="46f3d-103">DefineSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="46f3d-104">建立新的虛擬機器實例。</span><span class="sxs-lookup"><span data-stu-id="46f3d-104">Creates a new virtual machine instance.</span></span> <span data-ttu-id="46f3d-105">未指定的屬性將會填入預設值。</span><span class="sxs-lookup"><span data-stu-id="46f3d-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="46f3d-106">語法</span><span class="sxs-lookup"><span data-stu-id="46f3d-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="46f3d-107">參數</span><span class="sxs-lookup"><span data-stu-id="46f3d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46f3d-108">*SystemSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46f3d-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f3d-109">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="46f3d-109">Type: **string**</span></span>

<span data-ttu-id="46f3d-110">[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別的內嵌實例，可用來定義要建立之虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="46f3d-110">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is used to define the attributes of the virtual machine to be created.</span></span> <span data-ttu-id="46f3d-111">此為必要參數。</span><span class="sxs-lookup"><span data-stu-id="46f3d-111">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="46f3d-112">*ResourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46f3d-112">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f3d-113">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="46f3d-113">Type: **string\[\]**</span></span>

<span data-ttu-id="46f3d-114">許多 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) 類別的內嵌實例 (或) 的衍生類別。</span><span class="sxs-lookup"><span data-stu-id="46f3d-114">A number of embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class (or derived classes thereof).</span></span> <span data-ttu-id="46f3d-115">這些實例一起說明虛擬機器的虛擬資源。</span><span class="sxs-lookup"><span data-stu-id="46f3d-115">Together these instances describe the virtual resources of the virtual machine.</span></span> <span data-ttu-id="46f3d-116">無論是否已設定此參數，都會為虛擬機器建立一組預設的裝置。</span><span class="sxs-lookup"><span data-stu-id="46f3d-116">A default set of devices will be created for the virtual machine regardless of whether this parameter is set.</span></span> <span data-ttu-id="46f3d-117">例如，系統會自動建立處理器和記憶體，並以預設值設定。</span><span class="sxs-lookup"><span data-stu-id="46f3d-117">For example, processor and memory are automatically created and configured with default values.</span></span>

</dd> <dt>

<span data-ttu-id="46f3d-118">*ReferenceConfiguration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46f3d-118">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f3d-119">類型： **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="46f3d-119">Type: **CIM\_VirtualSystemSettingData**</span></span>

<span data-ttu-id="46f3d-120">參考虛擬機器設定的最上層物件之 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="46f3d-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is the top level object of a reference virtual machine configuration.</span></span> <span data-ttu-id="46f3d-121">如果 *SystemSettings* 和 *ResourceSettings* 參數未提供個別的資訊，則會使用參考設定來補充新虛擬機器的設定。</span><span class="sxs-lookup"><span data-stu-id="46f3d-121">The reference configuration is used to complement the configuration of the new virtual machine if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="46f3d-122">*ResultingSystem* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="46f3d-122">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46f3d-123">類型： **CIM \_** 操作一</span><span class="sxs-lookup"><span data-stu-id="46f3d-123">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="46f3d-124">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)系統類型實例的參考，代表新建立的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="46f3d-124">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly created virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="46f3d-125">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="46f3d-125">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46f3d-126">類型： **CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="46f3d-126">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="46f3d-127">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="46f3d-127">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46f3d-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="46f3d-128">Return value</span></span>

<span data-ttu-id="46f3d-129">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="46f3d-129">Type: **uint32**</span></span>

<span data-ttu-id="46f3d-130">如果這個方法是以同步方式執行，它會在成功時傳回0。</span><span class="sxs-lookup"><span data-stu-id="46f3d-130">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="46f3d-131">如果這個方法是以非同步方式執行，它會傳回4096，而 *作業* 輸出參數可以用來追蹤非同步作業的進度。</span><span class="sxs-lookup"><span data-stu-id="46f3d-131">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="46f3d-132">任何其他傳回值表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="46f3d-132">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="46f3d-133">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="46f3d-133">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="46f3d-134">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="46f3d-134">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="46f3d-135">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="46f3d-135">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="46f3d-136">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="46f3d-136">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="46f3d-137">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="46f3d-137">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="46f3d-138">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="46f3d-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="46f3d-139">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="46f3d-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="46f3d-140">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="46f3d-140">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="46f3d-141">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="46f3d-141">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="46f3d-142">備註</span><span class="sxs-lookup"><span data-stu-id="46f3d-142">Remarks</span></span>

<span data-ttu-id="46f3d-143">存取 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="46f3d-143">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="46f3d-144">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="46f3d-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="46f3d-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="46f3d-145">Requirements</span></span>



| <span data-ttu-id="46f3d-146">需求</span><span class="sxs-lookup"><span data-stu-id="46f3d-146">Requirement</span></span> | <span data-ttu-id="46f3d-147">值</span><span class="sxs-lookup"><span data-stu-id="46f3d-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46f3d-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46f3d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="46f3d-149">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46f3d-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="46f3d-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46f3d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="46f3d-151">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46f3d-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46f3d-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="46f3d-152">Namespace</span></span><br/>                | <span data-ttu-id="46f3d-153">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="46f3d-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="46f3d-154">MOF</span><span class="sxs-lookup"><span data-stu-id="46f3d-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46f3d-155"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="46f3d-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46f3d-156">DLL</span><span class="sxs-lookup"><span data-stu-id="46f3d-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46f3d-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46f3d-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="46f3d-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46f3d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f3d-159">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="46f3d-159">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

