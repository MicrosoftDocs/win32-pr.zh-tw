---
description: 在指定的模組中，判斷具有指定之類型和名稱之資源的位置。
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: FindResourceWrapW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 8f76d516570725fe6da5e8a21ec5a29699276ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192702"
---
# <a name="findresourcewrapw-function"></a><span data-ttu-id="46e62-103">FindResourceWrapW 函式</span><span class="sxs-lookup"><span data-stu-id="46e62-103">FindResourceWrapW function</span></span>

<span data-ttu-id="46e62-104">\[**FindResourceWrapW** 可用於 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="46e62-104">\[**FindResourceWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="46e62-105">在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="46e62-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="46e62-106">您應該改為使用 [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) 。\]</span><span class="sxs-lookup"><span data-stu-id="46e62-106">You should use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) instead.\]</span></span>

<span data-ttu-id="46e62-107">在指定的模組中，判斷具有指定之類型和名稱之資源的位置。</span><span class="sxs-lookup"><span data-stu-id="46e62-107">Determines the location of a resource with the specified type and name, in the specified module.</span></span>

> [!Note]  
> <span data-ttu-id="46e62-108">**FindResourceWrapW** 是 **FindResourceW** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="46e62-108">**FindResourceWrapW** is a wrapper for the **FindResourceW** function.</span></span> <span data-ttu-id="46e62-109">如需進一步的使用注意事項，請參閱 [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) 。</span><span class="sxs-lookup"><span data-stu-id="46e62-109">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="46e62-110">語法</span><span class="sxs-lookup"><span data-stu-id="46e62-110">Syntax</span></span>


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a><span data-ttu-id="46e62-111">參數</span><span class="sxs-lookup"><span data-stu-id="46e62-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46e62-112">*hModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46e62-112">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e62-113">類型： **HMODULE**</span><span class="sxs-lookup"><span data-stu-id="46e62-113">Type: **HMODULE**</span></span>

<span data-ttu-id="46e62-114">模組的控制碼，可執行檔包含資源。</span><span class="sxs-lookup"><span data-stu-id="46e62-114">A handle to the module whose executable file contains the resource.</span></span> <span data-ttu-id="46e62-115">**Null** 值會指定與作業系統用來建立目前進程的影像檔相關聯的模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="46e62-115">A value of **NULL** specifies the module handle associated with the image file that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="46e62-116">*lpName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46e62-116">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e62-117">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="46e62-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="46e62-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="46e62-118">The name of the resource.</span></span> <span data-ttu-id="46e62-119">如需詳細資訊，請參閱 [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea)。</span><span class="sxs-lookup"><span data-stu-id="46e62-119">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="46e62-120">*lpType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46e62-120">*lpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e62-121">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="46e62-121">Type: **LPCWSTR**</span></span>

<span data-ttu-id="46e62-122">指定資源類型之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="46e62-122">A pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="46e62-123">如需詳細資訊，請參閱 [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea)。</span><span class="sxs-lookup"><span data-stu-id="46e62-123">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46e62-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="46e62-124">Return value</span></span>

<span data-ttu-id="46e62-125">類型： **HRSRC**</span><span class="sxs-lookup"><span data-stu-id="46e62-125">Type: **HRSRC**</span></span>

<span data-ttu-id="46e62-126">如果函式成功，則傳回值是指定資源之資訊區塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="46e62-126">If the function succeeds, the return value is a handle to the specified resource's information block.</span></span> <span data-ttu-id="46e62-127">若要取得資源的控制碼，請將此控制碼傳遞給 [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) 函數。</span><span class="sxs-lookup"><span data-stu-id="46e62-127">To obtain a handle to the resource, pass this handle to the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

<span data-ttu-id="46e62-128">如果函式失敗，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="46e62-128">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="46e62-129">若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。</span><span class="sxs-lookup"><span data-stu-id="46e62-129">To get extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="46e62-130">備註</span><span class="sxs-lookup"><span data-stu-id="46e62-130">Remarks</span></span>

<span data-ttu-id="46e62-131">如果您需要指定特定的當地語系化，請使用 [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) 函式，而不是 **FindResourceWrapW**。</span><span class="sxs-lookup"><span data-stu-id="46e62-131">If you need to specify a particular localization, use the [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) function rather than **FindResourceWrapW**.</span></span>

<span data-ttu-id="46e62-132">**FindResourceWrapW** 提供在舊版作業系統中使用 Unicode 字串的能力。</span><span class="sxs-lookup"><span data-stu-id="46e62-132">**FindResourceWrapW** provides the ability to use Unicode strings in older operating systems.</span></span> <span data-ttu-id="46e62-133">慣用的方法是使用 [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。</span><span class="sxs-lookup"><span data-stu-id="46e62-133">The preferred method is to use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="46e62-134">您必須使用序數66，直接從 Shlwapi.dll 呼叫 **FindResourceWrapW** 。</span><span class="sxs-lookup"><span data-stu-id="46e62-134">**FindResourceWrapW** must be called directly from Shlwapi.dll, using ordinal 66.</span></span>

## <a name="requirements"></a><span data-ttu-id="46e62-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="46e62-135">Requirements</span></span>



| <span data-ttu-id="46e62-136">需求</span><span class="sxs-lookup"><span data-stu-id="46e62-136">Requirement</span></span> | <span data-ttu-id="46e62-137">值</span><span class="sxs-lookup"><span data-stu-id="46e62-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46e62-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46e62-138">Minimum supported client</span></span><br/> | <span data-ttu-id="46e62-139">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46e62-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46e62-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46e62-140">Minimum supported server</span></span><br/> | <span data-ttu-id="46e62-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46e62-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="46e62-142">標頭</span><span class="sxs-lookup"><span data-stu-id="46e62-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="46e62-143"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="46e62-143"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="46e62-144">DLL</span><span class="sxs-lookup"><span data-stu-id="46e62-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46e62-145"><dt>Shlwapi.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="46e62-145"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="46e62-146">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="46e62-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="46e62-147">**FindResourceWrapW** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="46e62-147">**FindResourceWrapW** (Unicode)</span></span><br/>                                                                    |



## <a name="see-also"></a><span data-ttu-id="46e62-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46e62-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e62-149">**FindResource**</span><span class="sxs-lookup"><span data-stu-id="46e62-149">**FindResource**</span></span>](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
