---
description: 指示 IME 視窗取得狀態視窗的位置。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配如下所示的參數設定。
ms.assetid: 59c7baae-1b8a-4761-9814-31afd8d39691
title: 'IMC_GETSTATUSWINDOWPOS 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd17c5787d9ef8c787e62a556afa2f136bd65c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966741"
---
# <a name="imc_getstatuswindowpos-command"></a><span data-ttu-id="ec644-104">IMC \_ GETSTATUSWINDOWPOS 命令</span><span class="sxs-lookup"><span data-stu-id="ec644-104">IMC\_GETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="ec644-105">指示 IME 視窗取得狀態視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="ec644-105">Instructs an IME window to get the position of the status window.</span></span> <span data-ttu-id="ec644-106">若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配如下所示的參數設定。</span><span class="sxs-lookup"><span data-stu-id="ec644-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="ec644-107">參數</span><span class="sxs-lookup"><span data-stu-id="ec644-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec644-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec644-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="ec644-109">設定為 IMC \_ GETSTATUSWINDOWPOS。</span><span class="sxs-lookup"><span data-stu-id="ec644-109">Set to IMC\_GETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="ec644-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec644-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ec644-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="ec644-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec644-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec644-112">Return Value</span></span>

<span data-ttu-id="ec644-113">傳回 [**點**](/previous-versions//dd162808(v=vs.85)) 結構，此結構包含相對於螢幕左上角之螢幕座標中狀態視窗位置的 x 座標和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="ec644-113">Returns a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the status window position in screen coordinates, relative to the upper left corner of the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec644-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec644-114">Requirements</span></span>



| <span data-ttu-id="ec644-115">需求</span><span class="sxs-lookup"><span data-stu-id="ec644-115">Requirement</span></span> | <span data-ttu-id="ec644-116">值</span><span class="sxs-lookup"><span data-stu-id="ec644-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec644-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec644-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ec644-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec644-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ec644-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec644-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ec644-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec644-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ec644-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ec644-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec644-122"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ec644-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec644-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec644-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec644-124">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="ec644-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="ec644-125">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="ec644-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="ec644-126">**WM \_ IME \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="ec644-126">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
