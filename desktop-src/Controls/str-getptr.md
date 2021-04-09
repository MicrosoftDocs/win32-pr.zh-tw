---
title: Str_GetPtr 函式
description: 將字串從一個緩衝區複製到另一個緩衝區。
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Str_GetPtr 函式 Windows 控制項
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec99bb4d91bde86d901c0e7ed4761bafd15f3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685660"
---
# <a name="str_getptr-function"></a><span data-ttu-id="1fc47-104">Str \_ GetPtr 函式</span><span class="sxs-lookup"><span data-stu-id="1fc47-104">Str\_GetPtr function</span></span>

<span data-ttu-id="1fc47-105">\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。</span><span class="sxs-lookup"><span data-stu-id="1fc47-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="1fc47-106">它可能會在後續版本的 Windows 中改變或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1fc47-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="1fc47-107">將字串從一個緩衝區複製到另一個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1fc47-107">Copies a string from one buffer to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc47-108">語法</span><span class="sxs-lookup"><span data-stu-id="1fc47-108">Syntax</span></span>


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a><span data-ttu-id="1fc47-109">參數</span><span class="sxs-lookup"><span data-stu-id="1fc47-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fc47-110">*pszSource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1fc47-110">*pszSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc47-111">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1fc47-111">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1fc47-112">來源字串的指標。</span><span class="sxs-lookup"><span data-stu-id="1fc47-112">A pointer to a source string.</span></span>

</dd> <dt>

<span data-ttu-id="1fc47-113">*pszDest* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1fc47-113">*pszDest* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc47-114">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1fc47-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1fc47-115">目的地緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="1fc47-115">A pointer to the destination buffer.</span></span> <span data-ttu-id="1fc47-116">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1fc47-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1fc47-117">*cchDest* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1fc47-117">*cchDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc47-118">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="1fc47-118">Type: **int**</span></span>

<span data-ttu-id="1fc47-119">*PszDest* 的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1fc47-119">The size of *pszDest*, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fc47-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="1fc47-120">Return value</span></span>

<span data-ttu-id="1fc47-121">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="1fc47-121">Type: **int**</span></span>

<span data-ttu-id="1fc47-122">如果 *pszDest* 為 **Null** 或 *cchDest* 為零，則會傳回所需的緩衝區大小（以字元為單位），以包含 *pszSource* 所指向之字串的以 Null 終止的複本。</span><span class="sxs-lookup"><span data-stu-id="1fc47-122">If *pszDest* is **NULL** or *cchDest* is zero, returns the size of the buffer, in characters, needed to contain a null-terminated copy of the string pointed to by *pszSource*.</span></span>

<span data-ttu-id="1fc47-123">如果 *pszDest* 為非 **Null**，則會傳回成功複製的字元數，包括結束的 Null 字元。</span><span class="sxs-lookup"><span data-stu-id="1fc47-123">If *pszDest* is non-**NULL**, returns the number of characters successfully copied, including the terminating null character.</span></span>

<span data-ttu-id="1fc47-124">如果 *pszDest* 無法保存 *pszSource* 所指向的整個字串，則會複製 (的 *cchDest*-1) 字元、以 null 終止的字串，以及傳回的 *cchDest* 。</span><span class="sxs-lookup"><span data-stu-id="1fc47-124">If *pszDest* cannot hold the entire string pointed to by *pszSource*, then (*cchDest*-1) characters are copied, the string null-terminated, and *cchDest* returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fc47-125">備註</span><span class="sxs-lookup"><span data-stu-id="1fc47-125">Remarks</span></span>

<span data-ttu-id="1fc47-126">**Str \_GetPtr** 可做為 ANSI (**str \_ GetPtrA**) 和 Unicode (**str \_ GetPtrW**) 版本。</span><span class="sxs-lookup"><span data-stu-id="1fc47-126">**Str\_GetPtr** is available as ANSI (**Str\_GetPtrA**) and Unicode (**Str\_GetPtrW**) versions.</span></span> <span data-ttu-id="1fc47-127">這些函式不會依名稱匯出，也不會在公用標頭檔中宣告。</span><span class="sxs-lookup"><span data-stu-id="1fc47-127">These functions are not exported by name or declared in a public header file.</span></span> <span data-ttu-id="1fc47-128">若要使用它們，您必須使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和要求序數 233 (**Str \_ GetPtrA**) 或 235 (**str \_ GetPtrW**) 自 ComCtl32.dll 取得函式指標。</span><span class="sxs-lookup"><span data-stu-id="1fc47-128">To use them, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 233 (**Str\_GetPtrA**) or 235 (**Str\_GetPtrW**) from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc47-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fc47-129">Requirements</span></span>



| <span data-ttu-id="1fc47-130">需求</span><span class="sxs-lookup"><span data-stu-id="1fc47-130">Requirement</span></span> | <span data-ttu-id="1fc47-131">值</span><span class="sxs-lookup"><span data-stu-id="1fc47-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc47-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fc47-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1fc47-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1fc47-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1fc47-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fc47-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1fc47-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1fc47-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1fc47-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1fc47-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fc47-137"><dt>ComCtl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fc47-137"><dt>ComCtl32.dll</dt></span></span> </dl> |
| <span data-ttu-id="1fc47-138">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="1fc47-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1fc47-139">**Str \_GetPtrW** (Unicode) 和 **Str \_ GetPtrA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="1fc47-139">**Str\_GetPtrW** (Unicode) and **Str\_GetPtrA** (ANSI)</span></span><br/>                       |



 

