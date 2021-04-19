---
description: 釋放使用 ExclusiveLock 至共用模式所取得的鎖定。
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: CShareLockNH：： ExclusiveUnlock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: f5fae5d6131bfcb386d52880b530f3def9464442
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983165"
---
# <a name="csharelocknhexclusiveunlock-method"></a><span data-ttu-id="a2856-103">CShareLockNH：： ExclusiveUnlock 方法</span><span class="sxs-lookup"><span data-stu-id="a2856-103">CShareLockNH::ExclusiveUnlock method</span></span>

<span data-ttu-id="a2856-104">釋放使用 [**ExclusiveLock**](csharelocknh--exclusivelock.md) 至共用模式所取得的鎖定。</span><span class="sxs-lookup"><span data-stu-id="a2856-104">Releases a lock acquired by using [**ExclusiveLock**](csharelocknh--exclusivelock.md) to shared mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2856-105">語法</span><span class="sxs-lookup"><span data-stu-id="a2856-105">Syntax</span></span>


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a><span data-ttu-id="a2856-106">參數</span><span class="sxs-lookup"><span data-stu-id="a2856-106">Parameters</span></span>

<span data-ttu-id="a2856-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a2856-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2856-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2856-108">Return value</span></span>

<span data-ttu-id="a2856-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a2856-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2856-110">備註</span><span class="sxs-lookup"><span data-stu-id="a2856-110">Remarks</span></span>

<span data-ttu-id="a2856-111">對 [**ExclusiveLock**](csharelocknh--exclusivelock.md) 的每個呼叫都必須成對 **ExclusiveUnlock** ，以避免發生鎖死的風險。</span><span class="sxs-lookup"><span data-stu-id="a2856-111">Each call to [**ExclusiveLock**](csharelocknh--exclusivelock.md) must be paired with exactly one call to **ExclusiveUnlock** to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="a2856-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="a2856-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2856-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2856-113">Requirements</span></span>



| <span data-ttu-id="a2856-114">需求</span><span class="sxs-lookup"><span data-stu-id="a2856-114">Requirement</span></span> | <span data-ttu-id="a2856-115">值</span><span class="sxs-lookup"><span data-stu-id="a2856-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a2856-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a2856-116">DLL</span></span><br/> | <dl> <span data-ttu-id="a2856-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2856-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2856-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2856-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2856-119">**ExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="a2856-119">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
