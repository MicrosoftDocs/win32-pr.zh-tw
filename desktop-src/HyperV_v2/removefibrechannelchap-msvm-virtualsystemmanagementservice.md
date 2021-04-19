---
description: 從虛擬機器中的綜合光纖通道埠，移除 DH-CHAP (Diffie-hellman 與挑戰交握驗證通訊協定) 參數。
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Msvm_VirtualSystemManagementService 類別的 RemoveFibreChannelChap 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06e944c3c592b0b61ace8a72b5d42a801ab0f5df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972886"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="95f39-103">Msvm VirtualSystemManagementService 類別的 RemoveFibreChannelChap 方法 \_</span><span class="sxs-lookup"><span data-stu-id="95f39-103">RemoveFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="95f39-104">從虛擬機器中的綜合光纖通道埠，移除 DH-CHAP (Diffie-hellman 與挑戰交握驗證通訊協定) 參數。</span><span class="sxs-lookup"><span data-stu-id="95f39-104">Removes DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters from a synthetic Fibre Channel port in a virtual machine.</span></span> <span data-ttu-id="95f39-105">如果虛擬機器正在執行，這個方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="95f39-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f39-106">語法</span><span class="sxs-lookup"><span data-stu-id="95f39-106">Syntax</span></span>


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a><span data-ttu-id="95f39-107">參數</span><span class="sxs-lookup"><span data-stu-id="95f39-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95f39-108">*FcPortSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95f39-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95f39-109">字串陣列，其中包含 [**Msvm \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) 類別的內嵌實例，此類別會定義要從中移除 DH CHAP 參數的綜合光纖通道埠。</span><span class="sxs-lookup"><span data-stu-id="95f39-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that define the synthetic Fibre Channel ports to remove the DH-CHAP parameters from.</span></span> <span data-ttu-id="95f39-110">每個實例的 **InstanceID** 屬性都會識別要修改的元素。</span><span class="sxs-lookup"><span data-stu-id="95f39-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95f39-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="95f39-111">Return value</span></span>

<span data-ttu-id="95f39-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="95f39-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="95f39-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="95f39-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="95f39-114">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="95f39-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="95f39-115">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="95f39-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="95f39-116">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="95f39-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="95f39-117">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="95f39-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="95f39-118">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="95f39-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="95f39-119">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="95f39-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="95f39-120">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="95f39-120">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="95f39-121">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="95f39-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="95f39-122">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="95f39-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="95f39-123">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="95f39-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="95f39-124">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="95f39-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="95f39-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="95f39-125">Requirements</span></span>



| <span data-ttu-id="95f39-126">需求</span><span class="sxs-lookup"><span data-stu-id="95f39-126">Requirement</span></span> | <span data-ttu-id="95f39-127">值</span><span class="sxs-lookup"><span data-stu-id="95f39-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95f39-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95f39-128">Minimum supported client</span></span><br/> | <span data-ttu-id="95f39-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95f39-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="95f39-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95f39-130">Minimum supported server</span></span><br/> | <span data-ttu-id="95f39-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95f39-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="95f39-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="95f39-132">Namespace</span></span><br/>                | <span data-ttu-id="95f39-133">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="95f39-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="95f39-134">MOF</span><span class="sxs-lookup"><span data-stu-id="95f39-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95f39-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="95f39-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95f39-136">DLL</span><span class="sxs-lookup"><span data-stu-id="95f39-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95f39-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95f39-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="95f39-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95f39-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f39-139">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="95f39-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




