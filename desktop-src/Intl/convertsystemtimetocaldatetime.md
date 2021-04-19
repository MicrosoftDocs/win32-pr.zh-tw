---
description: 已取代。 將指定的 SYSTEMTIME 結構轉換成 CALDATETIME 結構。
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: ConvertSystemTimeToCalDateTime 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertSystemTimeToCalDateTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 738899c7307797f0edeade93f7e4e706919be900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998115"
---
# <a name="convertsystemtimetocaldatetime-function"></a><span data-ttu-id="bf4dc-104">ConvertSystemTimeToCalDateTime 函式</span><span class="sxs-lookup"><span data-stu-id="bf4dc-104">ConvertSystemTimeToCalDateTime function</span></span>

<span data-ttu-id="bf4dc-105">已取代。</span><span class="sxs-lookup"><span data-stu-id="bf4dc-105">Deprecated.</span></span> <span data-ttu-id="bf4dc-106">將指定的 [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) 結構轉換成 [**CALDATETIME**](caldatetime.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="bf4dc-106">Converts a specified [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to a [**CALDATETIME**](caldatetime.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf4dc-107">語法</span><span class="sxs-lookup"><span data-stu-id="bf4dc-107">Syntax</span></span>


```C++
BOOL ConvertSystemTimeToCalDateTime(
  _In_  const SYSTEMTIME   *lpSysTime,
  _In_        CALID         calId,
  _Out_       LPCALDATETIME lpCalDateTime

);
```



## <a name="parameters"></a><span data-ttu-id="bf4dc-108">參數</span><span class="sxs-lookup"><span data-stu-id="bf4dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf4dc-109">*lpSysTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf4dc-109">*lpSysTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf4dc-110">要轉換之 [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="bf4dc-110">Pointer to the [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="bf4dc-111">*calId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf4dc-111">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf4dc-112">要在轉換中使用的系統行事 [曆識別碼](calendar-identifiers.md) 。</span><span class="sxs-lookup"><span data-stu-id="bf4dc-112">The system [calendar identifier](calendar-identifiers.md) to use in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="bf4dc-113">*lpCalDateTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bf4dc-113">*lpCalDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf4dc-114">對等 [**CALDATETIME**](caldatetime.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="bf4dc-114">Pointer to the equivalent [**CALDATETIME**](caldatetime.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf4dc-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf4dc-115">Return value</span></span>

<span data-ttu-id="bf4dc-116">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="bf4dc-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="bf4dc-117">若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="bf4dc-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="bf4dc-118">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="bf4dc-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="bf4dc-119">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="bf4dc-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf4dc-120">備註</span><span class="sxs-lookup"><span data-stu-id="bf4dc-120">Remarks</span></span>

<span data-ttu-id="bf4dc-121">此函數所支援的最早日期是1601年1月1日。</span><span class="sxs-lookup"><span data-stu-id="bf4dc-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="bf4dc-122">此函數沒有相關聯的標頭檔或程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="bf4dc-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="bf4dc-123">應用程式可以使用 DLL 名稱 (Kernel32.dll) 來呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="bf4dc-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="bf4dc-124">然後，它可以使用模組控制碼和此函式的名稱來呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，以取得函數位址。</span><span class="sxs-lookup"><span data-stu-id="bf4dc-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf4dc-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf4dc-125">Requirements</span></span>



| <span data-ttu-id="bf4dc-126">需求</span><span class="sxs-lookup"><span data-stu-id="bf4dc-126">Requirement</span></span> | <span data-ttu-id="bf4dc-127">值</span><span class="sxs-lookup"><span data-stu-id="bf4dc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf4dc-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf4dc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bf4dc-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf4dc-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bf4dc-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf4dc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bf4dc-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf4dc-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf4dc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bf4dc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf4dc-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf4dc-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf4dc-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf4dc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf4dc-135">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="bf4dc-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="bf4dc-136">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="bf4dc-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="bf4dc-137">正在抓取時間和日期資訊</span><span class="sxs-lookup"><span data-stu-id="bf4dc-137">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
