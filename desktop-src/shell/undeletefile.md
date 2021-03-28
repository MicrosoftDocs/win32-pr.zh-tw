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
ms.openlocfilehash: 3bed8995954cdfe05bcc8eea82dc47415033e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194801"
---
# <a name="fm_undelete_proc-function-pointer"></a><span data-ttu-id="42134-103">FM 取消 \_ 刪除進程函式 \_ 指標</span><span class="sxs-lookup"><span data-stu-id="42134-103">FM\_UNDELETE\_PROC function pointer</span></span>

<span data-ttu-id="42134-104">當使用者選擇 [檔案] 功能表中的 [取消 **刪除** ] 命令時，指定 **由 [檔** 管理器] 呼叫的應用程式定義回呼函數。</span><span class="sxs-lookup"><span data-stu-id="42134-104">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="42134-105">語法</span><span class="sxs-lookup"><span data-stu-id="42134-105">Syntax</span></span>


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a><span data-ttu-id="42134-106">參數</span><span class="sxs-lookup"><span data-stu-id="42134-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42134-107">*hwndOwner*</span><span class="sxs-lookup"><span data-stu-id="42134-107">*hwndOwner*</span></span> 
</dt> <dd>

<span data-ttu-id="42134-108">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="42134-108">Type: **HWND**</span></span>

<span data-ttu-id="42134-109">檔案管理員的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="42134-109">The window handle to File Manager.</span></span> <span data-ttu-id="42134-110">取消刪除 DLL 應使用這個控制碼來指定 DLL 可能顯示之任何對話方塊或訊息方塊的擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="42134-110">An undelete DLL should use this handle to specify the owner window for any dialog box or message box the DLL might display.</span></span>

</dd> <dt>

<span data-ttu-id="42134-111">*lpszDir*</span><span class="sxs-lookup"><span data-stu-id="42134-111">*lpszDir*</span></span> 
</dt> <dd>

<span data-ttu-id="42134-112">類型： **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="42134-112">Type: **LPSTR**</span></span>

<span data-ttu-id="42134-113">以 null 終止之字串的位址，其中包含初始目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="42134-113">The address of a null-terminated string that contains the name of the initial directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42134-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="42134-114">Return value</span></span>

<span data-ttu-id="42134-115">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="42134-115">Type: **DWORD**</span></span>

<span data-ttu-id="42134-116">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="42134-116">Returns one of the following values.</span></span>



| <span data-ttu-id="42134-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="42134-117">Return code</span></span>                                                                             | <span data-ttu-id="42134-118">Description</span><span class="sxs-lookup"><span data-stu-id="42134-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="42134-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="42134-119"><dt>**-1**</dt></span></span> </dl>       | <span data-ttu-id="42134-120">發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="42134-120">An error occurred.</span></span><br/>                                      |
| <dl> <span data-ttu-id="42134-121"><dt>**IDOK**</dt></span><span class="sxs-lookup"><span data-stu-id="42134-121"><dt>**IDOK**</dt></span></span> </dl>     | <span data-ttu-id="42134-122">已取消刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="42134-122">A file was undeleted.</span></span> <span data-ttu-id="42134-123">[檔案管理員] 會重新繪製其視窗。</span><span class="sxs-lookup"><span data-stu-id="42134-123">File Manager repaints its window.</span></span><br/> |
| <dl> <span data-ttu-id="42134-124"><dt>**IDCANCEL**</dt></span><span class="sxs-lookup"><span data-stu-id="42134-124"><dt>**IDCANCEL**</dt></span></span> </dl> | <span data-ttu-id="42134-125">未刪除任何檔案。</span><span class="sxs-lookup"><span data-stu-id="42134-125">No file was undeleted.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="42134-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="42134-126">Requirements</span></span>



| <span data-ttu-id="42134-127">需求</span><span class="sxs-lookup"><span data-stu-id="42134-127">Requirement</span></span> | <span data-ttu-id="42134-128">值</span><span class="sxs-lookup"><span data-stu-id="42134-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42134-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42134-129">Minimum supported client</span></span><br/> | <span data-ttu-id="42134-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42134-130">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42134-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42134-131">Minimum supported server</span></span><br/> | <span data-ttu-id="42134-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42134-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="42134-133">標頭</span><span class="sxs-lookup"><span data-stu-id="42134-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="42134-134"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="42134-134"><dt>Wfext.h</dt></span></span> </dl> |



 

 




