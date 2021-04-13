---
description: 將緩衝區中的小寫字元轉換成大寫字元。
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: CharUpperBuffWrapW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: dacc5e7609ca7f91bf7c66651d7ba9bdd11ab688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511061"
---
# <a name="charupperbuffwrapw-function"></a><span data-ttu-id="e2129-103">CharUpperBuffWrapW 函式</span><span class="sxs-lookup"><span data-stu-id="e2129-103">CharUpperBuffWrapW function</span></span>

<span data-ttu-id="e2129-104">\[**CharUpperBuffWrapW** 可用於 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e2129-104">\[**CharUpperBuffWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="e2129-105">在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2129-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="e2129-106">您應該在其位置使用 [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) 。\]</span><span class="sxs-lookup"><span data-stu-id="e2129-106">You should use [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in its place.\]</span></span>

<span data-ttu-id="e2129-107">將緩衝區中的小寫字元轉換成大寫字元。</span><span class="sxs-lookup"><span data-stu-id="e2129-107">Converts lowercase characters in a buffer to uppercase characters.</span></span> <span data-ttu-id="e2129-108">函數會就地轉換字元。</span><span class="sxs-lookup"><span data-stu-id="e2129-108">The function converts the characters in place.</span></span>

> [!Note]  
> <span data-ttu-id="e2129-109">**CharUpperBuffWrapW** 是 **CharUpperBuffW** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="e2129-109">**CharUpperBuffWrapW** is a wrapper for the **CharUpperBuffW** function.</span></span> <span data-ttu-id="e2129-110">如需進一步的使用注意事項，請參閱 [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) 頁面。</span><span class="sxs-lookup"><span data-stu-id="e2129-110">See the [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e2129-111">語法</span><span class="sxs-lookup"><span data-stu-id="e2129-111">Syntax</span></span>


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a><span data-ttu-id="e2129-112">參數</span><span class="sxs-lookup"><span data-stu-id="e2129-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2129-113">*pch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2129-113">*pch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2129-114">類型： **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e2129-114">Type: **LPWSTR**</span></span>

<span data-ttu-id="e2129-115">包含一或多個要處理的 Unicode 字元之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="e2129-115">A pointer to a buffer that contains one or more Unicode characters to process.</span></span>

</dd> <dt>

<span data-ttu-id="e2129-116">*cchLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2129-116">*cchLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2129-117">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e2129-117">Type: **DWORD**</span></span>

<span data-ttu-id="e2129-118">指定 *pch* 所指向之緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2129-118">Specifies the size, in characters, of the buffer pointed to by *pch*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2129-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2129-119">Return value</span></span>

<span data-ttu-id="e2129-120">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e2129-120">Type: **DWORD**</span></span>

<span data-ttu-id="e2129-121">處理的字元數。</span><span class="sxs-lookup"><span data-stu-id="e2129-121">The number of characters processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2129-122">備註</span><span class="sxs-lookup"><span data-stu-id="e2129-122">Remarks</span></span>

<span data-ttu-id="e2129-123">慣用的方法是使用 [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。</span><span class="sxs-lookup"><span data-stu-id="e2129-123">The preferred method is to use [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="e2129-124">您必須使用序數44，直接從 Shlwapi.dll 呼叫 **CharUpperBuffWrapW** 。</span><span class="sxs-lookup"><span data-stu-id="e2129-124">**CharUpperBuffWrapW** must be called directly from Shlwapi.dll, using ordinal 44.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2129-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2129-125">Requirements</span></span>



| <span data-ttu-id="e2129-126">需求</span><span class="sxs-lookup"><span data-stu-id="e2129-126">Requirement</span></span> | <span data-ttu-id="e2129-127">值</span><span class="sxs-lookup"><span data-stu-id="e2129-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2129-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2129-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e2129-129">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2129-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2129-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2129-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e2129-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2129-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e2129-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e2129-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2129-133"><dt>Shlwapi.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="e2129-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2129-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2129-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2129-135">**CharUpperBuff**</span><span class="sxs-lookup"><span data-stu-id="e2129-135">**CharUpperBuff**</span></span>](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
