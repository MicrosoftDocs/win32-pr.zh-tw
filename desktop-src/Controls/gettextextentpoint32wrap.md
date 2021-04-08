---
title: GetTextExtentPoint32Wrap 函式
description: 計算指定文字字串的寬度和高度。 此函數會包裝對 GetTextExtentPoint 的呼叫。
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- GetTextExtentPoint32Wrap 函式 Windows 控制項
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685560"
---
# <a name="gettextextentpoint32wrap-function"></a><span data-ttu-id="f84f7-105">GetTextExtentPoint32Wrap 函式</span><span class="sxs-lookup"><span data-stu-id="f84f7-105">GetTextExtentPoint32Wrap function</span></span>

<span data-ttu-id="f84f7-106">\[**GetTextExtentPoint32Wrap** 可透過 Windows XP Service Pack 2 (SP2) 取得。</span><span class="sxs-lookup"><span data-stu-id="f84f7-106">\[**GetTextExtentPoint32Wrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="f84f7-107">它可能會在後續版本中變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="f84f7-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f84f7-108">建議您改為直接使用 [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) 。\]</span><span class="sxs-lookup"><span data-stu-id="f84f7-108">It is recommended to use [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) directly instead.\]</span></span>

<span data-ttu-id="f84f7-109">計算指定文字字串的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="f84f7-109">Computes the width and height of the specified string of text.</span></span> <span data-ttu-id="f84f7-110">此函數會包裝對 [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="f84f7-110">This function wraps a call to [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="syntax"></a><span data-ttu-id="f84f7-111">語法</span><span class="sxs-lookup"><span data-stu-id="f84f7-111">Syntax</span></span>


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a><span data-ttu-id="f84f7-112">參數</span><span class="sxs-lookup"><span data-stu-id="f84f7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f84f7-113">*hdc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f84f7-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f84f7-114">類型： **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f84f7-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f84f7-115">裝置內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f84f7-115">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="f84f7-116">*lpString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f84f7-116">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f84f7-117">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f84f7-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f84f7-118">包含要繪製之文字的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="f84f7-118">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="f84f7-119">字串不需要以零結束，因為 *cbCount* 會指定字串的長度。</span><span class="sxs-lookup"><span data-stu-id="f84f7-119">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="f84f7-120">*cbCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f84f7-120">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f84f7-121">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f84f7-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f84f7-122">*LpString* 所指向之字串的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f84f7-122">The length, in bytes, of the string pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="f84f7-123">*lpSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f84f7-123">*lpSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f84f7-124">類型： **LPSIZE**</span><span class="sxs-lookup"><span data-stu-id="f84f7-124">Type: **LPSIZE**</span></span>

<span data-ttu-id="f84f7-125">當此方法傳回時，會包含 [**大小**](/previous-versions//dd145106(v=vs.85)) 結構的指標，其中包含字串的維度（以邏輯單位表示）。</span><span class="sxs-lookup"><span data-stu-id="f84f7-125">When this method returns, contains a pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure containing the dimensions of the string, in logical units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f84f7-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="f84f7-126">Return value</span></span>

<span data-ttu-id="f84f7-127">類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f84f7-127">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f84f7-128">如果成功，則傳回非零值;否則為0。</span><span class="sxs-lookup"><span data-stu-id="f84f7-128">Returns a nonzero value if successful; otherwise, 0.</span></span>

<span data-ttu-id="f84f7-129">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="f84f7-129">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="f84f7-130">備註</span><span class="sxs-lookup"><span data-stu-id="f84f7-130">Remarks</span></span>

<span data-ttu-id="f84f7-131">**GetTextExtentPoint32Wrap** 不會依名稱匯出，也不會在公用標頭檔中宣告。</span><span class="sxs-lookup"><span data-stu-id="f84f7-131">**GetTextExtentPoint32Wrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="f84f7-132">若要使用它，您必須從 ComCtl32.dll 使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和要求序數420來取得函式指標。</span><span class="sxs-lookup"><span data-stu-id="f84f7-132">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 420 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="f84f7-133">如需其他備註，請參閱 [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa)。</span><span class="sxs-lookup"><span data-stu-id="f84f7-133">For additional remarks, please see [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="requirements"></a><span data-ttu-id="f84f7-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="f84f7-134">Requirements</span></span>



| <span data-ttu-id="f84f7-135">需求</span><span class="sxs-lookup"><span data-stu-id="f84f7-135">Requirement</span></span> | <span data-ttu-id="f84f7-136">值</span><span class="sxs-lookup"><span data-stu-id="f84f7-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f84f7-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f84f7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f84f7-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f84f7-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="f84f7-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f84f7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f84f7-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f84f7-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f84f7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f84f7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f84f7-142"><dt>Comctl32.dll (5.81 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="f84f7-142"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 

