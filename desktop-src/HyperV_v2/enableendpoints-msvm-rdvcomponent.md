---
description: 要求遠端桌面服務的虛擬裝置啟動與虛擬機器的管道連接。
ms.assetid: e53238ee-8264-416b-8855-193c28089cfa
title: Msvm_RdvComponent 類別的 EnableEndPoints 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent.EnableEndPoints
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a668e6a2605a52c7021f630145d6e4897e1c76ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191491"
---
# <a name="enableendpoints-method-of-the-msvm_rdvcomponent-class"></a><span data-ttu-id="90d3b-103">Msvm RdvComponent 類別的 EnableEndPoints 方法 \_</span><span class="sxs-lookup"><span data-stu-id="90d3b-103">EnableEndPoints method of the Msvm\_RdvComponent class</span></span>

<span data-ttu-id="90d3b-104">要求遠端桌面服務的虛擬裝置啟動與虛擬機器的管道連接。</span><span class="sxs-lookup"><span data-stu-id="90d3b-104">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="90d3b-105">語法</span><span class="sxs-lookup"><span data-stu-id="90d3b-105">Syntax</span></span>


```mof
uint32 EnableEndPoints();
```



## <a name="parameters"></a><span data-ttu-id="90d3b-106">參數</span><span class="sxs-lookup"><span data-stu-id="90d3b-106">Parameters</span></span>

<span data-ttu-id="90d3b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="90d3b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="90d3b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="90d3b-108">Return value</span></span>

<span data-ttu-id="90d3b-109">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="90d3b-109">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="90d3b-110">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="90d3b-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="90d3b-111">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="90d3b-111">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="90d3b-112">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="90d3b-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="90d3b-113">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="90d3b-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="90d3b-114">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="90d3b-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="90d3b-115">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="90d3b-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="90d3b-116">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="90d3b-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="90d3b-117">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="90d3b-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="90d3b-118">**記憶體不足** (32774) </span><span class="sxs-lookup"><span data-stu-id="90d3b-118">**Out of memory** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="90d3b-119">**找不到** 檔案 (32775) </span><span class="sxs-lookup"><span data-stu-id="90d3b-119">**File not found** (32775)</span></span>
</dt> <dt>

 <span data-ttu-id="90d3b-120"> (32776) </span><span class="sxs-lookup"><span data-stu-id="90d3b-120">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="90d3b-121"> (32777) </span><span class="sxs-lookup"><span data-stu-id="90d3b-121">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="90d3b-122"> (32778) </span><span class="sxs-lookup"><span data-stu-id="90d3b-122">(32778)</span></span>
</dt> <dt>

 <span data-ttu-id="90d3b-123"> (32779) </span><span class="sxs-lookup"><span data-stu-id="90d3b-123">(32779)</span></span>
</dt> <dt>

 <span data-ttu-id="90d3b-124"> (32780) </span><span class="sxs-lookup"><span data-stu-id="90d3b-124">(32780)</span></span>
</dt> <dt>

 <span data-ttu-id="90d3b-125"> (32781) </span><span class="sxs-lookup"><span data-stu-id="90d3b-125">(32781)</span></span>
</dt> <dt>

 <span data-ttu-id="90d3b-126"> (32782) </span><span class="sxs-lookup"><span data-stu-id="90d3b-126">(32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="90d3b-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="90d3b-127">Requirements</span></span>



| <span data-ttu-id="90d3b-128">需求</span><span class="sxs-lookup"><span data-stu-id="90d3b-128">Requirement</span></span> | <span data-ttu-id="90d3b-129">值</span><span class="sxs-lookup"><span data-stu-id="90d3b-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90d3b-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90d3b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="90d3b-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90d3b-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="90d3b-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90d3b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="90d3b-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90d3b-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90d3b-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="90d3b-134">Namespace</span></span><br/>                | <span data-ttu-id="90d3b-135">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="90d3b-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="90d3b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="90d3b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90d3b-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="90d3b-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90d3b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="90d3b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90d3b-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90d3b-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90d3b-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90d3b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90d3b-141">**Msvm \_ RdvComponent**</span><span class="sxs-lookup"><span data-stu-id="90d3b-141">**Msvm\_RdvComponent**</span></span>](msvm-rdvcomponent.md)
</dt> </dl>

 

 




