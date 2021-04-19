---
description: GetDllVersion 函式會捕獲 Cabinet.dll 的版本號碼。
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: GetDllVersion 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 1b1142bd2ece965a3f2fc58b6bb2f90586a8b391
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982983"
---
# <a name="getdllversion-function"></a><span data-ttu-id="b6287-103">GetDllVersion 函式</span><span class="sxs-lookup"><span data-stu-id="b6287-103">GetDllVersion function</span></span>

<span data-ttu-id="b6287-104">\[不再支援此函式，因此無法保證其行為。</span><span class="sxs-lookup"><span data-stu-id="b6287-104">\[This function is no longer supported, so its behavior cannot be guaranteed.</span></span> <span data-ttu-id="b6287-105">\]</span><span class="sxs-lookup"><span data-stu-id="b6287-105">\]</span></span>

<span data-ttu-id="b6287-106">**GetDllVersion** 函式會捕獲 Cabinet.dll 的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="b6287-106">The **GetDllVersion** function retrieves the version number of Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6287-107">語法</span><span class="sxs-lookup"><span data-stu-id="b6287-107">Syntax</span></span>


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a><span data-ttu-id="b6287-108">參數</span><span class="sxs-lookup"><span data-stu-id="b6287-108">Parameters</span></span>

<span data-ttu-id="b6287-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="b6287-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6287-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6287-110">Return value</span></span>

<span data-ttu-id="b6287-111">檔案的版本號碼 (參閱 [VERSIONINFO 資源](../menurc/versioninfo-resource.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b6287-111">The version number of the file (see [VERSIONINFO Resource](../menurc/versioninfo-resource.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6287-112">備註</span><span class="sxs-lookup"><span data-stu-id="b6287-112">Remarks</span></span>

<span data-ttu-id="b6287-113">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="b6287-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6287-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6287-114">Requirements</span></span>



| <span data-ttu-id="b6287-115">需求</span><span class="sxs-lookup"><span data-stu-id="b6287-115">Requirement</span></span> | <span data-ttu-id="b6287-116">值</span><span class="sxs-lookup"><span data-stu-id="b6287-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6287-117">DLL</span><span class="sxs-lookup"><span data-stu-id="b6287-117">DLL</span></span><br/> | <dl> <span data-ttu-id="b6287-118"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6287-118"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6287-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6287-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6287-120">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="b6287-120">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 
