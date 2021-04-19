---
description: 指出目前的使用者是否為系統管理員。
ms.assetid: e759a6b9-19c3-4a2e-b8cf-1398037f88ee
title: pSetupIsUserAdmin 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupIsUserAdmin
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1c40a69fd682c22e2625a3ba362d11d719cf9cce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991330"
---
# <a name="psetupisuseradmin-function"></a><span data-ttu-id="5e55d-103">pSetupIsUserAdmin 函式</span><span class="sxs-lookup"><span data-stu-id="5e55d-103">pSetupIsUserAdmin function</span></span>

<span data-ttu-id="5e55d-104">\[在 Windows Vista 或 Windows Server 2008 中無法使用此功能。\]</span><span class="sxs-lookup"><span data-stu-id="5e55d-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="5e55d-105">指出目前的使用者是否為系統管理員。</span><span class="sxs-lookup"><span data-stu-id="5e55d-105">Indicates whether the current user is an administrator.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e55d-106">語法</span><span class="sxs-lookup"><span data-stu-id="5e55d-106">Syntax</span></span>


```C++
BOOL pSetupIsUserAdmin(void);
```



## <a name="parameters"></a><span data-ttu-id="5e55d-107">參數</span><span class="sxs-lookup"><span data-stu-id="5e55d-107">Parameters</span></span>

<span data-ttu-id="5e55d-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="5e55d-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e55d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e55d-109">Return value</span></span>

<span data-ttu-id="5e55d-110">如果目前的使用者是系統管理員，**則為 TRUE** ，否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5e55d-110">**TRUE** if the current user is an administrator, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e55d-111">備註</span><span class="sxs-lookup"><span data-stu-id="5e55d-111">Remarks</span></span>

<span data-ttu-id="5e55d-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="5e55d-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e55d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e55d-113">Requirements</span></span>



| <span data-ttu-id="5e55d-114">需求</span><span class="sxs-lookup"><span data-stu-id="5e55d-114">Requirement</span></span> | <span data-ttu-id="5e55d-115">值</span><span class="sxs-lookup"><span data-stu-id="5e55d-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e55d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="5e55d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="5e55d-117"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e55d-117"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
