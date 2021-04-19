---
description: 釋放共用鎖定。
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: CShareLockNH：： ShareUnlock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 80c4311f4bf66000440dac38da6300888a8e5d59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990187"
---
# <a name="csharelocknhshareunlock-method"></a><span data-ttu-id="9bff3-103">CShareLockNH：： ShareUnlock 方法</span><span class="sxs-lookup"><span data-stu-id="9bff3-103">CShareLockNH::ShareUnlock method</span></span>

<span data-ttu-id="9bff3-104">釋放共用鎖定。</span><span class="sxs-lookup"><span data-stu-id="9bff3-104">Releases a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bff3-105">語法</span><span class="sxs-lookup"><span data-stu-id="9bff3-105">Syntax</span></span>


```C++
void ShareUnlock();
```



## <a name="parameters"></a><span data-ttu-id="9bff3-106">參數</span><span class="sxs-lookup"><span data-stu-id="9bff3-106">Parameters</span></span>

<span data-ttu-id="9bff3-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9bff3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9bff3-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9bff3-108">Return value</span></span>

<span data-ttu-id="9bff3-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9bff3-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bff3-110">備註</span><span class="sxs-lookup"><span data-stu-id="9bff3-110">Remarks</span></span>

<span data-ttu-id="9bff3-111">每次呼叫 [**ShareLock**](csharelocknh--sharelock.md) 都必須與 **ShareUnlock** 的單一呼叫配對。</span><span class="sxs-lookup"><span data-stu-id="9bff3-111">Each call to [**ShareLock**](csharelocknh--sharelock.md) must be paired with exactly one call to **ShareUnlock**.</span></span> <span data-ttu-id="9bff3-112">只有成功呼叫 **ShareLock** 的執行緒可以呼叫 **ShareUnlock**;否則，可能會發生鎖死。</span><span class="sxs-lookup"><span data-stu-id="9bff3-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="9bff3-113">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="9bff3-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bff3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bff3-114">Requirements</span></span>



| <span data-ttu-id="9bff3-115">需求</span><span class="sxs-lookup"><span data-stu-id="9bff3-115">Requirement</span></span> | <span data-ttu-id="9bff3-116">值</span><span class="sxs-lookup"><span data-stu-id="9bff3-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9bff3-117">DLL</span><span class="sxs-lookup"><span data-stu-id="9bff3-117">DLL</span></span><br/> | <dl> <span data-ttu-id="9bff3-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bff3-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bff3-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bff3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bff3-120">**ShareLock**</span><span class="sxs-lookup"><span data-stu-id="9bff3-120">**ShareLock**</span></span>](csharelocknh--sharelock.md)
</dt> </dl>

 

 
