---
description: 將共用鎖定變更為部分鎖定。
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: CShareLockNH：： SharedToPartial 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.SharedToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: a997c5a437063a4c55b74d837dc77fd506688158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977687"
---
# <a name="csharelocknhsharedtopartial-method"></a><span data-ttu-id="287ca-103">CShareLockNH：： SharedToPartial 方法</span><span class="sxs-lookup"><span data-stu-id="287ca-103">CShareLockNH::SharedToPartial method</span></span>

<span data-ttu-id="287ca-104">將共用鎖定變更為部分鎖定。</span><span class="sxs-lookup"><span data-stu-id="287ca-104">Changes a shared lock to a partial lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="287ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="287ca-105">Syntax</span></span>


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a><span data-ttu-id="287ca-106">參數</span><span class="sxs-lookup"><span data-stu-id="287ca-106">Parameters</span></span>

<span data-ttu-id="287ca-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="287ca-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="287ca-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="287ca-108">Return value</span></span>

<span data-ttu-id="287ca-109">如果已取得部分鎖定，則傳回 **TRUE** ;否則，它會傳回 **FALSE** ，而且鎖定會維持在共用模式中。</span><span class="sxs-lookup"><span data-stu-id="287ca-109">Returns **TRUE** if the partial lock is obtained; otherwise, it returns **FALSE** and the lock remains in shared mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="287ca-110">備註</span><span class="sxs-lookup"><span data-stu-id="287ca-110">Remarks</span></span>

<span data-ttu-id="287ca-111">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="287ca-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="287ca-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="287ca-112">Requirements</span></span>



| <span data-ttu-id="287ca-113">需求</span><span class="sxs-lookup"><span data-stu-id="287ca-113">Requirement</span></span> | <span data-ttu-id="287ca-114">值</span><span class="sxs-lookup"><span data-stu-id="287ca-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="287ca-115">DLL</span><span class="sxs-lookup"><span data-stu-id="287ca-115">DLL</span></span><br/> | <dl> <span data-ttu-id="287ca-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="287ca-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
