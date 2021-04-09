---
description: 這個方法是用來尋找實際的保留，而輸入參數是計算保留的虛擬機器處理器數目。
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Msvm_ProcessorPool 類別的 CalculatePossibleReserve 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool.CalculatePossibleReserve
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7f88bcf3295b1792fca6be88ae0c9282b72646e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693056"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a><span data-ttu-id="012f7-103">Msvm ProcessorPool 類別的 CalculatePossibleReserve 方法 \_</span><span class="sxs-lookup"><span data-stu-id="012f7-103">CalculatePossibleReserve method of the Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="012f7-104">這個方法是用來尋找實際的保留，而輸入參數是計算保留的虛擬機器處理器數目。</span><span class="sxs-lookup"><span data-stu-id="012f7-104">This method is used to find the actual reserve with the input parameter being the number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="012f7-105">這個方法是必要的，因為處理器資源的保留會高度依賴必須以平行方式排程的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="012f7-105">This method is necessary because the reservation of processor resources is highly dependent on the number of processors which must be scheduled in parallel.</span></span>

## <a name="syntax"></a><span data-ttu-id="012f7-106">語法</span><span class="sxs-lookup"><span data-stu-id="012f7-106">Syntax</span></span>


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a><span data-ttu-id="012f7-107">參數</span><span class="sxs-lookup"><span data-stu-id="012f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="012f7-108">*ProcessorCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="012f7-108">*ProcessorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="012f7-109">類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="012f7-109">Type: **uint16**</span></span>

<span data-ttu-id="012f7-110">計算保留的虛擬機器處理器數目。</span><span class="sxs-lookup"><span data-stu-id="012f7-110">The number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="012f7-111">這個屬性的最大值是主機電腦的邏輯處理器計數。</span><span class="sxs-lookup"><span data-stu-id="012f7-111">The maximum value for this property is the logical processor count for the host computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="012f7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="012f7-112">Return value</span></span>

<span data-ttu-id="012f7-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="012f7-113">Type: **uint32**</span></span>

<span data-ttu-id="012f7-114">可能保留給虛擬機器的 CPU 資源數量。</span><span class="sxs-lookup"><span data-stu-id="012f7-114">The amount of CPU resources that may be reserved for a virtual machine.</span></span>

## <a name="remarks"></a><span data-ttu-id="012f7-115">備註</span><span class="sxs-lookup"><span data-stu-id="012f7-115">Remarks</span></span>

<span data-ttu-id="012f7-116">存取 [**Msvm \_ ProcessorPool**](msvm-processorpool.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="012f7-116">Access to the [**Msvm\_ProcessorPool**](msvm-processorpool.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="012f7-117">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="012f7-117">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="012f7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="012f7-118">Requirements</span></span>



| <span data-ttu-id="012f7-119">需求</span><span class="sxs-lookup"><span data-stu-id="012f7-119">Requirement</span></span> | <span data-ttu-id="012f7-120">值</span><span class="sxs-lookup"><span data-stu-id="012f7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="012f7-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="012f7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="012f7-122">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="012f7-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="012f7-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="012f7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="012f7-124">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="012f7-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="012f7-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="012f7-125">Namespace</span></span><br/>                | <span data-ttu-id="012f7-126">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="012f7-126">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="012f7-127">MOF</span><span class="sxs-lookup"><span data-stu-id="012f7-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="012f7-128"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="012f7-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="012f7-129">DLL</span><span class="sxs-lookup"><span data-stu-id="012f7-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="012f7-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="012f7-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="012f7-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="012f7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="012f7-132">**Msvm \_ ProcessorPool**</span><span class="sxs-lookup"><span data-stu-id="012f7-132">**Msvm\_ProcessorPool**</span></span>](msvm-processorpool.md)
</dt> </dl>

 

