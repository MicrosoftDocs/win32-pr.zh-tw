---
description: 針對指定的內嵌 Msvm 錯誤實例陣列，傳回格式化的錯誤訊息字串 \_ 。
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: Msvm_VirtualSystemManagementService 類別的造成 stringbuilder.formaterror 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.FormatError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e768a6ea968d428d7809c7c322a80f3ad233aa2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970634"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="29a76-103">Msvm VirtualSystemManagementService 類別的造成 stringbuilder.formaterror 方法 \_</span><span class="sxs-lookup"><span data-stu-id="29a76-103">FormatError method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="29a76-104">針對指定的內嵌 [**Msvm \_ 錯誤**](msvm-error.md) 實例陣列，傳回格式化的錯誤訊息字串。</span><span class="sxs-lookup"><span data-stu-id="29a76-104">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="29a76-105">語法</span><span class="sxs-lookup"><span data-stu-id="29a76-105">Syntax</span></span>


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="29a76-106">參數</span><span class="sxs-lookup"><span data-stu-id="29a76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29a76-107">*錯誤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29a76-107">*Errors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29a76-108">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="29a76-108">Type: **string\[\]**</span></span>

<span data-ttu-id="29a76-109">字串陣列，其中包含用來產生輸出錯誤訊息的 [**Msvm \_ 錯誤**](msvm-error.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="29a76-109">An array of strings containing [**Msvm\_Error**](msvm-error.md) instances used to generate the output error message.</span></span>

</dd> <dt>

<span data-ttu-id="29a76-110">*ErrorMessage* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="29a76-110">*ErrorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29a76-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="29a76-111">Type: **string**</span></span>

<span data-ttu-id="29a76-112">在輸出中，包含由 *錯誤* 參數中傳遞的 [**Msvm \_ 錯誤**](msvm-error.md)實例所代表之串連錯誤訊息的字串。</span><span class="sxs-lookup"><span data-stu-id="29a76-112">On output, a string that contains the concatenated error messages represented by the [**Msvm\_Error**](msvm-error.md) instances passed in the *Errors* parameter.</span></span> <span data-ttu-id="29a76-113">每個錯誤字串都會以一對換行字元分隔 ( ' \\ n ' ) 。</span><span class="sxs-lookup"><span data-stu-id="29a76-113">Each error string is separated by a pair of newline characters ('\\n').</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29a76-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="29a76-114">Return value</span></span>

<span data-ttu-id="29a76-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="29a76-115">Type: **uint32**</span></span>

<span data-ttu-id="29a76-116">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="29a76-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="29a76-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="29a76-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="29a76-118">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="29a76-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="29a76-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="29a76-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="29a76-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="29a76-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="29a76-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="29a76-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="29a76-122">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="29a76-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="29a76-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="29a76-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="29a76-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="29a76-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="29a76-125">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="29a76-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="29a76-126">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="29a76-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="29a76-127">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="29a76-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="29a76-128">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="29a76-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="29a76-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="29a76-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="29a76-130">備註</span><span class="sxs-lookup"><span data-stu-id="29a76-130">Remarks</span></span>

<span data-ttu-id="29a76-131">存取 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="29a76-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="29a76-132">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="29a76-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="29a76-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="29a76-133">Requirements</span></span>



| <span data-ttu-id="29a76-134">需求</span><span class="sxs-lookup"><span data-stu-id="29a76-134">Requirement</span></span> | <span data-ttu-id="29a76-135">值</span><span class="sxs-lookup"><span data-stu-id="29a76-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29a76-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29a76-136">Minimum supported client</span></span><br/> | <span data-ttu-id="29a76-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29a76-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="29a76-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29a76-138">Minimum supported server</span></span><br/> | <span data-ttu-id="29a76-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29a76-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="29a76-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="29a76-140">Namespace</span></span><br/>                | <span data-ttu-id="29a76-141">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="29a76-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="29a76-142">MOF</span><span class="sxs-lookup"><span data-stu-id="29a76-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29a76-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="29a76-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="29a76-144">DLL</span><span class="sxs-lookup"><span data-stu-id="29a76-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29a76-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="29a76-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="29a76-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29a76-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29a76-147">**造成 stringbuilder.formaterror (V1)**</span><span class="sxs-lookup"><span data-stu-id="29a76-147">**FormatError (V1)**</span></span>](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="29a76-148">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="29a76-148">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

