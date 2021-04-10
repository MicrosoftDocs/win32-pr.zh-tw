---
title: 'WM_INPUT_DEVICE_CHANGE 訊息 (Winuser .h) '
description: 傳送至已註冊要接收原始輸入的視窗。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- WM_INPUT_DEVICE_CHANGE 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0edb6dbfbcfa9e024ba85613e3b7671e5f416397
ms.sourcegitcommit: 47d1f3859035a69340571bf50c3d36e0abeb2126
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "104024269"
---
# <a name="wm_input_device_change-message"></a><span data-ttu-id="07eb5-105">WM_INPUT_DEVICE_CHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="07eb5-105">WM_INPUT_DEVICE_CHANGE message</span></span>

## <a name="description"></a><span data-ttu-id="07eb5-106">Description</span><span class="sxs-lookup"><span data-stu-id="07eb5-106">Description</span></span>

<span data-ttu-id="07eb5-107">傳送至已註冊要接收原始輸入的視窗。</span><span class="sxs-lookup"><span data-stu-id="07eb5-107">Sent to the window that registered to receive raw input.</span></span> 

<span data-ttu-id="07eb5-108">只有在應用程式使用[RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice)旗標呼叫[RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)之後，才可以使用原始輸入通知。</span><span class="sxs-lookup"><span data-stu-id="07eb5-108">Raw input notifications are available only after the application calls [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) flag.</span></span>

<span data-ttu-id="07eb5-109">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="07eb5-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a><span data-ttu-id="07eb5-110">參數</span><span class="sxs-lookup"><span data-stu-id="07eb5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07eb5-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07eb5-111">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="07eb5-112">類型： **WPARAM**</span><span class="sxs-lookup"><span data-stu-id="07eb5-112">Type: **WPARAM**</span></span>

<span data-ttu-id="07eb5-113">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="07eb5-113">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="07eb5-114">值</span><span class="sxs-lookup"><span data-stu-id="07eb5-114">Value</span></span>                    | <span data-ttu-id="07eb5-115">意義</span><span class="sxs-lookup"><span data-stu-id="07eb5-115">Meaning</span></span>                                    |
|--------------------------|--------------------------------------------|
| <span data-ttu-id="07eb5-116">**GIDC \_ 抵達**</span><span class="sxs-lookup"><span data-stu-id="07eb5-116">**GIDC\_ARRIVAL**</span></span> </br><span data-ttu-id="07eb5-117">1</span><span class="sxs-lookup"><span data-stu-id="07eb5-117">1</span></span> | <span data-ttu-id="07eb5-118">系統已新增新的裝置。</span><span class="sxs-lookup"><span data-stu-id="07eb5-118">A new device has been added to the system.</span></span> </br> <span data-ttu-id="07eb5-119">您可以呼叫 [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) 來取得有關裝置的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="07eb5-119">You can call [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) to get more information regarding the device.</span></span> |
| <span data-ttu-id="07eb5-120">**GIDC \_ 移除**</span><span class="sxs-lookup"><span data-stu-id="07eb5-120">**GIDC\_REMOVAL**</span></span> </br><span data-ttu-id="07eb5-121">2</span><span class="sxs-lookup"><span data-stu-id="07eb5-121">2</span></span> | <span data-ttu-id="07eb5-122">裝置已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="07eb5-122">A device has been removed from the system.</span></span> |

</dd> <dt>

<span data-ttu-id="07eb5-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07eb5-123">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="07eb5-124">類型： **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="07eb5-124">Type: **LPARAM**</span></span>

<span data-ttu-id="07eb5-125">原始輸入裝置的 **控制碼** 。</span><span class="sxs-lookup"><span data-stu-id="07eb5-125">The **HANDLE** to the raw input device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07eb5-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="07eb5-126">Return value</span></span>

<span data-ttu-id="07eb5-127">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="07eb5-127">If an application processes this message, it should return zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="07eb5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07eb5-128">See also</span></span>

<span data-ttu-id="07eb5-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="07eb5-129">**Conceptual**</span></span>

[<span data-ttu-id="07eb5-130">原始輸入</span><span class="sxs-lookup"><span data-stu-id="07eb5-130">Raw Input</span></span>](/windows/desktop/inputdev/raw-input)

<span data-ttu-id="07eb5-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="07eb5-131">**Reference**</span></span>

[<span data-ttu-id="07eb5-132">RegisterRawInputDevices</span><span class="sxs-lookup"><span data-stu-id="07eb5-132">RegisterRawInputDevices</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="07eb5-133">RAWINPUTDEVICE 結構</span><span class="sxs-lookup"><span data-stu-id="07eb5-133">RAWINPUTDEVICE structure</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

