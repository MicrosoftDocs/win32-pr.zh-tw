---
description: 讓偵錯工具檢查動態函數資料表資訊。
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: RtlGetFunctionTableListHead 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dde476ee9958952d85c66816a113b92529aa13e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979456"
---
# <a name="rtlgetfunctiontablelisthead-function"></a><span data-ttu-id="bba5c-103">RtlGetFunctionTableListHead 函式</span><span class="sxs-lookup"><span data-stu-id="bba5c-103">RtlGetFunctionTableListHead function</span></span>

<span data-ttu-id="bba5c-104">\[您可以在不另行通知的情況下，從 Windows 變更或移除此功能。\]</span><span class="sxs-lookup"><span data-stu-id="bba5c-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="bba5c-105">讓偵錯工具檢查動態函數資料表資訊。</span><span class="sxs-lookup"><span data-stu-id="bba5c-105">Enables a debugger to examine dynamic function table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba5c-106">語法</span><span class="sxs-lookup"><span data-stu-id="bba5c-106">Syntax</span></span>


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a><span data-ttu-id="bba5c-107">參數</span><span class="sxs-lookup"><span data-stu-id="bba5c-107">Parameters</span></span>

<span data-ttu-id="bba5c-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="bba5c-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bba5c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="bba5c-109">Return value</span></span>

<span data-ttu-id="bba5c-110">傳回函式資料表清單開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="bba5c-110">Returns a pointer to the head of the function table list.</span></span>

## <a name="remarks"></a><span data-ttu-id="bba5c-111">備註</span><span class="sxs-lookup"><span data-stu-id="bba5c-111">Remarks</span></span>

<span data-ttu-id="bba5c-112">請注意，某些定義必須有 Windows 驅動程式套件 (WDK) 標頭檔 Ntdef。</span><span class="sxs-lookup"><span data-stu-id="bba5c-112">Note that the Windows Driver Kit (WDK) header file Ntdef.h is required for some definitions.</span></span> <span data-ttu-id="bba5c-113">相關聯的匯入程式庫（Ntdll.dll）可在 WDK 中使用。</span><span class="sxs-lookup"><span data-stu-id="bba5c-113">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="bba5c-114">您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，動態連結至 Ntdll.dll。</span><span class="sxs-lookup"><span data-stu-id="bba5c-114">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="bba5c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bba5c-115">Requirements</span></span>



| <span data-ttu-id="bba5c-116">需求</span><span class="sxs-lookup"><span data-stu-id="bba5c-116">Requirement</span></span> | <span data-ttu-id="bba5c-117">值</span><span class="sxs-lookup"><span data-stu-id="bba5c-117">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bba5c-118">DLL</span><span class="sxs-lookup"><span data-stu-id="bba5c-118">DLL</span></span><br/> | <dl> <span data-ttu-id="bba5c-119"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bba5c-119"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
