---
description: 釋放部分鎖定，讓其他專有或部分鎖定商家現在可以進入。
ms.assetid: 95a3e0d1-4e8b-4e30-b4fd-709b9db465de
title: CShareLockNH：:P artialUnlock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 930c0f51e199c1668a70f2dd017b0280939b0710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987090"
---
# <a name="csharelocknhpartialunlock-method"></a><span data-ttu-id="03d81-103">CShareLockNH：:P artialUnlock 方法</span><span class="sxs-lookup"><span data-stu-id="03d81-103">CShareLockNH::PartialUnlock method</span></span>

<span data-ttu-id="03d81-104">釋放部分鎖定，讓其他專有或部分鎖定商家現在可以進入。</span><span class="sxs-lookup"><span data-stu-id="03d81-104">Releases a partial lock so that other exclusive or partial lock acquirers can now enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d81-105">語法</span><span class="sxs-lookup"><span data-stu-id="03d81-105">Syntax</span></span>


```C++
void PartialUnlock();
```



## <a name="parameters"></a><span data-ttu-id="03d81-106">參數</span><span class="sxs-lookup"><span data-stu-id="03d81-106">Parameters</span></span>

<span data-ttu-id="03d81-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="03d81-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03d81-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="03d81-108">Return value</span></span>

<span data-ttu-id="03d81-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="03d81-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="03d81-110">備註</span><span class="sxs-lookup"><span data-stu-id="03d81-110">Remarks</span></span>

<span data-ttu-id="03d81-111">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="03d81-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="03d81-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="03d81-112">Requirements</span></span>



| <span data-ttu-id="03d81-113">需求</span><span class="sxs-lookup"><span data-stu-id="03d81-113">Requirement</span></span> | <span data-ttu-id="03d81-114">值</span><span class="sxs-lookup"><span data-stu-id="03d81-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="03d81-115">DLL</span><span class="sxs-lookup"><span data-stu-id="03d81-115">DLL</span></span><br/> | <dl> <span data-ttu-id="03d81-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03d81-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
