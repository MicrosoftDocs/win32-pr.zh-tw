---
description: 顯示對話方塊，其中包含已簽署訊息的簽署者資訊。
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: CryptUIDlgViewSignerInfo 函式
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 7ae677692b9266893eabf1002039c5efbf0ca5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847887"
---
# <a name="cryptuidlgviewsignerinfo-function"></a><span data-ttu-id="eb620-103">CryptUIDlgViewSignerInfo 函式</span><span class="sxs-lookup"><span data-stu-id="eb620-103">CryptUIDlgViewSignerInfo function</span></span>

<span data-ttu-id="eb620-104">\[**CryptUIDlgViewSignerInfo** 函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="eb620-104">\[The **CryptUIDlgViewSignerInfo** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eb620-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="eb620-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="eb620-106">\]</span><span class="sxs-lookup"><span data-stu-id="eb620-106">\]</span></span>

<span data-ttu-id="eb620-107">**CryptUIDlgViewSignerInfo** 函式會顯示一個對話方塊，其中包含已簽署訊息的簽署者資訊。</span><span class="sxs-lookup"><span data-stu-id="eb620-107">The **CryptUIDlgViewSignerInfo** function displays a dialog box that contains the signer information for a signed message.</span></span>

> [!Note]  
> <span data-ttu-id="eb620-108">未在已發行的標頭檔中宣告此函式。</span><span class="sxs-lookup"><span data-stu-id="eb620-108">This function is not declared in a published header file.</span></span> <span data-ttu-id="eb620-109">若要使用此結構，請使用所示的確切格式來宣告。</span><span class="sxs-lookup"><span data-stu-id="eb620-109">To use this structure, declare it in the exact format shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb620-110">語法</span><span class="sxs-lookup"><span data-stu-id="eb620-110">Syntax</span></span>


```C++
);
```



## <a name="parameters"></a><span data-ttu-id="eb620-111">參數</span><span class="sxs-lookup"><span data-stu-id="eb620-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb620-112">*pcvsi* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb620-112">*pcvsi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb620-113">[**CRYPTUI \_ VIEWSIGNERINFO \_ 結構**](cryptui-viewsignerinfo-struct.md)結構的指標，其中包含要顯示的簽署者資訊。</span><span class="sxs-lookup"><span data-stu-id="eb620-113">A pointer to a [**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**](cryptui-viewsignerinfo-struct.md) structure that contains the signer information to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb620-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb620-114">Return value</span></span>

<span data-ttu-id="eb620-115">此函式會在成功時傳回非零值，並在失敗時傳回零。</span><span class="sxs-lookup"><span data-stu-id="eb620-115">This function returns a nonzero value on success and zero on failure.</span></span> <span data-ttu-id="eb620-116">如需擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。</span><span class="sxs-lookup"><span data-stu-id="eb620-116">For extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="eb620-117">從 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回的可能錯誤碼包括但不限於下列各項。</span><span class="sxs-lookup"><span data-stu-id="eb620-117">Possible error codes returned from [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) include, but are not limited to, the following.</span></span>



| <span data-ttu-id="eb620-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="eb620-118">Return code</span></span>                                                                                   | <span data-ttu-id="eb620-119">Description</span><span class="sxs-lookup"><span data-stu-id="eb620-119">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="eb620-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="eb620-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="eb620-121">一或多個引數無效。</span><span class="sxs-lookup"><span data-stu-id="eb620-121">One or more arguments are not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="eb620-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="eb620-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="eb620-123">發生記憶體配置失敗。</span><span class="sxs-lookup"><span data-stu-id="eb620-123">A memory allocation failure occurred.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="eb620-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb620-124">Requirements</span></span>



| <span data-ttu-id="eb620-125">需求</span><span class="sxs-lookup"><span data-stu-id="eb620-125">Requirement</span></span> | <span data-ttu-id="eb620-126">值</span><span class="sxs-lookup"><span data-stu-id="eb620-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb620-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb620-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eb620-128">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb620-128">Windows XP \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eb620-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb620-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eb620-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb620-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb620-131">結束支援</span><span class="sxs-lookup"><span data-stu-id="eb620-131">End of support</span></span><br/> | <span data-ttu-id="eb620-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb620-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="eb620-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="eb620-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb620-134"><dt>Cryptui .lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb620-134"><dt>Cryptui.lib</dt></span></span> </dl>      |
| <span data-ttu-id="eb620-135">DLL</span><span class="sxs-lookup"><span data-stu-id="eb620-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb620-136"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb620-136"><dt>Cryptui.dll</dt></span></span> </dl>      |
| <span data-ttu-id="eb620-137">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="eb620-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="eb620-138">**CryptUIDlgViewSignerInfoW** (Unicode) 和 **CryptUIDlgViewSignerInfoA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="eb620-138">**CryptUIDlgViewSignerInfoW** (Unicode) and **CryptUIDlgViewSignerInfoA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb620-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb620-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb620-140">**CRYPTUI \_ VIEWSIGNERINFO \_ 結構**</span><span class="sxs-lookup"><span data-stu-id="eb620-140">**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**</span></span>](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
