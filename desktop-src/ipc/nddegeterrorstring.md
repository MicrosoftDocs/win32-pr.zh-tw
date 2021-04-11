---
description: 將網路 DDE 函數所傳回的錯誤碼轉換成錯誤字串，以說明傳回的錯誤碼。
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: 'NDdeGetErrorString 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetErrorString
- NDdeGetErrorStringA
- NDdeGetErrorStringW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8e043c8281d3ad049346ac7ce68991eb6bd08af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026079"
---
# <a name="nddegeterrorstring-function"></a><span data-ttu-id="70b2e-103">NDdeGetErrorString 函式</span><span class="sxs-lookup"><span data-stu-id="70b2e-103">NDdeGetErrorString function</span></span>

<span data-ttu-id="70b2e-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="70b2e-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="70b2e-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="70b2e-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="70b2e-106">將網路 DDE 函數所傳回的錯誤碼轉換成錯誤字串，以說明傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="70b2e-106">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="70b2e-107">語法</span><span class="sxs-lookup"><span data-stu-id="70b2e-107">Syntax</span></span>


```C++
UINT NDdeGetErrorString(
  _In_  UINT   uErrorCode,
  _Out_ LPTSTR lpszErrorString,
  _In_  DWORD  cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="70b2e-108">參數</span><span class="sxs-lookup"><span data-stu-id="70b2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70b2e-109">*uErrorCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70b2e-109">*uErrorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b2e-110">要轉換成錯誤字串的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="70b2e-110">The error code to be converted into an error string.</span></span>

</dd> <dt>

<span data-ttu-id="70b2e-111">*lpszErrorString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="70b2e-111">*lpszErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70b2e-112">接收轉譯的錯誤字串之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="70b2e-112">A pointer to a buffer that receives the translated error string.</span></span> <span data-ttu-id="70b2e-113">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="70b2e-113">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="70b2e-114">如果緩衝區不夠大，無法儲存完整的錯誤字串，則會截斷字串。</span><span class="sxs-lookup"><span data-stu-id="70b2e-114">If the buffer is not large enough to store the complete error string, the string is truncated.</span></span>

</dd> <dt>

<span data-ttu-id="70b2e-115">*cBufSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70b2e-115">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b2e-116">接收錯誤字串的緩衝區大小（以 **TCHARs**）。</span><span class="sxs-lookup"><span data-stu-id="70b2e-116">The size of the buffer to receive the error string, in **TCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70b2e-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="70b2e-117">Return value</span></span>

<span data-ttu-id="70b2e-118">如果此函式成功，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="70b2e-118">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="70b2e-119">如果函式失敗，則傳回值為非零的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="70b2e-119">If the function fails, the return value is a nonzero error code.</span></span> <span data-ttu-id="70b2e-120">如果 *lpszErrorString* 緩衝區不夠大，無法接受完整的錯誤字串，而且字串遭到截斷，則函式會傳回值 NDDE \_ 內部 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="70b2e-120">If the *lpszErrorString* buffer is not large enough to accept the complete error string, and the string is truncated, the function returns the value NDDE\_INTERNAL\_ERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="70b2e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="70b2e-121">Requirements</span></span>



| <span data-ttu-id="70b2e-122">需求</span><span class="sxs-lookup"><span data-stu-id="70b2e-122">Requirement</span></span> | <span data-ttu-id="70b2e-123">值</span><span class="sxs-lookup"><span data-stu-id="70b2e-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70b2e-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70b2e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="70b2e-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70b2e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="70b2e-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70b2e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="70b2e-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70b2e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="70b2e-128">標頭</span><span class="sxs-lookup"><span data-stu-id="70b2e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="70b2e-129"><dt>Nddeapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="70b2e-129"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="70b2e-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="70b2e-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="70b2e-131"><dt>Nddeapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="70b2e-131"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="70b2e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="70b2e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70b2e-133"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70b2e-133"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="70b2e-134">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="70b2e-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="70b2e-135">**NDdeGetErrorStringW** (Unicode) 和 **NDdeGetErrorStringA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="70b2e-135">**NDdeGetErrorStringW** (Unicode) and **NDdeGetErrorStringA** (ANSI)</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="70b2e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70b2e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b2e-137">網路動態資料交換總覽</span><span class="sxs-lookup"><span data-stu-id="70b2e-137">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="70b2e-138">網路 DDE 函數</span><span class="sxs-lookup"><span data-stu-id="70b2e-138">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




