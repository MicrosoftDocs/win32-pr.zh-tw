---
description: 產生一組全球通訊埠名稱 (WWPNs) 。
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Msvm_VirtualSystemManagementService 類別的 GenerateWwpn 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GenerateWwpn
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b0efba6a24a7e4f7e6826f91930cb69b4b54f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971251"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="50273-103">Msvm VirtualSystemManagementService 類別的 GenerateWwpn 方法 \_</span><span class="sxs-lookup"><span data-stu-id="50273-103">GenerateWwpn method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="50273-104">產生一組全球通訊埠名稱 (WWPNs) 。</span><span class="sxs-lookup"><span data-stu-id="50273-104">Generates a set of World Wide Port Names (WWPNs).</span></span> <span data-ttu-id="50273-105">WWPNs 是從 [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md)類別的 **MinimumWWPNAddress** 和 **MaximumWWPNAddress** 屬性所定義的預先設定範圍內產生的。</span><span class="sxs-lookup"><span data-stu-id="50273-105">The WWPNs are generated from within the pre-configured range defined by the **MinimumWWPNAddress** and **MaximumWWPNAddress** properties of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span> <span data-ttu-id="50273-106">如果可以產生的有效 WWPNs 數目小於所要求的數目，則 *GeneratedWwpn* 陣列中的其餘專案將會有不正確 "0000000000000000" 專案，而且傳回值會指出成功 (0) 。</span><span class="sxs-lookup"><span data-stu-id="50273-106">If the valid number of WWPNs that can be generated is less than the requested number, then the remaining entries in the *GeneratedWwpn* array will have the invalid entry of "0000000000000000" and the return value will indicate success (0).</span></span>

## <a name="syntax"></a><span data-ttu-id="50273-107">語法</span><span class="sxs-lookup"><span data-stu-id="50273-107">Syntax</span></span>


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a><span data-ttu-id="50273-108">參數</span><span class="sxs-lookup"><span data-stu-id="50273-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50273-109">*NumberOfWwpns* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50273-109">*NumberOfWwpns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50273-110">要產生的 WWPNs 數目。</span><span class="sxs-lookup"><span data-stu-id="50273-110">The number of WWPNs to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="50273-111">*GeneratedWwpn* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="50273-111">*GeneratedWwpn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50273-112">字串陣列，其中每個字串都包含產生的 WWPN。</span><span class="sxs-lookup"><span data-stu-id="50273-112">An array of strings, each of which will contain a generated WWPN.</span></span> <span data-ttu-id="50273-113">它會以字串形式格式化為 "01：23：45：67：89： ab： cd： ef"。</span><span class="sxs-lookup"><span data-stu-id="50273-113">It will be formatted in string form as "01:23:45:67:89:ab:cd:ef".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50273-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="50273-114">Return value</span></span>

<span data-ttu-id="50273-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="50273-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="50273-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="50273-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="50273-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="50273-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="50273-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="50273-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="50273-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="50273-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="50273-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="50273-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="50273-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="50273-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="50273-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="50273-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="50273-123">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="50273-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="50273-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="50273-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="50273-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="50273-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="50273-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="50273-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="50273-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="50273-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="50273-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="50273-128">Requirements</span></span>



| <span data-ttu-id="50273-129">需求</span><span class="sxs-lookup"><span data-stu-id="50273-129">Requirement</span></span> | <span data-ttu-id="50273-130">值</span><span class="sxs-lookup"><span data-stu-id="50273-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50273-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50273-131">Minimum supported client</span></span><br/> | <span data-ttu-id="50273-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50273-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="50273-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50273-133">Minimum supported server</span></span><br/> | <span data-ttu-id="50273-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50273-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="50273-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="50273-135">Namespace</span></span><br/>                | <span data-ttu-id="50273-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="50273-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="50273-137">MOF</span><span class="sxs-lookup"><span data-stu-id="50273-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50273-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="50273-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="50273-139">DLL</span><span class="sxs-lookup"><span data-stu-id="50273-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50273-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="50273-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="50273-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50273-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50273-142">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="50273-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




