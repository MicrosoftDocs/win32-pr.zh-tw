---
description: 停止服務。
ms.assetid: cf100cea-b0e1-42e9-831e-6422aded47c5
title: Msvm_SecurityService 類別的 StopService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 68e88e2c88d4f75f4d7671c389bab0cd81d0deb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193513"
---
# <a name="stopservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="9f6da-103">Msvm SecurityService 類別的 StopService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9f6da-103">StopService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="9f6da-104">停止服務。</span><span class="sxs-lookup"><span data-stu-id="9f6da-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f6da-105">語法</span><span class="sxs-lookup"><span data-stu-id="9f6da-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="9f6da-106">參數</span><span class="sxs-lookup"><span data-stu-id="9f6da-106">Parameters</span></span>

<span data-ttu-id="9f6da-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9f6da-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f6da-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f6da-108">Return value</span></span>

<span data-ttu-id="9f6da-109">成功時，會傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9f6da-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="9f6da-110">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="9f6da-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9f6da-111">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="9f6da-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9f6da-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f6da-112">Requirements</span></span>



| <span data-ttu-id="9f6da-113">需求</span><span class="sxs-lookup"><span data-stu-id="9f6da-113">Requirement</span></span> | <span data-ttu-id="9f6da-114">值</span><span class="sxs-lookup"><span data-stu-id="9f6da-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f6da-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f6da-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9f6da-116">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f6da-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9f6da-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f6da-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9f6da-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9f6da-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9f6da-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="9f6da-119">Namespace</span></span><br/>                | <span data-ttu-id="9f6da-120">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="9f6da-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9f6da-121">MOF</span><span class="sxs-lookup"><span data-stu-id="9f6da-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f6da-122"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9f6da-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f6da-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9f6da-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f6da-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9f6da-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9f6da-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f6da-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f6da-126">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="9f6da-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




