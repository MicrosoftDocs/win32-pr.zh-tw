---
description: 鎖定或釋放媒體。
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Msvm_DVDDrive 類別的 LockMedia 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 650a868d8e25e2ccc47271e49634827fe7d3d967
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116077"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a><span data-ttu-id="6a511-103">Msvm DVDDrive 類別的 LockMedia 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6a511-103">LockMedia method of the Msvm\_DVDDrive class</span></span>

<span data-ttu-id="6a511-104">鎖定或釋放媒體。</span><span class="sxs-lookup"><span data-stu-id="6a511-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a511-105">語法</span><span class="sxs-lookup"><span data-stu-id="6a511-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="6a511-106">參數</span><span class="sxs-lookup"><span data-stu-id="6a511-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a511-107">*鎖定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a511-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a511-108">**true** 表示鎖定媒體; **false** 表示釋放媒體。</span><span class="sxs-lookup"><span data-stu-id="6a511-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a511-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a511-109">Return value</span></span>

<span data-ttu-id="6a511-110">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="6a511-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6a511-111">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="6a511-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6a511-112">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="6a511-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6a511-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a511-113">Requirements</span></span>



| <span data-ttu-id="6a511-114">需求</span><span class="sxs-lookup"><span data-stu-id="6a511-114">Requirement</span></span> | <span data-ttu-id="6a511-115">值</span><span class="sxs-lookup"><span data-stu-id="6a511-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a511-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a511-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6a511-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6a511-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6a511-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a511-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6a511-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6a511-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6a511-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="6a511-120">Namespace</span></span><br/>                | <span data-ttu-id="6a511-121">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="6a511-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6a511-122">MOF</span><span class="sxs-lookup"><span data-stu-id="6a511-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a511-123"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6a511-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a511-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6a511-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a511-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6a511-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6a511-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a511-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a511-127">**Msvm \_ DVDDrive**</span><span class="sxs-lookup"><span data-stu-id="6a511-127">**Msvm\_DVDDrive**</span></span>](msvm-dvddrive.md)
</dt> </dl>

 

 




