---
description: Msvm_DisketteDrive 類別的 LockMedia 方法-鎖定或釋放媒體。
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: Msvm_DisketteDrive 類別的 LockMedia 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5f5f87354aa7c39534e8b32c8985c5d18b55caa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111972"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="87b79-103">Msvm DisketteDrive 類別的 LockMedia 方法 \_</span><span class="sxs-lookup"><span data-stu-id="87b79-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="87b79-104">鎖定或釋放媒體。</span><span class="sxs-lookup"><span data-stu-id="87b79-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="87b79-105">語法</span><span class="sxs-lookup"><span data-stu-id="87b79-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="87b79-106">參數</span><span class="sxs-lookup"><span data-stu-id="87b79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87b79-107">*鎖定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87b79-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87b79-108">**true** 表示鎖定媒體; **false** 表示釋放媒體。</span><span class="sxs-lookup"><span data-stu-id="87b79-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87b79-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="87b79-109">Return value</span></span>

<span data-ttu-id="87b79-110">成功時傳回 0;否則，會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="87b79-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="87b79-111">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="87b79-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="87b79-112">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="87b79-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="87b79-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="87b79-113">Requirements</span></span>



| <span data-ttu-id="87b79-114">需求</span><span class="sxs-lookup"><span data-stu-id="87b79-114">Requirement</span></span> | <span data-ttu-id="87b79-115">值</span><span class="sxs-lookup"><span data-stu-id="87b79-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87b79-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87b79-116">Minimum supported client</span></span><br/> | <span data-ttu-id="87b79-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="87b79-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="87b79-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87b79-118">Minimum supported server</span></span><br/> | <span data-ttu-id="87b79-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="87b79-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="87b79-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="87b79-120">Namespace</span></span><br/>                | <span data-ttu-id="87b79-121">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="87b79-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="87b79-122">MOF</span><span class="sxs-lookup"><span data-stu-id="87b79-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87b79-123"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="87b79-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87b79-124">DLL</span><span class="sxs-lookup"><span data-stu-id="87b79-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87b79-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87b79-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="87b79-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87b79-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b79-127">**Msvm \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="87b79-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




