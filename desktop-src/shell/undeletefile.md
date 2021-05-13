---
description: 當使用者選擇 [檔案] 功能表中的 [取消刪除] 命令時，指定由 [檔案管理員] 呼叫的應用程式定義回呼函數。
title: 'FM_UNDELETE_PROC 函式指標 (Wfext) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_UNDELETE_PROC
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 456b053e-e83d-43af-9691-57e1d4fd3f8f
ms.openlocfilehash: b7549b521c241429f1c5c7edb7f83eadf25f5d37
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842419"
---
# <a name="fm_undelete_proc-function-pointer"></a><span data-ttu-id="1ecc6-103">FM 取消 \_ 刪除進程函式 \_ 指標</span><span class="sxs-lookup"><span data-stu-id="1ecc6-103">FM\_UNDELETE\_PROC function pointer</span></span>

<span data-ttu-id="1ecc6-104">當使用者選擇 [檔案] 功能表中的 [取消 **刪除** ] 命令時，指定 **由 [檔** 管理器] 呼叫的應用程式定義回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1ecc6-104">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ecc6-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ecc6-105">Syntax</span></span>


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a><span data-ttu-id="1ecc6-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ecc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ecc6-107">*hwndOwner*</span><span class="sxs-lookup"><span data-stu-id="1ecc6-107">*hwndOwner*</span></span> 
</dt> <dd>

<span data-ttu-id="1ecc6-108">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="1ecc6-108">Type: **HWND**</span></span>

<span data-ttu-id="1ecc6-109">檔案管理員的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="1ecc6-109">The window handle to File Manager.</span></span> <span data-ttu-id="1ecc6-110">取消刪除 DLL 應使用這個控制碼來指定 DLL 可能顯示之任何對話方塊或訊息方塊的擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="1ecc6-110">An undelete DLL should use this handle to specify the owner window for any dialog box or message box the DLL might display.</span></span>

</dd> <dt>

<span data-ttu-id="1ecc6-111">*lpszDir*</span><span class="sxs-lookup"><span data-stu-id="1ecc6-111">*lpszDir*</span></span> 
</dt> <dd>

<span data-ttu-id="1ecc6-112">類型： **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="1ecc6-112">Type: **LPSTR**</span></span>

<span data-ttu-id="1ecc6-113">以 null 終止之字串的位址，其中包含初始目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ecc6-113">The address of a null-terminated string that contains the name of the initial directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ecc6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ecc6-114">Return value</span></span>

<span data-ttu-id="1ecc6-115">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1ecc6-115">Type: **DWORD**</span></span>

<span data-ttu-id="1ecc6-116">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1ecc6-116">Returns one of the following values.</span></span>



| <span data-ttu-id="1ecc6-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1ecc6-117">Return code</span></span>                                                                             | <span data-ttu-id="1ecc6-118">描述</span><span class="sxs-lookup"><span data-stu-id="1ecc6-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ecc6-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="1ecc6-119"><dt>**-1**</dt></span></span> </dl>       | <span data-ttu-id="1ecc6-120">發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="1ecc6-120">An error occurred.</span></span><br/>                                      |
| <dl> <span data-ttu-id="1ecc6-121"><dt>**IDOK**</dt></span><span class="sxs-lookup"><span data-stu-id="1ecc6-121"><dt>**IDOK**</dt></span></span> </dl>     | <span data-ttu-id="1ecc6-122">已取消刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="1ecc6-122">A file was undeleted.</span></span> <span data-ttu-id="1ecc6-123">[檔案管理員] 會重新繪製其視窗。</span><span class="sxs-lookup"><span data-stu-id="1ecc6-123">File Manager repaints its window.</span></span><br/> |
| <dl> <span data-ttu-id="1ecc6-124"><dt>**IDCANCEL**</dt></span><span class="sxs-lookup"><span data-stu-id="1ecc6-124"><dt>**IDCANCEL**</dt></span></span> </dl> | <span data-ttu-id="1ecc6-125">未刪除任何檔案。</span><span class="sxs-lookup"><span data-stu-id="1ecc6-125">No file was undeleted.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="1ecc6-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ecc6-126">Requirements</span></span>



| <span data-ttu-id="1ecc6-127">需求</span><span class="sxs-lookup"><span data-stu-id="1ecc6-127">Requirement</span></span> | <span data-ttu-id="1ecc6-128">值</span><span class="sxs-lookup"><span data-stu-id="1ecc6-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ecc6-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ecc6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1ecc6-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ecc6-130">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ecc6-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ecc6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1ecc6-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ecc6-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1ecc6-133">標頭</span><span class="sxs-lookup"><span data-stu-id="1ecc6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ecc6-134"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ecc6-134"><dt>Wfext.h</dt></span></span> </dl> |



 

 




