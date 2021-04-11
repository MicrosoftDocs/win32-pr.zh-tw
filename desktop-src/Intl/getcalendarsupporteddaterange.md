---
description: 已取代。 取得指定行事曆支援的日期範圍。
ms.assetid: fe036ac5-77c0-4e83-8d70-db3fa0f7c803
title: GetCalendarSupportedDateRange 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarSupportedDateRange
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 57b1175ef7bcf5b6b5d91af63682ca565bc0f1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944661"
---
# <a name="getcalendarsupporteddaterange-function"></a><span data-ttu-id="df144-104">GetCalendarSupportedDateRange 函式</span><span class="sxs-lookup"><span data-stu-id="df144-104">GetCalendarSupportedDateRange function</span></span>

<span data-ttu-id="df144-105">已取代。</span><span class="sxs-lookup"><span data-stu-id="df144-105">Deprecated.</span></span> <span data-ttu-id="df144-106">取得指定行事曆支援的日期範圍。</span><span class="sxs-lookup"><span data-stu-id="df144-106">Gets the supported date range for a specified calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="df144-107">語法</span><span class="sxs-lookup"><span data-stu-id="df144-107">Syntax</span></span>


```C++
BOOL GetCalendarSupportedDateRange(
  _In_  CALID         Calendar,
  _Out_ LPCALDATETIME lpCalMinDateTime,
  _Out_ LPCALDATETIME lpCalMaxDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="df144-108">參數</span><span class="sxs-lookup"><span data-stu-id="df144-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df144-109">行事 *曆* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df144-109">*Calendar* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df144-110">要取得其支援日期範圍的行事[曆識別碼](calendar-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="df144-110">[Calendar identifier](calendar-identifiers.md) for which to get the supported date range.</span></span>

</dd> <dt>

<span data-ttu-id="df144-111">*lpCalMinDateTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="df144-111">*lpCalMinDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df144-112">[**CALDATETIME**](caldatetime.md)結構的指標，定義支援的最小日期。</span><span class="sxs-lookup"><span data-stu-id="df144-112">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the minimum supported date.</span></span>

</dd> <dt>

<span data-ttu-id="df144-113">*lpCalMaxDateTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="df144-113">*lpCalMaxDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df144-114">[**CALDATETIME**](caldatetime.md)結構的指標，定義支援的最大日期。</span><span class="sxs-lookup"><span data-stu-id="df144-114">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the maximum supported date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df144-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="df144-115">Return value</span></span>

<span data-ttu-id="df144-116">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="df144-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="df144-117">若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="df144-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="df144-118">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="df144-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="df144-119">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="df144-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="df144-120">備註</span><span class="sxs-lookup"><span data-stu-id="df144-120">Remarks</span></span>

<span data-ttu-id="df144-121">此函數所支援的最早日期是1601年1月1日。</span><span class="sxs-lookup"><span data-stu-id="df144-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="df144-122">此函數沒有相關聯的標頭檔或程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="df144-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="df144-123">應用程式可以使用 DLL 名稱 (Kernel32.dll) 來呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="df144-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="df144-124">然後，它可以使用模組控制碼和此函式的名稱來呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，以取得函數位址。</span><span class="sxs-lookup"><span data-stu-id="df144-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="df144-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="df144-125">Requirements</span></span>



| <span data-ttu-id="df144-126">需求</span><span class="sxs-lookup"><span data-stu-id="df144-126">Requirement</span></span> | <span data-ttu-id="df144-127">值</span><span class="sxs-lookup"><span data-stu-id="df144-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df144-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df144-128">Minimum supported client</span></span><br/> | <span data-ttu-id="df144-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df144-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="df144-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df144-130">Minimum supported server</span></span><br/> | <span data-ttu-id="df144-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df144-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="df144-132">DLL</span><span class="sxs-lookup"><span data-stu-id="df144-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df144-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df144-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df144-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df144-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df144-135">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="df144-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="df144-136">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="df144-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="df144-137">NLS：以名稱為基礎的 Api 範例</span><span class="sxs-lookup"><span data-stu-id="df144-137">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
