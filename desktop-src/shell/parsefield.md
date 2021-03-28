---
description: 從 Setup.exe 讀取一行，並從字串中解壓縮指定的欄位。
ms.assetid: 621e85f8-af30-4f1f-bab1-b7f824daa363
title: 'ParseField 函式 (Util) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParseField
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 45c7d5bc692f969ba821b5d3243b312d0883658e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193351"
---
# <a name="parsefield-function"></a><span data-ttu-id="e2c0d-103">ParseField 函式</span><span class="sxs-lookup"><span data-stu-id="e2c0d-103">ParseField function</span></span>

<span data-ttu-id="e2c0d-104">\[**ParseField** 函式目前應可用於下一版的 Microsoft Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="e2c0d-104">\[The **ParseField** function is currently expected to be available for use in the next version of the Microsoft Windows operating system.</span></span> <span data-ttu-id="e2c0d-105">它可能會在後續版本中變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e2c0d-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="e2c0d-106">從 Setup.exe 讀取一行，並從字串中解壓縮指定的欄位。</span><span class="sxs-lookup"><span data-stu-id="e2c0d-106">Reads a line from Setup.inf and extracts the specified field from the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2c0d-107">語法</span><span class="sxs-lookup"><span data-stu-id="e2c0d-107">Syntax</span></span>


```C++
bool ParseField(
  _In_ LPCTSTR *szData,
  _In_ int     n,
  _In_ LPTSTR  *szBuf,
  _In_ int     iBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="e2c0d-108">參數</span><span class="sxs-lookup"><span data-stu-id="e2c0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2c0d-109">*szData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2c0d-109">*szData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c0d-110">類型： \**LPCTSTR \** _</span><span class="sxs-lookup"><span data-stu-id="e2c0d-110">Type: \**LPCTSTR\** _</span></span>

<span data-ttu-id="e2c0d-111">Setup.exe 的行指標。</span><span class="sxs-lookup"><span data-stu-id="e2c0d-111">A pointer to the line from Setup.inf.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0d-112">_n \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2c0d-112">_n\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c0d-113">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="e2c0d-113">Type: **int**</span></span>

<span data-ttu-id="e2c0d-114">**整數** ，表示要解壓縮的欄位。</span><span class="sxs-lookup"><span data-stu-id="e2c0d-114">**INT** that indicates which field to extract.</span></span>

<dt>



 <span data-ttu-id="e2c0d-115"> (0)</span><span class="sxs-lookup"><span data-stu-id="e2c0d-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e2c0d-116">指出在等號 (=) 之前的欄位。</span><span class="sxs-lookup"><span data-stu-id="e2c0d-116">Indicates the field before an equals sign (=).</span></span>

</dd> <dt>



 <span data-ttu-id="e2c0d-117">(1)</span><span class="sxs-lookup"><span data-stu-id="e2c0d-117">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e2c0d-118">表示第一個欄位。</span><span class="sxs-lookup"><span data-stu-id="e2c0d-118">Indicates the first field.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e2c0d-119">*szBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2c0d-119">*szBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c0d-120">類型： \**LPTSTR \** _</span><span class="sxs-lookup"><span data-stu-id="e2c0d-120">Type: \**LPTSTR\** _</span></span>

<span data-ttu-id="e2c0d-121">接收已解壓縮之欄位之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="e2c0d-121">A pointer to the buffer that receives the extracted field.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0d-122">_iBufLen \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2c0d-122">_iBufLen\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c0d-123">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="e2c0d-123">Type: **int**</span></span>

<span data-ttu-id="e2c0d-124">**INT** ，可接收已解壓縮之欄位的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="e2c0d-124">**INT** that receives the size of the buffer that receives the extracted field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2c0d-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2c0d-125">Return value</span></span>

<span data-ttu-id="e2c0d-126">類型： **bool**</span><span class="sxs-lookup"><span data-stu-id="e2c0d-126">Type: **bool**</span></span>

<span data-ttu-id="e2c0d-127">如果函式成功，則傳回 **TRUE** ，如果失敗，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e2c0d-127">Returns **TRUE** if the function is successful and **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2c0d-128">備註</span><span class="sxs-lookup"><span data-stu-id="e2c0d-128">Remarks</span></span>

<span data-ttu-id="e2c0d-129">字串中的欄位必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="e2c0d-129">The fields in the string must be separated by commas.</span></span>

<span data-ttu-id="e2c0d-130">移除前置和尾端空格。</span><span class="sxs-lookup"><span data-stu-id="e2c0d-130">Leading and trailing spaces are removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2c0d-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2c0d-131">Requirements</span></span>



| <span data-ttu-id="e2c0d-132">需求</span><span class="sxs-lookup"><span data-stu-id="e2c0d-132">Requirement</span></span> | <span data-ttu-id="e2c0d-133">值</span><span class="sxs-lookup"><span data-stu-id="e2c0d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c0d-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2c0d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e2c0d-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2c0d-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2c0d-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2c0d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e2c0d-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2c0d-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e2c0d-138">標頭</span><span class="sxs-lookup"><span data-stu-id="e2c0d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2c0d-139"><dt>Util。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2c0d-139"><dt>Util.h</dt></span></span> </dl>                             |
| <span data-ttu-id="e2c0d-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="e2c0d-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="e2c0d-141"><dt>Shell32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2c0d-141"><dt>Shell32.lib</dt></span></span> </dl>                        |
| <span data-ttu-id="e2c0d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e2c0d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2c0d-143"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="e2c0d-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




