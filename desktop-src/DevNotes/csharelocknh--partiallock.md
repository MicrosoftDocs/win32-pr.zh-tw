---
description: 防止一個以上的執行緒完成取得鎖定。
ms.assetid: 9cdcc6d5-b2f1-4c88-b859-1c15a80e70a9
title: CShareLockNH：:P artialLock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 0b7b7d55c9fd8d979aa14f12939df922e7a89099
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992893"
---
# <a name="csharelocknhpartiallock-method"></a><span data-ttu-id="3e440-103">CShareLockNH：:P artialLock 方法</span><span class="sxs-lookup"><span data-stu-id="3e440-103">CShareLockNH::PartialLock method</span></span>

<span data-ttu-id="3e440-104">防止一個以上的執行緒完成取得鎖定。</span><span class="sxs-lookup"><span data-stu-id="3e440-104">Prevents more than one thread from completing acquiring a lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e440-105">語法</span><span class="sxs-lookup"><span data-stu-id="3e440-105">Syntax</span></span>


```C++
void PartialLock();
```



## <a name="parameters"></a><span data-ttu-id="3e440-106">參數</span><span class="sxs-lookup"><span data-stu-id="3e440-106">Parameters</span></span>

<span data-ttu-id="3e440-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3e440-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e440-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e440-108">Return value</span></span>

<span data-ttu-id="3e440-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3e440-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e440-110">備註</span><span class="sxs-lookup"><span data-stu-id="3e440-110">Remarks</span></span>

<span data-ttu-id="3e440-111">當 **PartialLock** 生效時，呼叫 [**ShareLock**](csharelocknh--sharelock.md) 的其他執行緒可以進入鎖定。</span><span class="sxs-lookup"><span data-stu-id="3e440-111">While **PartialLock** is in effect, other threads calling [**ShareLock**](csharelocknh--sharelock.md) can enter the lock.</span></span>

<span data-ttu-id="3e440-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="3e440-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e440-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e440-113">Requirements</span></span>



| <span data-ttu-id="3e440-114">需求</span><span class="sxs-lookup"><span data-stu-id="3e440-114">Requirement</span></span> | <span data-ttu-id="3e440-115">值</span><span class="sxs-lookup"><span data-stu-id="3e440-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3e440-116">DLL</span><span class="sxs-lookup"><span data-stu-id="3e440-116">DLL</span></span><br/> | <dl> <span data-ttu-id="3e440-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e440-117"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
