---
description: 將 Unicode 字串傳送至偵錯工具以供顯示。
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: 'OutputDebugStringWrapW 函式 (Shlwapip) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: e8213aee48a90a816e2968aac115159472ed7b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991634"
---
# <a name="outputdebugstringwrapw-function"></a><span data-ttu-id="21119-103">OutputDebugStringWrapW 函式</span><span class="sxs-lookup"><span data-stu-id="21119-103">OutputDebugStringWrapW function</span></span>

<span data-ttu-id="21119-104">\[這項功能可用於 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="21119-104">\[This function is available for use in Windows XP.</span></span> <span data-ttu-id="21119-105">在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="21119-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="21119-106">使用 [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) 的位置。\]</span><span class="sxs-lookup"><span data-stu-id="21119-106">Use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in its place.\]</span></span>

<span data-ttu-id="21119-107">將 Unicode 字串傳送至偵錯工具以供顯示。</span><span class="sxs-lookup"><span data-stu-id="21119-107">Sends a Unicode string to the debugger for display.</span></span>

> [!Note]  
> <span data-ttu-id="21119-108">**OutputDebugStringWrapW** 是 **OutputDebugStringW** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="21119-108">**OutputDebugStringWrapW** is a wrapper for the **OutputDebugStringW** function.</span></span> <span data-ttu-id="21119-109">如需進一步的使用注意事項，請參閱 [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) 頁面。</span><span class="sxs-lookup"><span data-stu-id="21119-109">See the [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="21119-110">語法</span><span class="sxs-lookup"><span data-stu-id="21119-110">Syntax</span></span>


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a><span data-ttu-id="21119-111">參數</span><span class="sxs-lookup"><span data-stu-id="21119-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21119-112">*lpOutputString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21119-112">*lpOutputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21119-113">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="21119-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="21119-114">要顯示之以 null 結束的 Unicode 字串指標。</span><span class="sxs-lookup"><span data-stu-id="21119-114">A pointer to the null-terminated Unicode string to be displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21119-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="21119-115">Return value</span></span>

<span data-ttu-id="21119-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="21119-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21119-117">備註</span><span class="sxs-lookup"><span data-stu-id="21119-117">Remarks</span></span>

<span data-ttu-id="21119-118">**OutputDebugStringWrapW** 能讓您在 Windows XP 之前的作業系統中使用 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="21119-118">**OutputDebugStringWrapW** provides the ability to use Unicode strings in operating systems prior to Windows XP.</span></span> <span data-ttu-id="21119-119">慣用的方法是使用 [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。</span><span class="sxs-lookup"><span data-stu-id="21119-119">The preferred method is to use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="21119-120">您必須使用序數115，直接從 Shlwapi.dll 呼叫 **OutputDebugStringWrapW** 。</span><span class="sxs-lookup"><span data-stu-id="21119-120">**OutputDebugStringWrapW** must be called directly from Shlwapi.dll, using ordinal 115.</span></span>

<span data-ttu-id="21119-121">如果應用程式沒有偵錯工具，系統偵錯工具就會顯示字串。</span><span class="sxs-lookup"><span data-stu-id="21119-121">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="21119-122">如果應用程式沒有偵錯工具，而系統偵錯工具未啟用，則 **OutputDebugStringWrapW** 不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="21119-122">If the application has no debugger and the system debugger is not active, **OutputDebugStringWrapW** does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="21119-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="21119-123">Requirements</span></span>



| <span data-ttu-id="21119-124">需求</span><span class="sxs-lookup"><span data-stu-id="21119-124">Requirement</span></span> | <span data-ttu-id="21119-125">值</span><span class="sxs-lookup"><span data-stu-id="21119-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21119-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21119-126">Minimum supported client</span></span><br/> | <span data-ttu-id="21119-127">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21119-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21119-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21119-128">Minimum supported server</span></span><br/> | <span data-ttu-id="21119-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21119-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="21119-130">標頭</span><span class="sxs-lookup"><span data-stu-id="21119-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="21119-131"><dt>Shlwapip。h</dt></span><span class="sxs-lookup"><span data-stu-id="21119-131"><dt>Shlwapip.h</dt></span></span> </dl>                         |
| <span data-ttu-id="21119-132">DLL</span><span class="sxs-lookup"><span data-stu-id="21119-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21119-133"><dt>Shlwapi.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="21119-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21119-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21119-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21119-135">**OutputDebugString**</span><span class="sxs-lookup"><span data-stu-id="21119-135">**OutputDebugString**</span></span>](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
