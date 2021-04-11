---
description: 在 [內容] 工作表上，顯示指定資料夾的 [資料夾共用] 索引標籤。
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: ShowShareFolderUI 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: e6270f72d1574a21b98ac9ee3151af1f34f08a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319547"
---
# <a name="showsharefolderui-function"></a><span data-ttu-id="2f6e8-103">ShowShareFolderUI 函式</span><span class="sxs-lookup"><span data-stu-id="2f6e8-103">ShowShareFolderUI function</span></span>

<span data-ttu-id="2f6e8-104">在 [內容] 工作表上，顯示指定資料夾的 [ **資料夾共用** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2f6e8-104">Displays the **Folder Sharing** tab on the properties sheet for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f6e8-105">語法</span><span class="sxs-lookup"><span data-stu-id="2f6e8-105">Syntax</span></span>


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="2f6e8-106">參數</span><span class="sxs-lookup"><span data-stu-id="2f6e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f6e8-107">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f6e8-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f6e8-108">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="2f6e8-108">Type: **HWND**</span></span>

<span data-ttu-id="2f6e8-109">屬性工作表的父視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="2f6e8-109">A handle to the parent window for the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="2f6e8-110">*pszPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f6e8-110">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f6e8-111">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="2f6e8-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="2f6e8-112">字串的指標，指定資料夾的路徑，該路徑會顯示資料夾的 [ **共用** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2f6e8-112">A pointer to a string that specifies the path to the folder that displays its **Folder Sharing** tab.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f6e8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f6e8-113">Return value</span></span>

<span data-ttu-id="2f6e8-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2f6e8-114">Type: **HRESULT**</span></span>

<span data-ttu-id="2f6e8-115">此函式一律會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2f6e8-115">This function always returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f6e8-116">備註</span><span class="sxs-lookup"><span data-stu-id="2f6e8-116">Remarks</span></span>

<span data-ttu-id="2f6e8-117">此函數沒有相關聯的 .lib 檔案。</span><span class="sxs-lookup"><span data-stu-id="2f6e8-117">This function has no associated .lib file.</span></span> <span data-ttu-id="2f6e8-118">您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 才能使用它。</span><span class="sxs-lookup"><span data-stu-id="2f6e8-118">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f6e8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f6e8-119">Requirements</span></span>



| <span data-ttu-id="2f6e8-120">需求</span><span class="sxs-lookup"><span data-stu-id="2f6e8-120">Requirement</span></span> | <span data-ttu-id="2f6e8-121">值</span><span class="sxs-lookup"><span data-stu-id="2f6e8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f6e8-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f6e8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2f6e8-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f6e8-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2f6e8-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f6e8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2f6e8-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f6e8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2f6e8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2f6e8-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f6e8-127"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f6e8-127"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="2f6e8-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="2f6e8-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2f6e8-129">**ShowShareFolderUIW** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="2f6e8-129">**ShowShareFolderUIW** (Unicode)</span></span><br/>                                            |



## <a name="see-also"></a><span data-ttu-id="2f6e8-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f6e8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f6e8-131">**CanShareFolderW**</span><span class="sxs-lookup"><span data-stu-id="2f6e8-131">**CanShareFolderW**</span></span>](cansharefolderw.md)
</dt> </dl>

 

 
