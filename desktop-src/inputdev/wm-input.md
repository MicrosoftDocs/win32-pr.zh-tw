---
title: 'WM_INPUT 訊息 (Winuser .h) '
description: 傳送至正在取得原始輸入的視窗。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- WM_INPUT 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384421"
---
# <a name="wm_input-message"></a><span data-ttu-id="8bed7-105">WM \_ 輸入訊息</span><span class="sxs-lookup"><span data-stu-id="8bed7-105">WM\_INPUT message</span></span>

<span data-ttu-id="8bed7-106">傳送至正在取得原始輸入的視窗。</span><span class="sxs-lookup"><span data-stu-id="8bed7-106">Sent to the window that is getting raw input.</span></span>

<span data-ttu-id="8bed7-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="8bed7-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a><span data-ttu-id="8bed7-108">參數</span><span class="sxs-lookup"><span data-stu-id="8bed7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bed7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8bed7-109">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="8bed7-110">輸入代碼。</span><span class="sxs-lookup"><span data-stu-id="8bed7-110">The input code.</span></span> <span data-ttu-id="8bed7-111">使用 [**get \_ RAWINPUT \_ CODE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) 宏來取得值。</span><span class="sxs-lookup"><span data-stu-id="8bed7-111">Use [**GET\_RAWINPUT\_CODE\_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) macro to get the value.</span></span>

<span data-ttu-id="8bed7-112">可以是下列值之一：</span><span class="sxs-lookup"><span data-stu-id="8bed7-112">Can be one of the following values:</span></span>

| <span data-ttu-id="8bed7-113">值</span><span class="sxs-lookup"><span data-stu-id="8bed7-113">Value</span></span> | <span data-ttu-id="8bed7-114">意義</span><span class="sxs-lookup"><span data-stu-id="8bed7-114">Meaning</span></span> |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <span data-ttu-id="8bed7-115"><dt>**邊緣 \_輸入**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8bed7-115"><dt>**RIM\_INPUT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="8bed7-116">當應用程式在前景時，就會發生輸入。</span><span class="sxs-lookup"><span data-stu-id="8bed7-116">Input occurred while the application was in the foreground.</span></span> </br> <span data-ttu-id="8bed7-117">應用程式必須呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ，讓系統可以執行清除。</span><span class="sxs-lookup"><span data-stu-id="8bed7-117">The application must call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) so the system can perform cleanup.</span></span> |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <span data-ttu-id="8bed7-118"><dt>**邊緣 \_INPUTSINK**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8bed7-118"><dt>**RIM\_INPUTSINK**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="8bed7-119">當應用程式不在前景時，就會發生輸入。</span><span class="sxs-lookup"><span data-stu-id="8bed7-119">Input occurred while the application was not in the foreground.</span></span> |

</dd> <dt>

<span data-ttu-id="8bed7-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8bed7-120">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="8bed7-121">[**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)結構的 **HRAWINPUT** 控制碼，其中包含來自裝置的原始輸入。</span><span class="sxs-lookup"><span data-stu-id="8bed7-121">A **HRAWINPUT** handle to the [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structure that contains the raw input from the device.</span></span> <span data-ttu-id="8bed7-122">若要取得原始資料，請在 [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)的呼叫中使用這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="8bed7-122">To get the raw data, use this handle in the call to [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bed7-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="8bed7-123">Return value</span></span>

<span data-ttu-id="8bed7-124">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="8bed7-124">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bed7-125">備註</span><span class="sxs-lookup"><span data-stu-id="8bed7-125">Remarks</span></span>

<span data-ttu-id="8bed7-126">只有在應用程式使用有效的裝置規格呼叫 [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) 時，才可以使用原始輸入。</span><span class="sxs-lookup"><span data-stu-id="8bed7-126">Raw input is available only when the application calls [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with valid device specifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bed7-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bed7-127">Requirements</span></span>

| <span data-ttu-id="8bed7-128">需求</span><span class="sxs-lookup"><span data-stu-id="8bed7-128">Requirement</span></span> | <span data-ttu-id="8bed7-129">值</span><span class="sxs-lookup"><span data-stu-id="8bed7-129">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="8bed7-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8bed7-130">Minimum supported client</span></span> | <span data-ttu-id="8bed7-131">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bed7-131">Windows XP \[desktop apps only\]</span></span> |
| <span data-ttu-id="8bed7-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8bed7-132">Minimum supported server</span></span> | <span data-ttu-id="8bed7-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bed7-133">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="8bed7-134">標頭</span><span class="sxs-lookup"><span data-stu-id="8bed7-134">Header</span></span> | <dl> <span data-ttu-id="8bed7-135"><dt>**Winuser (包含) 的 Windows .h**</dt></span><span class="sxs-lookup"><span data-stu-id="8bed7-135"><dt>**Winuser.h (include Windows.h)** </dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="8bed7-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bed7-136">See also</span></span>

<span data-ttu-id="8bed7-137">**參考**</span><span class="sxs-lookup"><span data-stu-id="8bed7-137">**Reference**</span></span>

[<span data-ttu-id="8bed7-138">**GetRawInputData**</span><span class="sxs-lookup"><span data-stu-id="8bed7-138">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[<span data-ttu-id="8bed7-139">**RegisterRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="8bed7-139">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="8bed7-140">**RAWINPUT**</span><span class="sxs-lookup"><span data-stu-id="8bed7-140">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)

[<span data-ttu-id="8bed7-141">**取得 \_ RAWINPUT 程式 \_ 代碼 \_ WPARAM**</span><span class="sxs-lookup"><span data-stu-id="8bed7-141">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

<span data-ttu-id="8bed7-142">**概念**</span><span class="sxs-lookup"><span data-stu-id="8bed7-142">**Conceptual**</span></span>

[<span data-ttu-id="8bed7-143">原始輸入</span><span class="sxs-lookup"><span data-stu-id="8bed7-143">Raw Input</span></span>](raw-input.md)
