---
description: Msvm_SCSIProtocolController 類別的 reset 方法-要求重設。
ms.assetid: 8de43754-19dc-4865-af6c-badcb5445167
title: Msvm_SCSIProtocolController 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SCSIProtocolController.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 40d2ea3a69d0a13b067b6bb3ca70fe18c4741715
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111466"
---
# <a name="reset-method-of-the-msvm_scsiprotocolcontroller-class"></a><span data-ttu-id="7c092-103">Msvm SCSIProtocolController 類別的 Reset 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7c092-103">Reset method of the Msvm\_SCSIProtocolController class</span></span>

<span data-ttu-id="7c092-104">要求重設。</span><span class="sxs-lookup"><span data-stu-id="7c092-104">Requests a reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c092-105">語法</span><span class="sxs-lookup"><span data-stu-id="7c092-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="7c092-106">參數</span><span class="sxs-lookup"><span data-stu-id="7c092-106">Parameters</span></span>

<span data-ttu-id="7c092-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7c092-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c092-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c092-108">Return value</span></span>

<span data-ttu-id="7c092-109">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="7c092-109">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="7c092-110">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="7c092-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7c092-111">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="7c092-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7c092-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c092-112">Requirements</span></span>



| <span data-ttu-id="7c092-113">需求</span><span class="sxs-lookup"><span data-stu-id="7c092-113">Requirement</span></span> | <span data-ttu-id="7c092-114">值</span><span class="sxs-lookup"><span data-stu-id="7c092-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c092-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c092-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7c092-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7c092-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7c092-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c092-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7c092-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7c092-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7c092-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="7c092-119">Namespace</span></span><br/>                | <span data-ttu-id="7c092-120">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="7c092-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7c092-121">MOF</span><span class="sxs-lookup"><span data-stu-id="7c092-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c092-122"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7c092-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c092-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7c092-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c092-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7c092-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7c092-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c092-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c092-126">**Msvm \_ SCSIProtocolController**</span><span class="sxs-lookup"><span data-stu-id="7c092-126">**Msvm\_SCSIProtocolController**</span></span>](msvm-scsiprotocolcontroller.md)
</dt> </dl>

 

 




