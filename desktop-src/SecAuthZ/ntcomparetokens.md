---
description: 比較兩個存取權杖，並判斷它們是否相等於對 AccessCheck 函數的呼叫。
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: 'NtCompareTokens 函式 (Ntseapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d4d0f35bff8fa65e0e09be32a55281b5118f244c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977864"
---
# <a name="ntcomparetokens-function"></a><span data-ttu-id="56931-103">NtCompareTokens 函式</span><span class="sxs-lookup"><span data-stu-id="56931-103">NtCompareTokens function</span></span>

<span data-ttu-id="56931-104">**NtCompareTokens** 函式會比較兩個 [*存取權杖*](/windows/desktop/SecGloss/a-gly)，並判斷它們是否相等於對 [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)函數的呼叫。</span><span class="sxs-lookup"><span data-stu-id="56931-104">The **NtCompareTokens** function compares two [*access tokens*](/windows/desktop/SecGloss/a-gly) and determines whether they are equivalent with respect to a call to the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="56931-105">語法</span><span class="sxs-lookup"><span data-stu-id="56931-105">Syntax</span></span>


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a><span data-ttu-id="56931-106">參數</span><span class="sxs-lookup"><span data-stu-id="56931-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56931-107">*FirstTokenHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="56931-107">*FirstTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56931-108">要比較之第一個存取權杖的控制碼。</span><span class="sxs-lookup"><span data-stu-id="56931-108">A handle to the first access token to compare.</span></span> <span data-ttu-id="56931-109">必須開啟權杖，才能存取 **權杖 \_ 查詢** 。</span><span class="sxs-lookup"><span data-stu-id="56931-109">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="56931-110">*SecondTokenHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="56931-110">*SecondTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56931-111">要比較之第二個存取權杖的控制碼。</span><span class="sxs-lookup"><span data-stu-id="56931-111">A handle to the second access token to compare.</span></span> <span data-ttu-id="56931-112">必須開啟權杖，才能存取 **權杖 \_ 查詢** 。</span><span class="sxs-lookup"><span data-stu-id="56931-112">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="56931-113">*等於* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="56931-113">*Equal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56931-114">變數的指標，此變數會接收表示 *FirstTokenHandle* 和 *SecondTokenHandle* 參數所代表的標記是否相等的值。</span><span class="sxs-lookup"><span data-stu-id="56931-114">A pointer to a variable that receives a value that indicates whether the tokens represented by the *FirstTokenHandle* and *SecondTokenHandle* parameters are equivalent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56931-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="56931-115">Return value</span></span>

<span data-ttu-id="56931-116">如果函式成功，函數會傳回狀態 \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="56931-116">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="56931-117">如果函式失敗，則會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="56931-117">If the function fails, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="56931-118">備註</span><span class="sxs-lookup"><span data-stu-id="56931-118">Remarks</span></span>

<span data-ttu-id="56931-119">如果下列所有條件都成立，則會將兩個存取控制權杖視為相等：</span><span class="sxs-lookup"><span data-stu-id="56931-119">Two access control tokens are considered to be equivalent if all of the following conditions are true:</span></span>

-   <span data-ttu-id="56931-120">每一個權杖中 (SID) 的每個 [*安全性識別*](/windows/desktop/SecGloss/s-gly) 元也會出現在另一個權杖中。</span><span class="sxs-lookup"><span data-stu-id="56931-120">Every [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) that is present in either token is also present in the other token.</span></span>
-   <span data-ttu-id="56931-121">這兩個權杖都不受限制。</span><span class="sxs-lookup"><span data-stu-id="56931-121">Neither or both of the tokens are restricted.</span></span>
-   <span data-ttu-id="56931-122">如果這兩個權杖都受到限制，則在一個權杖中受限制的每個 SID 也會在另一個權杖中受到限制。</span><span class="sxs-lookup"><span data-stu-id="56931-122">If both tokens are restricted, every SID that is restricted in one token is also restricted in the other token.</span></span>
-   <span data-ttu-id="56931-123">任一個權杖中出現的每個許可權也會出現在另一個權杖中。</span><span class="sxs-lookup"><span data-stu-id="56931-123">Every privilege present in either token is also present in the other token.</span></span>

<span data-ttu-id="56931-124">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="56931-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="56931-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="56931-125">Requirements</span></span>



| <span data-ttu-id="56931-126">需求</span><span class="sxs-lookup"><span data-stu-id="56931-126">Requirement</span></span> | <span data-ttu-id="56931-127">值</span><span class="sxs-lookup"><span data-stu-id="56931-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="56931-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56931-128">Minimum supported client</span></span><br/> | <span data-ttu-id="56931-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56931-129">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="56931-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56931-130">Minimum supported server</span></span><br/> | <span data-ttu-id="56931-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56931-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="56931-132">標頭</span><span class="sxs-lookup"><span data-stu-id="56931-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="56931-133"><dt>Ntseapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="56931-133"><dt>Ntseapi.h</dt></span></span> </dl> |
| <span data-ttu-id="56931-134">DLL</span><span class="sxs-lookup"><span data-stu-id="56931-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56931-135"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56931-135"><dt>Ntdll.dll</dt></span></span> </dl> |



 

