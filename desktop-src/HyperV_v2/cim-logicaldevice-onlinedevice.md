---
description: OnlineDevice 方法已被取代，而不是與這個方法所提供的功能直接重迭的一般 RequestStateChange 方法。
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: CIM_LogicalDevice 類別的 OnlineDevice 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56e5fae557198a713aec338f92ad8f2865b2c351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988972"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="7f6c8-103">CIM LogicalDevice 類別的 OnlineDevice 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7f6c8-103">OnlineDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="7f6c8-104">**OnlineDevice** 方法已被取代，而不是與這個方法所提供的功能直接重迭的一般 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="7f6c8-104">The **OnlineDevice** method has been deprecated in lieu of the more general **RequestStateChange** method that directly overlaps with the functionality provided by this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f6c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="7f6c8-105">Syntax</span></span>


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a><span data-ttu-id="7f6c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="7f6c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f6c8-107">*線上* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f6c8-107">*Online* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f6c8-108">若 **為 TRUE**，請讓裝置上線，如果是 **FALSE**，則讓裝置離線。</span><span class="sxs-lookup"><span data-stu-id="7f6c8-108">If **TRUE**, take the device online, if **FALSE**, take the device offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f6c8-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f6c8-109">Return value</span></span>

<span data-ttu-id="7f6c8-110">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7f6c8-110">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f6c8-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f6c8-111">Requirements</span></span>



| <span data-ttu-id="7f6c8-112">需求</span><span class="sxs-lookup"><span data-stu-id="7f6c8-112">Requirement</span></span> | <span data-ttu-id="7f6c8-113">值</span><span class="sxs-lookup"><span data-stu-id="7f6c8-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f6c8-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f6c8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7f6c8-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7f6c8-115">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7f6c8-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f6c8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7f6c8-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7f6c8-117">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7f6c8-118">命名空間</span><span class="sxs-lookup"><span data-stu-id="7f6c8-118">Namespace</span></span><br/>                | <span data-ttu-id="7f6c8-119">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="7f6c8-119">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7f6c8-120">MOF</span><span class="sxs-lookup"><span data-stu-id="7f6c8-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f6c8-121"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7f6c8-121"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f6c8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7f6c8-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f6c8-123"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7f6c8-123"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7f6c8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f6c8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f6c8-125">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="7f6c8-125">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




