---
description: 鎖定並解除鎖定可移動存取裝置中的媒體。
ms.assetid: 357ee552-82d0-4201-bcc2-0acf208e16a0
title: CIM_MediaAccessDevice 類別的 LockMedia 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 12c4aa6c6ba9e57a2ab88e58624b246fb98065f3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104027639"
---
# <a name="lockmedia-method-of-the-cim_mediaaccessdevice-class"></a><span data-ttu-id="2d2cc-103">CIM MediaAccessDevice 類別的 LockMedia 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2d2cc-103">LockMedia method of the CIM\_MediaAccessDevice class</span></span>

<span data-ttu-id="2d2cc-104">鎖定並解除鎖定可移動存取裝置中的媒體。</span><span class="sxs-lookup"><span data-stu-id="2d2cc-104">Locks and unlocks the media in a removeable access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d2cc-105">語法</span><span class="sxs-lookup"><span data-stu-id="2d2cc-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="2d2cc-106">參數</span><span class="sxs-lookup"><span data-stu-id="2d2cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d2cc-107">*鎖定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d2cc-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d2cc-108">若 **為 TRUE**，則會鎖定媒體。</span><span class="sxs-lookup"><span data-stu-id="2d2cc-108">If **TRUE**, locks the media.</span></span> <span data-ttu-id="2d2cc-109">如果 **為 FALSE**，則會釋放媒體。</span><span class="sxs-lookup"><span data-stu-id="2d2cc-109">If **FALSE**, releases the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d2cc-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d2cc-110">Return value</span></span>

<span data-ttu-id="2d2cc-111">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2d2cc-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d2cc-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d2cc-112">Requirements</span></span>



| <span data-ttu-id="2d2cc-113">需求</span><span class="sxs-lookup"><span data-stu-id="2d2cc-113">Requirement</span></span> | <span data-ttu-id="2d2cc-114">值</span><span class="sxs-lookup"><span data-stu-id="2d2cc-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d2cc-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d2cc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2d2cc-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2d2cc-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2d2cc-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d2cc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2d2cc-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2d2cc-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2d2cc-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="2d2cc-119">Namespace</span></span><br/>                | <span data-ttu-id="2d2cc-120">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="2d2cc-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2d2cc-121">MOF</span><span class="sxs-lookup"><span data-stu-id="2d2cc-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d2cc-122"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2d2cc-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d2cc-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2d2cc-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d2cc-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d2cc-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d2cc-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d2cc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d2cc-126">**CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="2d2cc-126">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




