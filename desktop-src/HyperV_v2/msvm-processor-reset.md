---
description: 要求重設。
ms.assetid: c69b5c65-8f00-48ed-8602-7e0c5a76653d
title: Msvm_Processor 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Processor.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aaa0c74ac71e4c3d1be4b9580353c15f5ed94dca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982458"
---
# <a name="reset-method-of-the-msvm_processor-class"></a><span data-ttu-id="33b1f-103">Msvm Processor 類別的 Reset 方法 \_</span><span class="sxs-lookup"><span data-stu-id="33b1f-103">Reset method of the Msvm\_Processor class</span></span>

<span data-ttu-id="33b1f-104">要求重設。</span><span class="sxs-lookup"><span data-stu-id="33b1f-104">Requests a reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="33b1f-105">語法</span><span class="sxs-lookup"><span data-stu-id="33b1f-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="33b1f-106">參數</span><span class="sxs-lookup"><span data-stu-id="33b1f-106">Parameters</span></span>

<span data-ttu-id="33b1f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="33b1f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="33b1f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="33b1f-108">Return value</span></span>

<span data-ttu-id="33b1f-109">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="33b1f-109">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="33b1f-110">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="33b1f-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="33b1f-111">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="33b1f-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="33b1f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="33b1f-112">Requirements</span></span>



| <span data-ttu-id="33b1f-113">需求</span><span class="sxs-lookup"><span data-stu-id="33b1f-113">Requirement</span></span> | <span data-ttu-id="33b1f-114">值</span><span class="sxs-lookup"><span data-stu-id="33b1f-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33b1f-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33b1f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="33b1f-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="33b1f-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="33b1f-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33b1f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="33b1f-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="33b1f-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="33b1f-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="33b1f-119">Namespace</span></span><br/>                | <span data-ttu-id="33b1f-120">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="33b1f-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="33b1f-121">MOF</span><span class="sxs-lookup"><span data-stu-id="33b1f-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33b1f-122"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="33b1f-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="33b1f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="33b1f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33b1f-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="33b1f-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="33b1f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33b1f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33b1f-126">**Msvm \_ 處理器**</span><span class="sxs-lookup"><span data-stu-id="33b1f-126">**Msvm\_Processor**</span></span>](msvm-processor.md)
</dt> </dl>

 

 




