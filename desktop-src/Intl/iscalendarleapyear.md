---
description: 已取代。 識別指定的年份是否為特定行事曆在指定紀元內的閏年。
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: IsCalendarLeapYear 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCalendarLeapYear
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 484531f8107bacb70f9e24ba2537090317825e26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849477"
---
# <a name="iscalendarleapyear-function"></a><span data-ttu-id="905fd-104">IsCalendarLeapYear 函式</span><span class="sxs-lookup"><span data-stu-id="905fd-104">IsCalendarLeapYear function</span></span>

<span data-ttu-id="905fd-105">已取代。</span><span class="sxs-lookup"><span data-stu-id="905fd-105">Deprecated.</span></span> <span data-ttu-id="905fd-106">識別指定的年份是否為特定行事曆在指定紀元內的閏年。</span><span class="sxs-lookup"><span data-stu-id="905fd-106">Identifies whether the specified year is a leap year within the given era for the specific calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="905fd-107">語法</span><span class="sxs-lookup"><span data-stu-id="905fd-107">Syntax</span></span>


```C++
BOOL IsCalendarLeapYear(
  _In_ CALID calId,
  _In_ UINT  year,
  _In_ UINT  era
);
```



## <a name="parameters"></a><span data-ttu-id="905fd-108">參數</span><span class="sxs-lookup"><span data-stu-id="905fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="905fd-109">*calId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="905fd-109">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="905fd-110">要用於檢查閏年度的行事 [曆識別碼](calendar-identifiers.md) 。</span><span class="sxs-lookup"><span data-stu-id="905fd-110">The [calendar identifier](calendar-identifiers.md) to use for checking leap year.</span></span>

</dd> <dt>

<span data-ttu-id="905fd-111">*年* \[在\]</span><span class="sxs-lookup"><span data-stu-id="905fd-111">*year* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="905fd-112">要檢查的年份。</span><span class="sxs-lookup"><span data-stu-id="905fd-112">The year to check.</span></span>

</dd> <dt>

<span data-ttu-id="905fd-113">*紀元* \[在\]</span><span class="sxs-lookup"><span data-stu-id="905fd-113">*era* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="905fd-114">要檢查的紀元。</span><span class="sxs-lookup"><span data-stu-id="905fd-114">The era to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="905fd-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="905fd-115">Return value</span></span>

<span data-ttu-id="905fd-116">如果指定的年份為閏年，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="905fd-116">Returns **TRUE** if the specified year is a leap year, or **FALSE** otherwise.</span></span> <span data-ttu-id="905fd-117">若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="905fd-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="905fd-118">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="905fd-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="905fd-119">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="905fd-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="905fd-120">備註</span><span class="sxs-lookup"><span data-stu-id="905fd-120">Remarks</span></span>

<span data-ttu-id="905fd-121">此函數沒有相關聯的標頭檔或程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="905fd-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="905fd-122">應用程式可以使用 DLL 名稱 (Kernel32.dll) 來呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="905fd-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="905fd-123">然後，您可以使用該模組控制碼和此函式的名稱來呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，以取得函數位址。</span><span class="sxs-lookup"><span data-stu-id="905fd-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="905fd-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="905fd-124">Requirements</span></span>



| <span data-ttu-id="905fd-125">需求</span><span class="sxs-lookup"><span data-stu-id="905fd-125">Requirement</span></span> | <span data-ttu-id="905fd-126">值</span><span class="sxs-lookup"><span data-stu-id="905fd-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="905fd-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="905fd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="905fd-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="905fd-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="905fd-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="905fd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="905fd-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="905fd-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="905fd-131">DLL</span><span class="sxs-lookup"><span data-stu-id="905fd-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="905fd-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="905fd-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="905fd-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="905fd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="905fd-134">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="905fd-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="905fd-135">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="905fd-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> </dl>

 

 
