---
description: Msvm_SecurityService 類別的 StopService 方法會停止服務。
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
ms.openlocfilehash: a9a16fef951fdee5ed7fc580da61f43d848a8dec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118706"
---
# <a name="stopservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="673f2-103">Msvm SecurityService 類別的 StopService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="673f2-103">StopService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="673f2-104">停止服務。</span><span class="sxs-lookup"><span data-stu-id="673f2-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="673f2-105">語法</span><span class="sxs-lookup"><span data-stu-id="673f2-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="673f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="673f2-106">Parameters</span></span>

<span data-ttu-id="673f2-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="673f2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="673f2-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="673f2-108">Return value</span></span>

<span data-ttu-id="673f2-109">成功時，會傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="673f2-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="673f2-110">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="673f2-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="673f2-111">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="673f2-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="673f2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="673f2-112">Requirements</span></span>



| <span data-ttu-id="673f2-113">需求</span><span class="sxs-lookup"><span data-stu-id="673f2-113">Requirement</span></span> | <span data-ttu-id="673f2-114">值</span><span class="sxs-lookup"><span data-stu-id="673f2-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="673f2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="673f2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="673f2-116">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="673f2-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="673f2-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="673f2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="673f2-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="673f2-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="673f2-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="673f2-119">Namespace</span></span><br/>                | <span data-ttu-id="673f2-120">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="673f2-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="673f2-121">MOF</span><span class="sxs-lookup"><span data-stu-id="673f2-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="673f2-122"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="673f2-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="673f2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="673f2-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="673f2-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="673f2-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="673f2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="673f2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673f2-126">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="673f2-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




