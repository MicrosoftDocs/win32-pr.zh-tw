---
description: 傳回指定之虛擬機器定義檔的虛擬機器摘要資訊。
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: Msvm_VirtualSystemManagementService 類別的 GetDefinitionFileSummaryInformation 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a46daedd282d07c2367931a9f20a7fbfa1849f9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985612"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a6414-103">Msvm VirtualSystemManagementService 類別的 GetDefinitionFileSummaryInformation 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a6414-103">GetDefinitionFileSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a6414-104">傳回指定之虛擬機器定義檔的虛擬機器摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="a6414-104">Returns virtual machine summary information for the specified virtual machine definition files.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6414-105">語法</span><span class="sxs-lookup"><span data-stu-id="a6414-105">Syntax</span></span>


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="a6414-106">參數</span><span class="sxs-lookup"><span data-stu-id="a6414-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6414-107">*DefinitionFiles* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6414-107">*DefinitionFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6414-108">要傳回摘要資訊之 XML 設定檔的路徑陣列。</span><span class="sxs-lookup"><span data-stu-id="a6414-108">An array of paths to XML configuration files for which to return summary information.</span></span>

</dd> <dt>

<span data-ttu-id="a6414-109">*SummaryInformation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a6414-109">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6414-110">[**Msvm \_ SummaryInformationBase**](msvm-summaryinformation.md)實例的陣列，其中包含 *DefinitionFiles* 陣列中所指定之虛擬機器和（或）快照的要求資訊。</span><span class="sxs-lookup"><span data-stu-id="a6414-110">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformation.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *DefinitionFiles* array.</span></span> <span data-ttu-id="a6414-111">只會傳回 **Name**、 **ElementName**、 **CreationTime** 和 **Notes** 屬性，其他所有屬性都是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a6414-111">Only the **Name**, **ElementName**, **CreationTime**, and **Notes** properties are returned, all other properties will be **Null**.</span></span>

> [!Note]  

 

<span data-ttu-id="a6414-112">在 Windows 10 之前，版本1703，datatype 是 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)。</span><span class="sxs-lookup"><span data-stu-id="a6414-112">Prior to Windows 10, version 1703, datatype was [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6414-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6414-113">Return value</span></span>

<span data-ttu-id="a6414-114">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a6414-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a6414-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="a6414-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a6414-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="a6414-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a6414-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="a6414-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a6414-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="a6414-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a6414-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="a6414-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a6414-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="a6414-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a6414-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="a6414-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a6414-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="a6414-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a6414-123">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="a6414-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a6414-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="a6414-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a6414-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="a6414-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a6414-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="a6414-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a6414-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="a6414-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a6414-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6414-128">Requirements</span></span>



| <span data-ttu-id="a6414-129">需求</span><span class="sxs-lookup"><span data-stu-id="a6414-129">Requirement</span></span> | <span data-ttu-id="a6414-130">值</span><span class="sxs-lookup"><span data-stu-id="a6414-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6414-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6414-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a6414-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6414-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a6414-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6414-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a6414-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6414-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6414-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="a6414-135">Namespace</span></span><br/>                | <span data-ttu-id="a6414-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a6414-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a6414-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a6414-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6414-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a6414-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6414-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a6414-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6414-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a6414-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a6414-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6414-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6414-142">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a6414-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




