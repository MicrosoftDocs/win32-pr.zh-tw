---
description: 用來判斷是否要在 web view 中顯示 [共用此資料夾] 選項。
title: CanShareFolderW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: cf7d0feb31666f3a918c0307a0b0983bff246fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511063"
---
# <a name="cansharefolderw-function"></a><span data-ttu-id="9e6ac-103">CanShareFolderW 函式</span><span class="sxs-lookup"><span data-stu-id="9e6ac-103">CanShareFolderW function</span></span>

<span data-ttu-id="9e6ac-104">\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。</span><span class="sxs-lookup"><span data-stu-id="9e6ac-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="9e6ac-105">它可能會在後續版本的 Windows 中改變或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="9e6ac-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="9e6ac-106">用來判斷是否要在 web view 中顯示 [ **共用此資料夾** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="9e6ac-106">Used to determine whether to show the **Share this folder** option in web view.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e6ac-107">語法</span><span class="sxs-lookup"><span data-stu-id="9e6ac-107">Syntax</span></span>


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="9e6ac-108">參數</span><span class="sxs-lookup"><span data-stu-id="9e6ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e6ac-109">*pszPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e6ac-109">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e6ac-110">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="9e6ac-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="9e6ac-111">指定要測試之資料夾路徑的字串指標。</span><span class="sxs-lookup"><span data-stu-id="9e6ac-111">A pointer to a string that specifies the path of the folder to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e6ac-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e6ac-112">Return value</span></span>

<span data-ttu-id="9e6ac-113">類型： **STDAPI**</span><span class="sxs-lookup"><span data-stu-id="9e6ac-113">Type: **STDAPI**</span></span>

<span data-ttu-id="9e6ac-114">傳回值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="9e6ac-114">Return values include the following.</span></span>



| <span data-ttu-id="9e6ac-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="9e6ac-115">Return code/value</span></span>                                                                        | <span data-ttu-id="9e6ac-116">Description</span><span class="sxs-lookup"><span data-stu-id="9e6ac-116">Description</span></span>                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e6ac-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9e6ac-117"><dt>**S\_OK**</dt></span></span> </dl>     | <span data-ttu-id="9e6ac-118">*PszPath* 所指向的路徑會指定可共用的資料夾。</span><span class="sxs-lookup"><span data-stu-id="9e6ac-118">The path pointed to by *pszPath* specifies a folder that can be shared.</span></span><br/>    |
| <dl> <span data-ttu-id="9e6ac-119"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="9e6ac-119"><dt>**S\_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="9e6ac-120">*PszPath* 所指向的路徑會指定無法共用的資料夾。</span><span class="sxs-lookup"><span data-stu-id="9e6ac-120">The path pointed to by *pszPath* specifies a folder that cannot be shared.</span></span><br/> |
| <dl> <span data-ttu-id="9e6ac-121"><dt>HRESULT 錯誤</dt></span><span class="sxs-lookup"><span data-stu-id="9e6ac-121"><dt>HRESULT error</dt></span></span> </dl> | <span data-ttu-id="9e6ac-122">發生錯誤了。</span><span class="sxs-lookup"><span data-stu-id="9e6ac-122">An error has occurred.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="9e6ac-123">備註</span><span class="sxs-lookup"><span data-stu-id="9e6ac-123">Remarks</span></span>

<span data-ttu-id="9e6ac-124">此函數沒有相關聯的 .lib 檔案。</span><span class="sxs-lookup"><span data-stu-id="9e6ac-124">This function has no associated .lib file.</span></span> <span data-ttu-id="9e6ac-125">您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 才能使用它。</span><span class="sxs-lookup"><span data-stu-id="9e6ac-125">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e6ac-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e6ac-126">Requirements</span></span>



| <span data-ttu-id="9e6ac-127">需求</span><span class="sxs-lookup"><span data-stu-id="9e6ac-127">Requirement</span></span> | <span data-ttu-id="9e6ac-128">值</span><span class="sxs-lookup"><span data-stu-id="9e6ac-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e6ac-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e6ac-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9e6ac-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e6ac-130">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9e6ac-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e6ac-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9e6ac-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e6ac-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9e6ac-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9e6ac-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e6ac-134"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e6ac-134"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e6ac-135">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="9e6ac-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9e6ac-136">**CanShareFolderW** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="9e6ac-136">**CanShareFolderW** (Unicode)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="9e6ac-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e6ac-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e6ac-138">**ShowShareFolderUI**</span><span class="sxs-lookup"><span data-stu-id="9e6ac-138">**ShowShareFolderUI**</span></span>](./showsharefolderui.md)
</dt> </dl>

 

 
