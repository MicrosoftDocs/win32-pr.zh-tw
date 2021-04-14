---
title: 'ACM_OPEN 訊息 (Commctrl .h) '
description: 開啟 AVI 剪輯，並在動畫控制項中顯示其第一個畫面格。 您可以明確地傳送此訊息，或使用動畫 \_ 開啟或 \_ OpenEx 宏的動畫。 我們建議使用此訊息的 Unicode 版本 \_ OPENW。
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- ACM_OPEN message Windows 控制項
topic_type:
- apiref
api_name:
- ACM_OPEN
- ACM_OPENA
- ACM_OPENW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0588c0e321efe5cace63baf4016dbaa97f735252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384130"
---
# <a name="acm_open-message"></a><span data-ttu-id="14166-106">\_未結的開啟訊息</span><span class="sxs-lookup"><span data-stu-id="14166-106">ACM\_OPEN message</span></span>

<span data-ttu-id="14166-107">開啟 AVI 剪輯，並在動畫控制項中顯示其第一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="14166-107">Opens an AVI clip and displays its first frame in an animation control.</span></span> <span data-ttu-id="14166-108">您可以明確地傳送此訊息，或使用 [**動畫 \_ 開啟**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) 或 [**\_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) 宏的動畫。</span><span class="sxs-lookup"><span data-stu-id="14166-108">You can send this message explicitly or use the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) or [**Animate\_OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) macro.</span></span> <span data-ttu-id="14166-109">我們建議使用此訊息的 Unicode 版本 \_ OPENW。</span><span class="sxs-lookup"><span data-stu-id="14166-109">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

## <a name="parameters"></a><span data-ttu-id="14166-110">參數</span><span class="sxs-lookup"><span data-stu-id="14166-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14166-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14166-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14166-112">[4.71 版](common-control-versions.md) 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="14166-112">[Version 4.71](common-control-versions.md) and later.</span></span> <span data-ttu-id="14166-113">應從中載入資源之模組的實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="14166-113">An instance handle to the module from which the resource should be loaded.</span></span> <span data-ttu-id="14166-114">將此值設定為 **Null** ，讓控制項使用用來建立視窗的 HINSTANCE 值。</span><span class="sxs-lookup"><span data-stu-id="14166-114">Set this value to **NULL** to have the control use the HINSTANCE value used to create the window.</span></span> <span data-ttu-id="14166-115">請注意，如果視窗是由 DLL 所建立，則 *wParam* 的預設值為 DLL 的 HINSTANCE 值，而不是呼叫 dll 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="14166-115">Note that if the window is created by a DLL, the default value for *wParam* is the HINSTANCE value of the DLL, not of the application that calls the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="14166-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14166-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14166-117">緩衝區的指標，其中包含 AVI 檔案的路徑或 AVI 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="14166-117">A pointer to a buffer that contains the path of the AVI file or the name of an AVI resource.</span></span> <span data-ttu-id="14166-118">或者，此參數可以包含 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中的 AVI 資源識別碼，以及 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中的零。</span><span class="sxs-lookup"><span data-stu-id="14166-118">Alternatively, this parameter can consist of the AVI resource identifier in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and zero in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="14166-119">若要建立這個值，請使用 [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) 宏。</span><span class="sxs-lookup"><span data-stu-id="14166-119">To create this value, use the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="14166-120">控制項會從傳遞給 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 函式的實例控制碼所指定的模組、建立動畫的宏或 [**建立 \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) 控制項的對話方塊建立函數載入 AVI 資源。</span><span class="sxs-lookup"><span data-stu-id="14166-120">The control loads the AVI resource from the module specified by the instance handle passed to the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function, the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro, or the dialog box creation function that created the control.</span></span> <span data-ttu-id="14166-121">在 [4.71 版](common-control-versions.md) 和更新版本中，資源是從 *wParam* 所指定的模組載入。</span><span class="sxs-lookup"><span data-stu-id="14166-121">In [Version 4.71](common-control-versions.md) and later, the resource is loaded from the module specified by *wParam*.</span></span> <span data-ttu-id="14166-122">AVI 資源必須有 "AVI" 類型。</span><span class="sxs-lookup"><span data-stu-id="14166-122">An AVI resource must have the "AVI" type.</span></span> <span data-ttu-id="14166-123">如果這個參數為 **Null**，系統會關閉先前針對指定動畫控制項開啟的 AVI 檔案（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="14166-123">If this parameter is **NULL**, the system closes the AVI file that was previously opened for the specified animation control, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14166-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="14166-124">Return value</span></span>

<span data-ttu-id="14166-125">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="14166-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="14166-126">備註</span><span class="sxs-lookup"><span data-stu-id="14166-126">Remarks</span></span>

<span data-ttu-id="14166-127">*LpszName* 所指定的 AVI 檔案或資源不得包含音訊。</span><span class="sxs-lookup"><span data-stu-id="14166-127">The AVI file or resource specified by *lpszName* must not contain audio.</span></span>

<span data-ttu-id="14166-128">我們建議使用此訊息的 Unicode 版本 \_ OPENW。</span><span class="sxs-lookup"><span data-stu-id="14166-128">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

<span data-ttu-id="14166-129">您只能開啟無訊息的 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="14166-129">You can only open silent AVI clips.</span></span> <span data-ttu-id="14166-130">\_如果 *lParam* 指定包含音效的 AVI 剪輯，則開啟的 [開啟] 和 [建立 [**動畫動畫 \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) ] 會失敗。</span><span class="sxs-lookup"><span data-stu-id="14166-130">ACM\_OPEN and [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) fail if *lParam* specifies an AVI clip that contains sound.</span></span>

<span data-ttu-id="14166-131">您可以使用 [**「 \_ 左右動畫**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) 」來關閉先前針對指定動畫控制項開啟的 AVI 檔案或 avi 資源。</span><span class="sxs-lookup"><span data-stu-id="14166-131">You can use [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) to close an AVI file or AVI resource that was previously opened for the specified animation control.</span></span>

## <a name="requirements"></a><span data-ttu-id="14166-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="14166-132">Requirements</span></span>



| <span data-ttu-id="14166-133">需求</span><span class="sxs-lookup"><span data-stu-id="14166-133">Requirement</span></span> | <span data-ttu-id="14166-134">值</span><span class="sxs-lookup"><span data-stu-id="14166-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14166-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14166-135">Minimum supported client</span></span><br/> | <span data-ttu-id="14166-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14166-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14166-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14166-137">Minimum supported server</span></span><br/> | <span data-ttu-id="14166-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14166-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14166-139">標頭</span><span class="sxs-lookup"><span data-stu-id="14166-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="14166-140"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="14166-140"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="14166-141">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="14166-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="14166-142">進行中 **\_OPENW** (Unicode) 和 **\_ OPENA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="14166-142">**ACM\_OPENW** (Unicode) and **ACM\_OPENA** (ANSI)</span></span><br/>                         |



 

