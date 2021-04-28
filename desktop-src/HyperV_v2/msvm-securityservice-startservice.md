---
description: Msvm_SecurityService 類別的 StartService 方法會啟動服務。
ms.assetid: 59918c15-7216-4cf7-9215-b27532febc72
title: Msvm_SecurityService 類別的 StartService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31e16eea84cf61ace11c241b6409a5810f74b8f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111396"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="c2542-103">Msvm SecurityService 類別的 StartService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c2542-103">StartService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="c2542-104">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="c2542-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2542-105">語法</span><span class="sxs-lookup"><span data-stu-id="c2542-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="c2542-106">參數</span><span class="sxs-lookup"><span data-stu-id="c2542-106">Parameters</span></span>

<span data-ttu-id="c2542-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c2542-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2542-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2542-108">Return value</span></span>

<span data-ttu-id="c2542-109">成功時，會傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c2542-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="c2542-110">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="c2542-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c2542-111">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="c2542-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c2542-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2542-112">Requirements</span></span>



| <span data-ttu-id="c2542-113">需求</span><span class="sxs-lookup"><span data-stu-id="c2542-113">Requirement</span></span> | <span data-ttu-id="c2542-114">值</span><span class="sxs-lookup"><span data-stu-id="c2542-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2542-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2542-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c2542-116">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2542-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c2542-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2542-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c2542-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c2542-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c2542-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="c2542-119">Namespace</span></span><br/>                | <span data-ttu-id="c2542-120">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c2542-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c2542-121">MOF</span><span class="sxs-lookup"><span data-stu-id="c2542-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2542-122"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c2542-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2542-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c2542-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2542-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c2542-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c2542-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2542-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2542-126">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="c2542-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




