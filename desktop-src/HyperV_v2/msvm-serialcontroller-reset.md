---
description: 重設裝置。
ms.assetid: 4ac8ee27-0629-45aa-80ee-f308c044d7fc
title: Msvm_SerialController 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bf5fd2ff0218a4a4f39e64921e41fd497753d04e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978990"
---
# <a name="reset-method-of-the-msvm_serialcontroller-class"></a><span data-ttu-id="f800e-103">Msvm SerialController 類別的 Reset 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f800e-103">Reset method of the Msvm\_SerialController class</span></span>

<span data-ttu-id="f800e-104">重設裝置。</span><span class="sxs-lookup"><span data-stu-id="f800e-104">Resets the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f800e-105">語法</span><span class="sxs-lookup"><span data-stu-id="f800e-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="f800e-106">參數</span><span class="sxs-lookup"><span data-stu-id="f800e-106">Parameters</span></span>

<span data-ttu-id="f800e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f800e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f800e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f800e-108">Return value</span></span>

<span data-ttu-id="f800e-109">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f800e-109">Returns 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f800e-110">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="f800e-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f800e-111">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="f800e-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f800e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f800e-112">Requirements</span></span>



| <span data-ttu-id="f800e-113">需求</span><span class="sxs-lookup"><span data-stu-id="f800e-113">Requirement</span></span> | <span data-ttu-id="f800e-114">值</span><span class="sxs-lookup"><span data-stu-id="f800e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f800e-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f800e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f800e-116">Windows 8.1，版本1703</span><span class="sxs-lookup"><span data-stu-id="f800e-116">Windows 8.1, version 1703</span></span><br/>                                                                    |
| <span data-ttu-id="f800e-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f800e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f800e-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f800e-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f800e-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="f800e-119">Namespace</span></span><br/>                | <span data-ttu-id="f800e-120">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="f800e-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f800e-121">MOF</span><span class="sxs-lookup"><span data-stu-id="f800e-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f800e-122"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f800e-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f800e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f800e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f800e-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f800e-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f800e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f800e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f800e-126">**Msvm \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="f800e-126">**Msvm\_SerialController**</span></span>](msvm-serialcontroller.md)
</dt> </dl>

 

 




