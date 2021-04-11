---
description: 將 DH-CHAP (Diffie-hellman 的) 參數新增到虛擬機器上的綜合光纖通道埠。
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Msvm_VirtualSystemManagementService 類別的 AddFibreChannelChap 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 07151a902efa8f8077debc44bd732286c0a96a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944302"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="9b0c7-103">Msvm VirtualSystemManagementService 類別的 AddFibreChannelChap 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9b0c7-103">AddFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="9b0c7-104">將 DH-CHAP (Diffie-hellman 的) 參數新增到虛擬機器上的綜合光纖通道埠。</span><span class="sxs-lookup"><span data-stu-id="9b0c7-104">Adds DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters to a synthetic Fibre Channel port on a virtual machine.</span></span> <span data-ttu-id="9b0c7-105">如果虛擬機器正在執行，這個方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="9b0c7-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b0c7-106">語法</span><span class="sxs-lookup"><span data-stu-id="9b0c7-106">Syntax</span></span>


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a><span data-ttu-id="9b0c7-107">參數</span><span class="sxs-lookup"><span data-stu-id="9b0c7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b0c7-108">*FcPortSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b0c7-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b0c7-109">字串陣列，其中包含 [**Msvm \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) 類別的內嵌實例，描述虛擬機器的綜合光纖通道埠的設定。</span><span class="sxs-lookup"><span data-stu-id="9b0c7-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that describes settings for synthetic Fibre Channel ports for virtual machines.</span></span> <span data-ttu-id="9b0c7-110">每個實例的 **InstanceID** 屬性都會識別要修改的元素。</span><span class="sxs-lookup"><span data-stu-id="9b0c7-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="9b0c7-111">*SecretEncoding* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b0c7-111">*SecretEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b0c7-112">指定共用密碼的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="9b0c7-112">Specifies the type of encoding for the shared secret.</span></span>

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

<span data-ttu-id="9b0c7-113">**可列印的 ASCII** (1) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-113">**Printable ASCII** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="9b0c7-114">**二元** (2) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-114">**Binary** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="9b0c7-115">*SharedSecret* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b0c7-115">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b0c7-116">指定共用機密。</span><span class="sxs-lookup"><span data-stu-id="9b0c7-116">Specifies the shared secret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b0c7-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b0c7-117">Return value</span></span>

<span data-ttu-id="9b0c7-118">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9b0c7-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9b0c7-119">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9b0c7-120">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9b0c7-121">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9b0c7-122">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9b0c7-123">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9b0c7-124">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9b0c7-125">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9b0c7-126">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9b0c7-127">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9b0c7-128">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9b0c7-129">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9b0c7-130">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="9b0c7-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9b0c7-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b0c7-131">Requirements</span></span>



| <span data-ttu-id="9b0c7-132">需求</span><span class="sxs-lookup"><span data-stu-id="9b0c7-132">Requirement</span></span> | <span data-ttu-id="9b0c7-133">值</span><span class="sxs-lookup"><span data-stu-id="9b0c7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b0c7-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b0c7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9b0c7-135">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b0c7-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9b0c7-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b0c7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9b0c7-137">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b0c7-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9b0c7-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="9b0c7-138">Namespace</span></span><br/>                | <span data-ttu-id="9b0c7-139">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="9b0c7-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9b0c7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="9b0c7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b0c7-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9b0c7-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b0c7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9b0c7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b0c7-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9b0c7-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9b0c7-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b0c7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b0c7-145">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="9b0c7-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




