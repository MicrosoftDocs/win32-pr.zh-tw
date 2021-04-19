---
description: 已取代。 取得對應到指定日期的星期幾，並以該值填入指定 CALDATETIME 結構中的 DayOfWeek 成員。
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: UpdateCalendarDayOfWeek 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateCalendarDayOfWeek
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 316af539e6ca0476f0f8d575a160fcd7c3219e90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975549"
---
# <a name="updatecalendardayofweek-function"></a><span data-ttu-id="606af-104">UpdateCalendarDayOfWeek 函式</span><span class="sxs-lookup"><span data-stu-id="606af-104">UpdateCalendarDayOfWeek function</span></span>

<span data-ttu-id="606af-105">已取代。</span><span class="sxs-lookup"><span data-stu-id="606af-105">Deprecated.</span></span> <span data-ttu-id="606af-106">取得對應到指定日期的星期幾，並以該值填入指定 [**CALDATETIME**](caldatetime.md)結構中的 **DayOfWeek** 成員。</span><span class="sxs-lookup"><span data-stu-id="606af-106">Gets the day of the week that corresponds to a specified day and populates the **DayOfWeek** member in the specified [**CALDATETIME**](caldatetime.md) structure with that value.</span></span>

## <a name="syntax"></a><span data-ttu-id="606af-107">語法</span><span class="sxs-lookup"><span data-stu-id="606af-107">Syntax</span></span>


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="606af-108">參數</span><span class="sxs-lookup"><span data-stu-id="606af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="606af-109">*lpCalDateTime* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="606af-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="606af-110">[**CALDATETIME**](caldatetime.md)結構的指標，其中包含要設定星期幾的日期。</span><span class="sxs-lookup"><span data-stu-id="606af-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure containing the date for which to set the day of the week.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="606af-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="606af-111">Return value</span></span>

<span data-ttu-id="606af-112">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="606af-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="606af-113">若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="606af-113">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="606af-114">錯誤 \_ 日期 \_ 超出 \_ \_ 範圍。</span><span class="sxs-lookup"><span data-stu-id="606af-114">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="606af-115">指定的日期超出範圍。</span><span class="sxs-lookup"><span data-stu-id="606af-115">The specified date was out of range.</span></span>
-   <span data-ttu-id="606af-116">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="606af-116">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="606af-117">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="606af-117">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="606af-118">備註</span><span class="sxs-lookup"><span data-stu-id="606af-118">Remarks</span></span>

<span data-ttu-id="606af-119">此函數沒有相關聯的標頭檔或程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="606af-119">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="606af-120">應用程式可以使用 DLL 名稱 (Kernel32.dll) 來呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="606af-120">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="606af-121">然後，您可以使用該模組控制碼和此函式的名稱來呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，以取得函數位址。</span><span class="sxs-lookup"><span data-stu-id="606af-121">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="606af-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="606af-122">Requirements</span></span>



| <span data-ttu-id="606af-123">需求</span><span class="sxs-lookup"><span data-stu-id="606af-123">Requirement</span></span> | <span data-ttu-id="606af-124">值</span><span class="sxs-lookup"><span data-stu-id="606af-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="606af-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="606af-125">Minimum supported client</span></span><br/> | <span data-ttu-id="606af-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="606af-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="606af-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="606af-127">Minimum supported server</span></span><br/> | <span data-ttu-id="606af-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="606af-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="606af-129">DLL</span><span class="sxs-lookup"><span data-stu-id="606af-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="606af-130"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="606af-130"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="606af-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="606af-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="606af-132">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="606af-132">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="606af-133">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="606af-133">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="606af-134">**CALDATETIME**</span><span class="sxs-lookup"><span data-stu-id="606af-134">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 
