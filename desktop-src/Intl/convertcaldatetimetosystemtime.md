---
description: 已取代。 將指定的 CALDATETIME 結構轉換成 SYSTEMTIME 結構。
ms.assetid: 0c3f602d-62de-4c27-95d9-d35738f3279d
title: ConvertCalDateTimeToSystemTime 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertCalDateTimeToSystemTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 9c317a31904e2d1b0b2110f6b2dc367ac3e2e0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983669"
---
# <a name="convertcaldatetimetosystemtime-function"></a><span data-ttu-id="f0b43-104">ConvertCalDateTimeToSystemTime 函式</span><span class="sxs-lookup"><span data-stu-id="f0b43-104">ConvertCalDateTimeToSystemTime function</span></span>

<span data-ttu-id="f0b43-105">已取代。</span><span class="sxs-lookup"><span data-stu-id="f0b43-105">Deprecated.</span></span> <span data-ttu-id="f0b43-106">將指定的 [**CALDATETIME**](caldatetime.md) 結構轉換成 [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) 結構。</span><span class="sxs-lookup"><span data-stu-id="f0b43-106">Converts a specified [**CALDATETIME**](caldatetime.md) structure to a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0b43-107">語法</span><span class="sxs-lookup"><span data-stu-id="f0b43-107">Syntax</span></span>


```C++
BOOL ConvertCalDateTimeToSystemTime(
  _In_  const LPCALDATETIME lpCalDateTime,
  _Out_       SYSTEMTIME    *lpSysTime
);
```



## <a name="parameters"></a><span data-ttu-id="f0b43-108">參數</span><span class="sxs-lookup"><span data-stu-id="f0b43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0b43-109">*lpCalDateTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0b43-109">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0b43-110">要轉換之 [**CALDATETIME**](caldatetime.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f0b43-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="f0b43-111">*lpSysTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f0b43-111">*lpSysTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0b43-112">對等 [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f0b43-112">Pointer to the equivalent [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0b43-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0b43-113">Return value</span></span>

<span data-ttu-id="f0b43-114">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f0b43-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="f0b43-115">若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="f0b43-115">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="f0b43-116">錯誤 \_ 日期 \_ 超出 \_ \_ 範圍。</span><span class="sxs-lookup"><span data-stu-id="f0b43-116">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="f0b43-117">指定的日期超出範圍。</span><span class="sxs-lookup"><span data-stu-id="f0b43-117">The specified date was out of range.</span></span>
-   <span data-ttu-id="f0b43-118">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="f0b43-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="f0b43-119">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="f0b43-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0b43-120">備註</span><span class="sxs-lookup"><span data-stu-id="f0b43-120">Remarks</span></span>

<span data-ttu-id="f0b43-121">此函數沒有相關聯的標頭檔或程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="f0b43-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="f0b43-122">應用程式可以使用 DLL 名稱 (Kernel32.dll) 來呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="f0b43-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="f0b43-123">然後，它可以使用模組控制碼和此函式的名稱來呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，以取得函數位址。</span><span class="sxs-lookup"><span data-stu-id="f0b43-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0b43-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0b43-124">Requirements</span></span>



| <span data-ttu-id="f0b43-125">需求</span><span class="sxs-lookup"><span data-stu-id="f0b43-125">Requirement</span></span> | <span data-ttu-id="f0b43-126">值</span><span class="sxs-lookup"><span data-stu-id="f0b43-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b43-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0b43-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f0b43-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0b43-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f0b43-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0b43-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f0b43-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0b43-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0b43-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f0b43-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0b43-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0b43-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0b43-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0b43-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0b43-134">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="f0b43-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="f0b43-135">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="f0b43-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="f0b43-136">正在抓取時間和日期資訊</span><span class="sxs-lookup"><span data-stu-id="f0b43-136">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
