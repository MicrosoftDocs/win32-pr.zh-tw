---
description: QuiesceDevice 方法已被取代，而不是與這個方法所提供的功能直接重迭的一般 RequestStateChange 方法。
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: CIM_LogicalDevice 類別的 QuiesceDevice 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 82041b36592f00bf71dc7e2d744fcf94b7a666c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320099"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="0c3b0-103">CIM LogicalDevice 類別的 QuiesceDevice 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0c3b0-103">QuiesceDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="0c3b0-104">**QuiesceDevice** 方法已被取代，而不是與這個方法所提供的功能直接重迭的一般 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="0c3b0-104">The **QuiesceDevice** method has been deprecated in lieu of the more general **RequestStateChange** method that directly overlaps with the functionality provided by this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c3b0-105">語法</span><span class="sxs-lookup"><span data-stu-id="0c3b0-105">Syntax</span></span>


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a><span data-ttu-id="0c3b0-106">參數</span><span class="sxs-lookup"><span data-stu-id="0c3b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c3b0-107">*靜止* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c3b0-107">*Quiesce* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c3b0-108">如果設定為 **TRUE** ，則會完全停止所有活動（如果 **為 FALSE** resume 活動）。</span><span class="sxs-lookup"><span data-stu-id="0c3b0-108">If set to **TRUE** then cleanly cease all activity, if **FALSE** resume activity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c3b0-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c3b0-109">Return value</span></span>

<span data-ttu-id="0c3b0-110">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c3b0-110">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c3b0-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c3b0-111">Requirements</span></span>



| <span data-ttu-id="0c3b0-112">需求</span><span class="sxs-lookup"><span data-stu-id="0c3b0-112">Requirement</span></span> | <span data-ttu-id="0c3b0-113">值</span><span class="sxs-lookup"><span data-stu-id="0c3b0-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c3b0-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c3b0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0c3b0-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0c3b0-115">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0c3b0-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c3b0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0c3b0-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0c3b0-117">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0c3b0-118">命名空間</span><span class="sxs-lookup"><span data-stu-id="0c3b0-118">Namespace</span></span><br/>                | <span data-ttu-id="0c3b0-119">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="0c3b0-119">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0c3b0-120">MOF</span><span class="sxs-lookup"><span data-stu-id="0c3b0-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c3b0-121"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0c3b0-121"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c3b0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0c3b0-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c3b0-123"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c3b0-123"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0c3b0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c3b0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c3b0-125">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="0c3b0-125">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




