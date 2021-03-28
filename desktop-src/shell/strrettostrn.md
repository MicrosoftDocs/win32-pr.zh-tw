---
description: 採用 IShellFolder：： GetDisplayNameOf 傳回的 STRRET 結構，將它轉換成字串，並將結果放在緩衝區中。
title: StrRetToStrN 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 89a8d991e22e8615456bd8d4690c046ec0d325d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991810"
---
# <a name="strrettostrn-function"></a><span data-ttu-id="da61f-103">StrRetToStrN 函式</span><span class="sxs-lookup"><span data-stu-id="da61f-103">StrRetToStrN function</span></span>

<span data-ttu-id="da61f-104">採用 [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)傳回的 [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret)結構，將它轉換成字串，並將結果放在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="da61f-104">Takes an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure returned by [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), converts it to a string, and places the result in a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="da61f-105">語法</span><span class="sxs-lookup"><span data-stu-id="da61f-105">Syntax</span></span>


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a><span data-ttu-id="da61f-106">參數</span><span class="sxs-lookup"><span data-stu-id="da61f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da61f-107">*pszOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="da61f-107">*pszOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da61f-108">類型： **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="da61f-108">Type: **LPTSTR**</span></span>

<span data-ttu-id="da61f-109">保存顯示名稱的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="da61f-109">Buffer to hold the display name.</span></span> <span data-ttu-id="da61f-110">它會以 null 終止字串的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="da61f-110">It will be returned as a null-terminated string.</span></span> <span data-ttu-id="da61f-111">如果 *cchOut* 太小，名稱將會被截斷以配合其大小。</span><span class="sxs-lookup"><span data-stu-id="da61f-111">If *cchOut* is too small, the name will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="da61f-112">*cchOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da61f-112">*cchOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da61f-113">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="da61f-113">Type: **UINT**</span></span>

<span data-ttu-id="da61f-114">*PszOut* 的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="da61f-114">Size of *pszOut*, in characters.</span></span> <span data-ttu-id="da61f-115">如果 *cchOut* 太小，則字串將會被截斷以配合其大小。</span><span class="sxs-lookup"><span data-stu-id="da61f-115">If *cchOut* is too small, the string will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="da61f-116">*pStrRet* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="da61f-116">*pStrRet* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="da61f-117">類型： **LPSTRRET**</span><span class="sxs-lookup"><span data-stu-id="da61f-117">Type: **LPSTRRET**</span></span>

<span data-ttu-id="da61f-118">[**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="da61f-118">Pointer to an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure.</span></span> <span data-ttu-id="da61f-119">當函式傳回時，這個指標將不再有效。</span><span class="sxs-lookup"><span data-stu-id="da61f-119">When the function returns, this pointer will no longer be valid.</span></span>

</dd> <dt>

<span data-ttu-id="da61f-120">*pidl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da61f-120">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da61f-121">類型： **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="da61f-121">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="da61f-122">專案之 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="da61f-122">Pointer to the item's [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da61f-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="da61f-123">Return value</span></span>

<span data-ttu-id="da61f-124">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="da61f-124">Type: **BOOL**</span></span>

<span data-ttu-id="da61f-125">若為成功，**則為 TRUE** ，如果失敗，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="da61f-125">**TRUE** for success, **FALSE** for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="da61f-126">備註</span><span class="sxs-lookup"><span data-stu-id="da61f-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="da61f-127">從 Shell32.dll 5.0 版起，呼叫此函式相當於呼叫 [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)。</span><span class="sxs-lookup"><span data-stu-id="da61f-127">As of Shell32.dll version 5.0, calling this function is equivalent to calling [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span></span>

 

<span data-ttu-id="da61f-128">**StrRetToStrN** 不是依名稱匯出。</span><span class="sxs-lookup"><span data-stu-id="da61f-128">**StrRetToStrN** is not exported by name.</span></span> <span data-ttu-id="da61f-129">若要使用它，您必須從 Shell32.dll 使用 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 和要求序數96來取得函式指標。</span><span class="sxs-lookup"><span data-stu-id="da61f-129">To use it, you must use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 96 from Shell32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="da61f-130">如果 *pStrRet* 所指向之結構的 **uType** 成員設定為 **STRRET \_ WSTR**，該結構的 **pOleStr** 成員將會在傳回時釋出。</span><span class="sxs-lookup"><span data-stu-id="da61f-130">If the **uType** member of the structure pointed to by *pStrRet* is set to **STRRET\_WSTR**, the **pOleStr** member of that structure will be freed on return.</span></span>

<span data-ttu-id="da61f-131">請注意，此函式會從 Shell32.dll 匯出，而不是 Shlwapi.dll。</span><span class="sxs-lookup"><span data-stu-id="da61f-131">Note that this function is exported from Shell32.dll rather than Shlwapi.dll.</span></span> <span data-ttu-id="da61f-132">它也包含在 Shlobj.h 中，而不是 Shlwapi。</span><span class="sxs-lookup"><span data-stu-id="da61f-132">It is also included in Shlobj.h rather than Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="da61f-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="da61f-133">Requirements</span></span>



| <span data-ttu-id="da61f-134">需求</span><span class="sxs-lookup"><span data-stu-id="da61f-134">Requirement</span></span> | <span data-ttu-id="da61f-135">值</span><span class="sxs-lookup"><span data-stu-id="da61f-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da61f-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da61f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="da61f-137">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da61f-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="da61f-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da61f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="da61f-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da61f-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="da61f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="da61f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da61f-141"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="da61f-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da61f-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da61f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da61f-143">**StrRetToStr**</span><span class="sxs-lookup"><span data-stu-id="da61f-143">**StrRetToStr**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[<span data-ttu-id="da61f-144">**StrRetToBuf**</span><span class="sxs-lookup"><span data-stu-id="da61f-144">**StrRetToBuf**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
