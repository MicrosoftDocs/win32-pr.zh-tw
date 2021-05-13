---
description: 設定或取得磁片區磁片配額的狀態。
title: DiskQuotaControl. QuotaState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: 3580ad47a5ec6a5d0276dc0e30a4a6463aca2fb3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843189"
---
# <a name="diskquotacontrolquotastate-property"></a><span data-ttu-id="6a488-103">DiskQuotaControl. QuotaState 屬性</span><span class="sxs-lookup"><span data-stu-id="6a488-103">DiskQuotaControl.QuotaState property</span></span>

<span data-ttu-id="6a488-104">設定或取得磁片區磁片配額的狀態。</span><span class="sxs-lookup"><span data-stu-id="6a488-104">Sets or gets the state of the volume's disk quotas.</span></span>

<span data-ttu-id="6a488-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6a488-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a488-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a488-106">Syntax</span></span>


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a><span data-ttu-id="6a488-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="6a488-107">Property value</span></span>

<span data-ttu-id="6a488-108">這個屬性可以設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6a488-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="6a488-109">狀態</span><span class="sxs-lookup"><span data-stu-id="6a488-109">State</span></span>          | <span data-ttu-id="6a488-110">值</span><span class="sxs-lookup"><span data-stu-id="6a488-110">Value</span></span> | <span data-ttu-id="6a488-111">描述</span><span class="sxs-lookup"><span data-stu-id="6a488-111">Description</span></span>               |
|----------------|-------|---------------------------|
| <span data-ttu-id="6a488-112">dqStateDisable</span><span class="sxs-lookup"><span data-stu-id="6a488-112">dqStateDisable</span></span> | <span data-ttu-id="6a488-113">0</span><span class="sxs-lookup"><span data-stu-id="6a488-113">0</span></span>     | <span data-ttu-id="6a488-114">磁片配額已停用。</span><span class="sxs-lookup"><span data-stu-id="6a488-114">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="6a488-115">dqStateTrack</span><span class="sxs-lookup"><span data-stu-id="6a488-115">dqStateTrack</span></span>   | <span data-ttu-id="6a488-116">1</span><span class="sxs-lookup"><span data-stu-id="6a488-116">1</span></span>     | <span data-ttu-id="6a488-117">磁片配額已停用。</span><span class="sxs-lookup"><span data-stu-id="6a488-117">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="6a488-118">dqStateEnforce</span><span class="sxs-lookup"><span data-stu-id="6a488-118">dqStateEnforce</span></span> | <span data-ttu-id="6a488-119">2</span><span class="sxs-lookup"><span data-stu-id="6a488-119">2</span></span>     | <span data-ttu-id="6a488-120">強制執行配額限制。</span><span class="sxs-lookup"><span data-stu-id="6a488-120">Enforce quota limit.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="6a488-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a488-121">Requirements</span></span>



| <span data-ttu-id="6a488-122">需求</span><span class="sxs-lookup"><span data-stu-id="6a488-122">Requirement</span></span> | <span data-ttu-id="6a488-123">值</span><span class="sxs-lookup"><span data-stu-id="6a488-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a488-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a488-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6a488-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a488-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6a488-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a488-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6a488-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a488-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6a488-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6a488-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a488-129"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="6a488-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a488-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a488-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a488-131">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="6a488-131">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




