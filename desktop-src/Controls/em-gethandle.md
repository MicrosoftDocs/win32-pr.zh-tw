---
title: 'EM_GETHANDLE 訊息 (Winuser .h) '
description: 取得目前配置給多行編輯控制項文字的記憶體控制碼。
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- EM_GETHANDLE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88a466394b48d2d726621e50a7e2c5df2f747f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508923"
---
# <a name="em_gethandle-message"></a><span data-ttu-id="1d628-104">EM \_ GETHANDLE 訊息</span><span class="sxs-lookup"><span data-stu-id="1d628-104">EM\_GETHANDLE message</span></span>

<span data-ttu-id="1d628-105">取得目前配置給多行編輯控制項文字的記憶體控制碼。</span><span class="sxs-lookup"><span data-stu-id="1d628-105">Gets a handle of the memory currently allocated for a multiline edit control's text.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d628-106">參數</span><span class="sxs-lookup"><span data-stu-id="1d628-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d628-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d628-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d628-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="1d628-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1d628-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d628-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d628-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="1d628-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d628-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d628-111">Return value</span></span>

<span data-ttu-id="1d628-112">傳回值是識別保存編輯控制項內容之緩衝區的記憶體控制碼。</span><span class="sxs-lookup"><span data-stu-id="1d628-112">The return value is a memory handle identifying the buffer that holds the content of the edit control.</span></span> <span data-ttu-id="1d628-113">如果發生錯誤（例如將訊息傳送到單行編輯控制項），則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="1d628-113">If an error occurs, such as sending the message to a single-line edit control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d628-114">備註</span><span class="sxs-lookup"><span data-stu-id="1d628-114">Remarks</span></span>

<span data-ttu-id="1d628-115">如果函式成功，應用程式可以藉由將傳回值轉換成 [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) 並將它傳遞給 [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)，來存取編輯控制項的內容。</span><span class="sxs-lookup"><span data-stu-id="1d628-115">If the function succeeds, the application can access the contents of the edit control by casting the return value to [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) and passing it to [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock).</span></span> <span data-ttu-id="1d628-116">**LocalLock** 會根據 ANSI 或 Unicode 函數是否建立控制項，傳回以 null 結束的 **CHAR** s 或 **WCHAR** s 陣列的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="1d628-116">**LocalLock** returns a pointer to a buffer that is a null-terminated array of **CHAR** s or **WCHAR** s, depending on whether an ANSI or Unicode function created the control.</span></span> <span data-ttu-id="1d628-117">例如，如果使用 [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ，則緩衝區是 **CHAR** s 的陣列，但如果使用 **CreateWindowExW** ，則緩衝區是 **WCHAR** 的陣列。</span><span class="sxs-lookup"><span data-stu-id="1d628-117">For example, if [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) was used the buffer is an array of **CHAR** s, but if **CreateWindowExW** was used the buffer is an array of **WCHAR** s.</span></span> <span data-ttu-id="1d628-118">應用程式可能不會變更緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="1d628-118">The application may not change the contents of the buffer.</span></span> <span data-ttu-id="1d628-119">若要解除鎖定緩衝區，應用程式會先呼叫 [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) ，然後再允許編輯控制項接收新訊息。</span><span class="sxs-lookup"><span data-stu-id="1d628-119">To unlock the buffer, the application calls [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) before allowing the edit control to receive new messages.</span></span>

> [!Note]  
> <span data-ttu-id="1d628-120">針對 Comctl32.dll 第6版，無論 ANSI 或 Unicode 函數是否建立了編輯控制項，緩衝區一律會包含 **WCHAR** 的陣列。</span><span class="sxs-lookup"><span data-stu-id="1d628-120">For Comctl32.dll version 6, the buffer always contains an array of **WCHAR** s, regardless of whether an ANSI or Unicode function created the edit control.</span></span> <span data-ttu-id="1d628-121">如需 DLL 版本的詳細資訊，請參閱 [通用控制項版本](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="1d628-121">For more information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

 

<span data-ttu-id="1d628-122">如果您的應用程式無法遵守 **EM \_ GETHANDLE** 所加諸的限制，請使用 [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) 和 [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) 函數將編輯控制項的內容複寫到應用程式提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1d628-122">If your application cannot abide by the restrictions imposed by **EM\_GETHANDLE**, use the [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) and [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) functions to copy the contents of the edit control into an application-provided buffer.</span></span>

<span data-ttu-id="1d628-123">**Rich Edit：** 不支援 **EM \_ GETHANDLE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="1d628-123">**Rich Edit:** The **EM\_GETHANDLE** message is not supported.</span></span> <span data-ttu-id="1d628-124">Rich edit 控制項不會將文字儲存為簡單字元陣列。</span><span class="sxs-lookup"><span data-stu-id="1d628-124">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d628-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d628-125">Requirements</span></span>



| <span data-ttu-id="1d628-126">需求</span><span class="sxs-lookup"><span data-stu-id="1d628-126">Requirement</span></span> | <span data-ttu-id="1d628-127">值</span><span class="sxs-lookup"><span data-stu-id="1d628-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d628-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d628-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1d628-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d628-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1d628-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d628-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1d628-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d628-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d628-132">標頭</span><span class="sxs-lookup"><span data-stu-id="1d628-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d628-133"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1d628-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d628-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d628-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d628-135">**參考**</span><span class="sxs-lookup"><span data-stu-id="1d628-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1d628-136">**EM \_ SETHANDLE**</span><span class="sxs-lookup"><span data-stu-id="1d628-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

<span data-ttu-id="1d628-137">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="1d628-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1d628-138">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="1d628-138">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="1d628-139">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="1d628-139">**GetWindowTextLength**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="1d628-140">**LocalLock**</span><span class="sxs-lookup"><span data-stu-id="1d628-140">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[<span data-ttu-id="1d628-141">**LocalUnlock**</span><span class="sxs-lookup"><span data-stu-id="1d628-141">**LocalUnlock**</span></span>](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 

