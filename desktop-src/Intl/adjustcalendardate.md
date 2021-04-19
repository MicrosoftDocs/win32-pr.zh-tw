---
description: 已取代。 以指定的年、月、周或日數來調整日期。
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: AdjustCalendarDate 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: ce2f61fd7d7d6354130873b5b2b2376c856e3958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972198"
---
# <a name="adjustcalendardate-function"></a><span data-ttu-id="c0993-104">AdjustCalendarDate 函式</span><span class="sxs-lookup"><span data-stu-id="c0993-104">AdjustCalendarDate function</span></span>

<span data-ttu-id="c0993-105">已取代。</span><span class="sxs-lookup"><span data-stu-id="c0993-105">Deprecated.</span></span> <span data-ttu-id="c0993-106">以指定的年、月、周或日數來調整日期。</span><span class="sxs-lookup"><span data-stu-id="c0993-106">Adjusts a date by a specified number of years, months, weeks, or days.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0993-107">語法</span><span class="sxs-lookup"><span data-stu-id="c0993-107">Syntax</span></span>


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a><span data-ttu-id="c0993-108">參數</span><span class="sxs-lookup"><span data-stu-id="c0993-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0993-109">*lpCalDateTime* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c0993-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0993-110">[**CALDATETIME**](caldatetime.md)結構的指標，其中包含要調整的日期和行事曆資訊。</span><span class="sxs-lookup"><span data-stu-id="c0993-110">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to adjust.</span></span>

</dd> <dt>

<span data-ttu-id="c0993-111">*calUnit* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c0993-111">*calUnit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0993-112">指出日期單位的 [**CALDATETIME \_ DATEUNIT**](caldatetime-dateunit.md) 列舉值，例如 DayUnit。</span><span class="sxs-lookup"><span data-stu-id="c0993-112">The [**CALDATETIME\_DATEUNIT**](caldatetime-dateunit.md) enumeration value indicating the date unit, for example, DayUnit.</span></span>

</dd> <dt>

<span data-ttu-id="c0993-113">*金額* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c0993-113">*amount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0993-114">用來調整指定日期的量。</span><span class="sxs-lookup"><span data-stu-id="c0993-114">The amount by which to adjust the specified date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0993-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0993-115">Return value</span></span>

<span data-ttu-id="c0993-116">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c0993-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="c0993-117">若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="c0993-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="c0993-118">錯誤 \_ 日期 \_ 超出 \_ \_ 範圍。</span><span class="sxs-lookup"><span data-stu-id="c0993-118">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="c0993-119">指定的日期超出範圍。</span><span class="sxs-lookup"><span data-stu-id="c0993-119">The specified date was out of range.</span></span>
-   <span data-ttu-id="c0993-120">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="c0993-120">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="c0993-121">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="c0993-121">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0993-122">備註</span><span class="sxs-lookup"><span data-stu-id="c0993-122">Remarks</span></span>

<span data-ttu-id="c0993-123">此函數沒有相關聯的標頭檔或程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="c0993-123">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="c0993-124">應用程式可以使用 DLL 名稱 (Kernel32.dll) 來呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="c0993-124">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="c0993-125">然後，它可以使用模組控制碼和此函式的名稱來呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，以取得函數位址。</span><span class="sxs-lookup"><span data-stu-id="c0993-125">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0993-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0993-126">Requirements</span></span>



| <span data-ttu-id="c0993-127">需求</span><span class="sxs-lookup"><span data-stu-id="c0993-127">Requirement</span></span> | <span data-ttu-id="c0993-128">值</span><span class="sxs-lookup"><span data-stu-id="c0993-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0993-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0993-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c0993-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0993-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c0993-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0993-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c0993-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0993-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0993-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c0993-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0993-134"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0993-134"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0993-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0993-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0993-136">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="c0993-136">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="c0993-137">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="c0993-137">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="c0993-138">NLS：以名稱為基礎的 Api 範例</span><span class="sxs-lookup"><span data-stu-id="c0993-138">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
