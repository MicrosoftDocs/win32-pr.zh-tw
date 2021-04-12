---
description: 要求重設 LogicalDevice。
ms.assetid: f7655825-3de5-421f-a3e9-97d2f605affd
title: " (Hyper-v 管理的 CIM_LogicalDevice 類別重設方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 851332103143e84863762d8cc1183ec3ad841ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320095"
---
# <a name="reset-method-of-the-cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="3a26d-103"> (Hyper-v 管理的 CIM_LogicalDevice 類別重設方法) </span><span class="sxs-lookup"><span data-stu-id="3a26d-103">Reset method of the CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="3a26d-104">要求重設 LogicalDevice。</span><span class="sxs-lookup"><span data-stu-id="3a26d-104">Requests a reset of the LogicalDevice.</span></span> <span data-ttu-id="3a26d-105">在子類別中，可以使用方法上的 ValueMap 辨識符號來指定可能的傳回碼集。</span><span class="sxs-lookup"><span data-stu-id="3a26d-105">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="3a26d-106">您也可以在子類別中，以值陣列限定詞的形式指定可將 ValueMap 內容「轉譯」的字串。</span><span class="sxs-lookup"><span data-stu-id="3a26d-106">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a26d-107">語法</span><span class="sxs-lookup"><span data-stu-id="3a26d-107">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="3a26d-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a26d-108">Parameters</span></span>

<span data-ttu-id="3a26d-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3a26d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a26d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a26d-110">Return value</span></span>

<span data-ttu-id="3a26d-111">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a26d-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a26d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a26d-112">Requirements</span></span>



| <span data-ttu-id="3a26d-113">需求</span><span class="sxs-lookup"><span data-stu-id="3a26d-113">Requirement</span></span> | <span data-ttu-id="3a26d-114">值</span><span class="sxs-lookup"><span data-stu-id="3a26d-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a26d-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a26d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3a26d-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3a26d-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3a26d-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a26d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3a26d-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3a26d-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3a26d-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="3a26d-119">Namespace</span></span><br/>                | <span data-ttu-id="3a26d-120">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="3a26d-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3a26d-121">MOF</span><span class="sxs-lookup"><span data-stu-id="3a26d-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a26d-122"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3a26d-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a26d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3a26d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a26d-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a26d-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a26d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a26d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a26d-126">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="3a26d-126">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




