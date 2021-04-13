---
description: 將 Unicode 字元字串或單一字元轉換成小寫。
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: CharLowerWrapW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharLowerWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 3911e0366d30f3eb9420391f9d06867ded73530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511062"
---
# <a name="charlowerwrapw-function"></a><span data-ttu-id="184d5-103">CharLowerWrapW 函式</span><span class="sxs-lookup"><span data-stu-id="184d5-103">CharLowerWrapW function</span></span>

<span data-ttu-id="184d5-104">\[**CharLowerWrapW** 可用於 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="184d5-104">\[**CharLowerWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="184d5-105">在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="184d5-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="184d5-106">您應該在其位置使用 [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) 。\]</span><span class="sxs-lookup"><span data-stu-id="184d5-106">You should use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in its place.\]</span></span>

<span data-ttu-id="184d5-107">將 Unicode 字元字串或單一字元轉換成小寫。</span><span class="sxs-lookup"><span data-stu-id="184d5-107">Converts a Unicode character string or a single character to lowercase.</span></span> <span data-ttu-id="184d5-108">如果運算元是字元字串，則函式會就地轉換字元。</span><span class="sxs-lookup"><span data-stu-id="184d5-108">If the operand is a character string, the function converts the characters in place.</span></span>

> [!Note]  
> <span data-ttu-id="184d5-109">**CharLowerWrapW** 是 **CharLowerW** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="184d5-109">**CharLowerWrapW** is a wrapper for the **CharLowerW** function.</span></span> <span data-ttu-id="184d5-110">如需進一步的使用注意事項，請參閱 [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) 頁面。</span><span class="sxs-lookup"><span data-stu-id="184d5-110">See the [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="184d5-111">語法</span><span class="sxs-lookup"><span data-stu-id="184d5-111">Syntax</span></span>


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a><span data-ttu-id="184d5-112">參數</span><span class="sxs-lookup"><span data-stu-id="184d5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="184d5-113">*pch* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="184d5-113">*pch* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="184d5-114">類型： **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="184d5-114">Type: **LPWSTR**</span></span>

<span data-ttu-id="184d5-115">指標，指向以 null 終止的 Unicode 字串或單一字元。</span><span class="sxs-lookup"><span data-stu-id="184d5-115">A pointer to a null-terminated Unicode string or a single character.</span></span> <span data-ttu-id="184d5-116">如果此參數的高序位字為零，則低序位單字必須只包含要轉換的單一字元。</span><span class="sxs-lookup"><span data-stu-id="184d5-116">If the high-order word of this parameter is zero, the low-order word must contain only a single character to be converted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="184d5-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="184d5-117">Return value</span></span>

<span data-ttu-id="184d5-118">類型： **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="184d5-118">Type: **LPWSTR**</span></span>

<span data-ttu-id="184d5-119">如果 *pch* 是字元字串，則函式會傳回已轉換之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="184d5-119">If *pch* is a character string, the function returns a pointer to the converted string.</span></span> <span data-ttu-id="184d5-120">因為字串會就地轉換，所以傳回值等於 *pch*。</span><span class="sxs-lookup"><span data-stu-id="184d5-120">Since the string is converted in place, the return value is equal to *pch*.</span></span>

<span data-ttu-id="184d5-121">如果 *pch* 是單一字元，則傳回值為32位值，其高序位字組為零，而低序位字組包含轉換的字元。</span><span class="sxs-lookup"><span data-stu-id="184d5-121">If *pch* is a single character, the return value is a 32-bit value whose high-order word is zero, and low-order word contains the converted character.</span></span>

<span data-ttu-id="184d5-122">沒有指示成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="184d5-122">There is no indication of success or failure.</span></span> <span data-ttu-id="184d5-123">失敗很罕見。</span><span class="sxs-lookup"><span data-stu-id="184d5-123">Failure is rare.</span></span> <span data-ttu-id="184d5-124">此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="184d5-124">There is no extended error information for this function; do not call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="184d5-125">備註</span><span class="sxs-lookup"><span data-stu-id="184d5-125">Remarks</span></span>

<span data-ttu-id="184d5-126">慣用的方法是使用 [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。</span><span class="sxs-lookup"><span data-stu-id="184d5-126">The preferred method is to use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="184d5-127">您必須使用序數38，直接從 Shlwapi.dll 呼叫 **CharLowerWrapW** 。</span><span class="sxs-lookup"><span data-stu-id="184d5-127">**CharLowerWrapW** must be called directly from Shlwapi.dll, using ordinal 38.</span></span>

## <a name="requirements"></a><span data-ttu-id="184d5-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="184d5-128">Requirements</span></span>



| <span data-ttu-id="184d5-129">需求</span><span class="sxs-lookup"><span data-stu-id="184d5-129">Requirement</span></span> | <span data-ttu-id="184d5-130">值</span><span class="sxs-lookup"><span data-stu-id="184d5-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="184d5-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="184d5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="184d5-132">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="184d5-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="184d5-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="184d5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="184d5-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="184d5-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="184d5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="184d5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="184d5-136"><dt>Shlwapi.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="184d5-136"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="184d5-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="184d5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="184d5-138">**CharLower**</span><span class="sxs-lookup"><span data-stu-id="184d5-138">**CharLower**</span></span>](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
