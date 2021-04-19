---
description: 取得共用鎖定。
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: CShareLockNH：： ShareLock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: d0c77564deceab29a8bee0cbffbd477559117cbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992892"
---
# <a name="csharelocknhsharelock-method"></a><span data-ttu-id="5914d-103">CShareLockNH：： ShareLock 方法</span><span class="sxs-lookup"><span data-stu-id="5914d-103">CShareLockNH::ShareLock method</span></span>

<span data-ttu-id="5914d-104">取得共用鎖定。</span><span class="sxs-lookup"><span data-stu-id="5914d-104">Obtains a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="5914d-105">語法</span><span class="sxs-lookup"><span data-stu-id="5914d-105">Syntax</span></span>


```C++
void ShareLock();
```



## <a name="parameters"></a><span data-ttu-id="5914d-106">參數</span><span class="sxs-lookup"><span data-stu-id="5914d-106">Parameters</span></span>

<span data-ttu-id="5914d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5914d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5914d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5914d-108">Return value</span></span>

<span data-ttu-id="5914d-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5914d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5914d-110">備註</span><span class="sxs-lookup"><span data-stu-id="5914d-110">Remarks</span></span>

<span data-ttu-id="5914d-111">每次呼叫 **ShareLock** 都必須與 [**ShareUnlock**](csharelocknh--shareunlock.md)的單一呼叫配對。</span><span class="sxs-lookup"><span data-stu-id="5914d-111">Each call to **ShareLock** must be paired with exactly one call to [**ShareUnlock**](csharelocknh--shareunlock.md).</span></span> <span data-ttu-id="5914d-112">只有成功呼叫 **ShareLock** 的執行緒可以呼叫 **ShareUnlock**;否則，可能會發生鎖死。</span><span class="sxs-lookup"><span data-stu-id="5914d-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="5914d-113">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="5914d-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5914d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5914d-114">Requirements</span></span>



| <span data-ttu-id="5914d-115">需求</span><span class="sxs-lookup"><span data-stu-id="5914d-115">Requirement</span></span> | <span data-ttu-id="5914d-116">值</span><span class="sxs-lookup"><span data-stu-id="5914d-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5914d-117">DLL</span><span class="sxs-lookup"><span data-stu-id="5914d-117">DLL</span></span><br/> | <dl> <span data-ttu-id="5914d-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5914d-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5914d-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5914d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5914d-120">**ShareUnlock**</span><span class="sxs-lookup"><span data-stu-id="5914d-120">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
