---
description: 當系統要求視窗要接收的系統手勢時傳送。
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: 'WM_TABLET_QUERYSYSTEMGESTURESTATUS 訊息 (Tpcshrd .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395196f963cae9b8d18697276e546f1eba05b245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847974"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a><span data-ttu-id="bca7c-103">WM \_ 平板電腦 \_ QUERYSYSTEMGESTURESTATUS 訊息</span><span class="sxs-lookup"><span data-stu-id="bca7c-103">WM\_TABLET\_QUERYSYSTEMGESTURESTATUS message</span></span>

<span data-ttu-id="bca7c-104">當系統要求視窗要接收的系統手勢時傳送。</span><span class="sxs-lookup"><span data-stu-id="bca7c-104">Sent when the system asks a window which system gestures it would like to receive.</span></span>


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a><span data-ttu-id="bca7c-105">參數</span><span class="sxs-lookup"><span data-stu-id="bca7c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bca7c-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bca7c-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bca7c-107">未使用。</span><span class="sxs-lookup"><span data-stu-id="bca7c-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="bca7c-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bca7c-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bca7c-109">代表螢幕座標的點值。</span><span class="sxs-lookup"><span data-stu-id="bca7c-109">A point value that represents the screen coordinates.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bca7c-110">備註</span><span class="sxs-lookup"><span data-stu-id="bca7c-110">Remarks</span></span>

<span data-ttu-id="bca7c-111">藉由處理此訊息，您可以動態停用視窗區域的筆觸。</span><span class="sxs-lookup"><span data-stu-id="bca7c-111">By handling this message, you can dynamically disable flicks for regions of a window.</span></span>

> [!Note]  
> <span data-ttu-id="bca7c-112">您可以使用和宏，將 *lParam* 轉換為 x 座標和 y 座標 `GET_X_LPARAM` `GET_Y_LPARAM` 。</span><span class="sxs-lookup"><span data-stu-id="bca7c-112">The *lParam* can be converted to x-coordinates and y-coordinates by using the `GET_X_LPARAM` and `GET_Y_LPARAM` macros.</span></span>

 

<span data-ttu-id="bca7c-113">根據預設，您的視窗將會接收所有系統手勢事件。</span><span class="sxs-lookup"><span data-stu-id="bca7c-113">By default, your window will receive all system gesture events.</span></span> <span data-ttu-id="bca7c-114">您可以在 **WndProc** 中回應 **WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS** 訊息，以選擇您希望視窗接收的事件，以及您想要停用的事件。</span><span class="sxs-lookup"><span data-stu-id="bca7c-114">You can choose which events you would like your window to receive and which events you would like disabled by responding to the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message in your **WndProc**.</span></span> <span data-ttu-id="bca7c-115">**WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS** 訊息定義于 tpcshrd 中。</span><span class="sxs-lookup"><span data-stu-id="bca7c-115">The **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message is defined in tpcshrd.h.</span></span> <span data-ttu-id="bca7c-116">啟用及停用系統 tablet 系統手勢的值也會在 tpcshrd 中定義，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bca7c-116">The values to enable and disable system tablet system gestures are also defined in tpcshrd.h as follows:</span></span>

``` syntax
#define TABLET_DISABLE_PRESSANDHOLD        0x00000001
#define TABLET_DISABLE_PENTAPFEEDBACK      0x00000008
#define TABLET_DISABLE_PENBARRELFEEDBACK   0x00000010
#define TABLET_DISABLE_TOUCHUIFORCEON      0x00000100
#define TABLET_DISABLE_TOUCHUIFORCEOFF     0x00000200
#define TABLET_DISABLE_TOUCHSWITCH         0x00008000
#define TABLET_DISABLE_FLICKS              0x00010000
#define TABLET_ENABLE_FLICKSONCONTEXT      0x00020000
#define TABLET_ENABLE_FLICKLEARNINGMODE    0x00040000
#define TABLET_DISABLE_SMOOTHSCROLLING     0x00080000
#define TABLET_DISABLE_FLICKFALLBACKKEYS   0x00100000
#define TABLET_ENABLE_MULTITOUCHDATA       0x01000000
```

> [!Note]
>
> <span data-ttu-id="bca7c-117">停用按住不放將會改善滑鼠點擊的回應速度，因為此功能會建立一個等候時間來區別這兩個作業。</span><span class="sxs-lookup"><span data-stu-id="bca7c-117">Disabling press and hold will improve responsiveness for mouse clicks because this functionality creates a wait time to distinguish between the two operations.</span></span>

 

<span data-ttu-id="bca7c-118">處理 **WM \_ 平板電腦 \_ QUERYSYSTEMGESTURESTATUS** 訊息時，請特別小心。</span><span class="sxs-lookup"><span data-stu-id="bca7c-118">Use caution when handling the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message.</span></span> <span data-ttu-id="bca7c-119">**WM \_TABLET \_ QUERYSYSTEMGESTURESTATUS** 是使用 [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) 函式來傳遞。</span><span class="sxs-lookup"><span data-stu-id="bca7c-119">**WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** is passed using the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="bca7c-120">如果您呼叫 COM 介面上的方法，該物件必須在相同的進程中。</span><span class="sxs-lookup"><span data-stu-id="bca7c-120">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="bca7c-121">如果不是，COM 會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="bca7c-121">If not, COM throws an exception.</span></span>

## <a name="examples"></a><span data-ttu-id="bca7c-122">範例</span><span class="sxs-lookup"><span data-stu-id="bca7c-122">Examples</span></span>

<span data-ttu-id="bca7c-123">下列範例示範如何使用 WM TABLET QUERYSYSTEMGESTURESTATUS 來停用區域的 \_ 筆觸 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bca7c-123">The following example shows how to disable flicks for a region using WM\_TABLET\_QUERYSYSTEMGESTURESTATUS.</span></span>


```C++
#include <windowsx.h>        

(...)        
        
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    case WM_TABLET_QUERYSYSTEMGESTURESTATUS:
        int x = GET_X_LPARAM(lParam);
        int y = GET_Y_LPARAM(lParam);
        if (x < xThreashold && y < yThreshold){
            // no flicks in the region specified by the threashold
            return TABLET_DISABLE_FLICKS;
        }
        // flicks will happen otherwise
        return 0;
}        
        
```



<span data-ttu-id="bca7c-124">下列範例顯示如何針對整個視窗停用各種筆觸功能。</span><span class="sxs-lookup"><span data-stu-id="bca7c-124">The following example shows how to disable various flicks features for an entire window.</span></span>


```C++
const DWORD dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
        
void SetTabletpenserviceProperties(HWND hWnd){
    ATOM atom = ::GlobalAddAtom(MICROSOFT_TABLETPENSERVICE_PROPERTY);    
    ::SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
    ::GlobalDeleteAtom(atom);
}        
        
```



## <a name="requirements"></a><span data-ttu-id="bca7c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="bca7c-125">Requirements</span></span>



| <span data-ttu-id="bca7c-126">需求</span><span class="sxs-lookup"><span data-stu-id="bca7c-126">Requirement</span></span> | <span data-ttu-id="bca7c-127">值</span><span class="sxs-lookup"><span data-stu-id="bca7c-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bca7c-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bca7c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bca7c-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bca7c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bca7c-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bca7c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bca7c-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bca7c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bca7c-132">標頭</span><span class="sxs-lookup"><span data-stu-id="bca7c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bca7c-133"><dt>Tpcshrd。h</dt></span><span class="sxs-lookup"><span data-stu-id="bca7c-133"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
