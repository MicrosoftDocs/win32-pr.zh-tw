---
description: 如果目前沒有其他鎖定，則取得獨佔鎖定。
ms.assetid: d655b89c-f2c8-4965-a21b-f539b1598296
title: CShareLockNH：： TryExclusiveLock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.TryExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8465e247807c4229821acef552e0786a5604a3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981623"
---
# <a name="csharelocknhtryexclusivelock-method"></a><span data-ttu-id="25697-103">CShareLockNH：： TryExclusiveLock 方法</span><span class="sxs-lookup"><span data-stu-id="25697-103">CShareLockNH::TryExclusiveLock method</span></span>

<span data-ttu-id="25697-104">如果目前沒有其他鎖定，則取得獨佔鎖定。</span><span class="sxs-lookup"><span data-stu-id="25697-104">Obtains a lock exclusively if no others are currently hold it.</span></span>

## <a name="syntax"></a><span data-ttu-id="25697-105">語法</span><span class="sxs-lookup"><span data-stu-id="25697-105">Syntax</span></span>


```C++
BOOL TryExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="25697-106">參數</span><span class="sxs-lookup"><span data-stu-id="25697-106">Parameters</span></span>

<span data-ttu-id="25697-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="25697-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25697-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="25697-108">Return value</span></span>

<span data-ttu-id="25697-109">如果函式成功，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="25697-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="25697-110">備註</span><span class="sxs-lookup"><span data-stu-id="25697-110">Remarks</span></span>

<span data-ttu-id="25697-111">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="25697-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="25697-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="25697-112">Requirements</span></span>



| <span data-ttu-id="25697-113">需求</span><span class="sxs-lookup"><span data-stu-id="25697-113">Requirement</span></span> | <span data-ttu-id="25697-114">值</span><span class="sxs-lookup"><span data-stu-id="25697-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="25697-115">DLL</span><span class="sxs-lookup"><span data-stu-id="25697-115">DLL</span></span><br/> | <dl> <span data-ttu-id="25697-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25697-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
