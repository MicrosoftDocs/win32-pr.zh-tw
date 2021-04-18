---
title: SystemRestore 類別的 GetLastRestoreStatus 方法
description: 捕獲上次系統還原的狀態。
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- GetLastRestoreStatus 方法系統還原
- GetLastRestoreStatus 方法系統還原，SystemRestore 類別
- SystemRestore 類別系統還原，GetLastRestoreStatus 方法
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965468"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a><span data-ttu-id="4321c-106">SystemRestore 類別的 GetLastRestoreStatus 方法</span><span class="sxs-lookup"><span data-stu-id="4321c-106">GetLastRestoreStatus method of the SystemRestore class</span></span>

<span data-ttu-id="4321c-107">捕獲上次系統還原的狀態。</span><span class="sxs-lookup"><span data-stu-id="4321c-107">Retrieves the status of the last system restore.</span></span>

## <a name="syntax"></a><span data-ttu-id="4321c-108">語法</span><span class="sxs-lookup"><span data-stu-id="4321c-108">Syntax</span></span>


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a><span data-ttu-id="4321c-109">參數</span><span class="sxs-lookup"><span data-stu-id="4321c-109">Parameters</span></span>

<span data-ttu-id="4321c-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4321c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4321c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4321c-111">Return value</span></span>

<span data-ttu-id="4321c-112">方法會傳回下列其中一個狀態值。</span><span class="sxs-lookup"><span data-stu-id="4321c-112">The method returns one of the following status values.</span></span>



| <span data-ttu-id="4321c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4321c-113">Return value</span></span>                                                                 | <span data-ttu-id="4321c-114">描述</span><span class="sxs-lookup"><span data-stu-id="4321c-114">Description</span></span>                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4321c-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4321c-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="4321c-116">上次還原失敗。</span><span class="sxs-lookup"><span data-stu-id="4321c-116">The last restore failed.</span></span><br/>          |
| <dl> <span data-ttu-id="4321c-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4321c-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="4321c-118">上次還原成功。</span><span class="sxs-lookup"><span data-stu-id="4321c-118">The last restore was successful.</span></span><br/>  |
| <dl> <span data-ttu-id="4321c-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4321c-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="4321c-120">上次還原已中斷。</span><span class="sxs-lookup"><span data-stu-id="4321c-120">The last restore was interrupted.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="4321c-121">範例</span><span class="sxs-lookup"><span data-stu-id="4321c-121">Examples</span></span>


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
End If
```



## <a name="requirements"></a><span data-ttu-id="4321c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4321c-122">Requirements</span></span>



| <span data-ttu-id="4321c-123">需求</span><span class="sxs-lookup"><span data-stu-id="4321c-123">Requirement</span></span> | <span data-ttu-id="4321c-124">值</span><span class="sxs-lookup"><span data-stu-id="4321c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4321c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4321c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4321c-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4321c-126">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4321c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4321c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4321c-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="4321c-128">None supported</span></span><br/>                                                         |
| <span data-ttu-id="4321c-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="4321c-129">Namespace</span></span><br/>                | <span data-ttu-id="4321c-130">根 \\ 預設值</span><span class="sxs-lookup"><span data-stu-id="4321c-130">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="4321c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4321c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4321c-132"><dt>Sr-iov</dt></span><span class="sxs-lookup"><span data-stu-id="4321c-132"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4321c-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4321c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4321c-134">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="4321c-134">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





