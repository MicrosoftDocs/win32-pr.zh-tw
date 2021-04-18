---
description: 取得讀取器/寫入器鎖定。
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: CShareLockNH：： ExclusiveLock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8b35b544c10e6dde2887e75971d747feade5517e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976205"
---
# <a name="csharelocknhexclusivelock-method"></a><span data-ttu-id="6cc4f-103">CShareLockNH：： ExclusiveLock 方法</span><span class="sxs-lookup"><span data-stu-id="6cc4f-103">CShareLockNH::ExclusiveLock method</span></span>

<span data-ttu-id="6cc4f-104">取得讀取器/寫入器鎖定。</span><span class="sxs-lookup"><span data-stu-id="6cc4f-104">Acquires a reader/writer lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc4f-105">語法</span><span class="sxs-lookup"><span data-stu-id="6cc4f-105">Syntax</span></span>


```C++
void ExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="6cc4f-106">參數</span><span class="sxs-lookup"><span data-stu-id="6cc4f-106">Parameters</span></span>

<span data-ttu-id="6cc4f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6cc4f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6cc4f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="6cc4f-108">Return value</span></span>

<span data-ttu-id="6cc4f-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6cc4f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cc4f-110">備註</span><span class="sxs-lookup"><span data-stu-id="6cc4f-110">Remarks</span></span>

<span data-ttu-id="6cc4f-111">對 **ExclusiveLock** 的每個呼叫都必須成對 [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) ，以避免發生鎖死的風險。</span><span class="sxs-lookup"><span data-stu-id="6cc4f-111">Each call to **ExclusiveLock** must be paired with exactly one call to [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="6cc4f-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="6cc4f-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cc4f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cc4f-113">Requirements</span></span>



| <span data-ttu-id="6cc4f-114">需求</span><span class="sxs-lookup"><span data-stu-id="6cc4f-114">Requirement</span></span> | <span data-ttu-id="6cc4f-115">值</span><span class="sxs-lookup"><span data-stu-id="6cc4f-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc4f-116">DLL</span><span class="sxs-lookup"><span data-stu-id="6cc4f-116">DLL</span></span><br/> | <dl> <span data-ttu-id="6cc4f-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cc4f-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cc4f-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cc4f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc4f-119">**ExclusiveUnlock**</span><span class="sxs-lookup"><span data-stu-id="6cc4f-119">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
