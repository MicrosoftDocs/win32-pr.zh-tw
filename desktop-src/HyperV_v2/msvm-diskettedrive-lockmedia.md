---
description: 鎖定或釋放媒體。
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
ms.openlocfilehash: 4f9bce4e9e46d76c3426271af16c28026c242fa9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853416"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="bbdec-103">Msvm DisketteDrive 類別的 LockMedia 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bbdec-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="bbdec-104">鎖定或釋放媒體。</span><span class="sxs-lookup"><span data-stu-id="bbdec-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbdec-105">語法</span><span class="sxs-lookup"><span data-stu-id="bbdec-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="bbdec-106">參數</span><span class="sxs-lookup"><span data-stu-id="bbdec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbdec-107">*鎖定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbdec-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbdec-108">**true** 表示鎖定媒體; **false** 表示釋放媒體。</span><span class="sxs-lookup"><span data-stu-id="bbdec-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbdec-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="bbdec-109">Return value</span></span>

<span data-ttu-id="bbdec-110">成功時傳回 0;否則，會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="bbdec-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bbdec-111">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="bbdec-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bbdec-112">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="bbdec-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bbdec-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbdec-113">Requirements</span></span>



| <span data-ttu-id="bbdec-114">需求</span><span class="sxs-lookup"><span data-stu-id="bbdec-114">Requirement</span></span> | <span data-ttu-id="bbdec-115">值</span><span class="sxs-lookup"><span data-stu-id="bbdec-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbdec-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbdec-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bbdec-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bbdec-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="bbdec-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbdec-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bbdec-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bbdec-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="bbdec-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="bbdec-120">Namespace</span></span><br/>                | <span data-ttu-id="bbdec-121">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="bbdec-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bbdec-122">MOF</span><span class="sxs-lookup"><span data-stu-id="bbdec-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbdec-123"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="bbdec-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbdec-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bbdec-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbdec-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bbdec-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bbdec-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbdec-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbdec-127">**Msvm \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="bbdec-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




