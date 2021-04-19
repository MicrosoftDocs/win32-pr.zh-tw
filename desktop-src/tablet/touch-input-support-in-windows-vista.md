---
description: 從 Windows Vista 開始，Tablet PC 技術支援 Tablet PC 上的觸控輸入，並具備觸控功能的數位化器。 這項支援包括增強的使用者介面，可協助您在使用手指進行輸入時，鎖定目標和命令視窗。
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: Windows Vista 中的觸控輸入支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b623630c93c33b846ab1bb491fc56fe46dfe825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998511"
---
# <a name="touch-input-support-in-windows-vista"></a><span data-ttu-id="00500-104">Windows Vista 中的觸控輸入支援</span><span class="sxs-lookup"><span data-stu-id="00500-104">Touch Input Support in Windows Vista</span></span>

<span data-ttu-id="00500-105">從 Windows Vista 開始，Tablet PC 技術支援 Tablet PC 上的觸控輸入，並具備觸控功能的數位化器。</span><span class="sxs-lookup"><span data-stu-id="00500-105">Starting with Windows Vista, Tablet PC Technology has support for touch input on Tablet PC's with touch capable digitizers.</span></span> <span data-ttu-id="00500-106">這項支援包括增強的使用者介面，可協助您在使用手指進行輸入時，鎖定目標和命令視窗。</span><span class="sxs-lookup"><span data-stu-id="00500-106">This support includes an enhanced user interface to aid in targeting and commanding Windows when using a finger for input.</span></span>

## <a name="touch-digitizer-support"></a><span data-ttu-id="00500-107">Touch 數位化器支援</span><span class="sxs-lookup"><span data-stu-id="00500-107">Touch Digitizer Support</span></span>

### <a name="pen-and-touch-input-not-exclusive"></a><span data-ttu-id="00500-108">畫筆和觸控輸入非獨佔</span><span class="sxs-lookup"><span data-stu-id="00500-108">Pen and Touch Input Not Exclusive</span></span>

<span data-ttu-id="00500-109">請勿假設 [**InkCollector**](inkcollector-class.md)、 [**InkOverlay**](inkoverlay-class.md)和 [**RealTimeStylus**](realtimestylus-class.md) 應用程式中的畫筆和觸控輸入互斥。</span><span class="sxs-lookup"><span data-stu-id="00500-109">Do not assume pen and touch input are mutually exclusive in [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), and [**RealTimeStylus**](realtimestylus-class.md) applications.</span></span>

<span data-ttu-id="00500-110">在 Windows Vista 中，當系統辨識畫筆時，會忽略觸控輸入。</span><span class="sxs-lookup"><span data-stu-id="00500-110">In Windows Vista, when the system recognizes a pen it ignores touch input.</span></span> <span data-ttu-id="00500-111">也就是說，觸控筆觸會結束，且筆刷筆觸會開始。</span><span class="sxs-lookup"><span data-stu-id="00500-111">That is, the touch stroke ends and the pen stroke begins.</span></span> <span data-ttu-id="00500-112">因為未來可能會變更，所以您的程式碼不應假設畫筆和觸控輸入互斥。</span><span class="sxs-lookup"><span data-stu-id="00500-112">Because this could possibly change in the future, your code should not assume pen and touch input are mutually exclusive.</span></span>

### <a name="other-mouse-message-sources"></a><span data-ttu-id="00500-113">其他滑鼠訊息來源</span><span class="sxs-lookup"><span data-stu-id="00500-113">Other Mouse Message Sources</span></span>

<span data-ttu-id="00500-114">即使使用者只是使用手指或畫筆進行互動，也有其他的滑鼠訊息來源。</span><span class="sxs-lookup"><span data-stu-id="00500-114">There are other sources of mouse messages even when the user is only interacting using finger or pen.</span></span> <span data-ttu-id="00500-115">來源包括 touchpads，以及要讓分層視窗後方的應用程式知道滑鼠正在移至應用程式上方的移動。</span><span class="sxs-lookup"><span data-stu-id="00500-115">Sources include touchpads, as well as movement intended to let an application behind a layered window be aware that the mouse is moving above the application.</span></span>

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a><span data-ttu-id="00500-116">啟用和停用觸控輸入消費者介面</span><span class="sxs-lookup"><span data-stu-id="00500-116">Enabling and Disabling the Touch Input User Interface</span></span>

<span data-ttu-id="00500-117">視應用程式的需求而定，您可能會想要啟用或停用觸控輸入使用者介面。</span><span class="sxs-lookup"><span data-stu-id="00500-117">You may wish to enable or disable the touch input user interface depending on the requirements of your application.</span></span> <span data-ttu-id="00500-118">若要完成此動作，請在視窗程式中攔截作業系統視窗訊息，並修改 Windows 訊息。</span><span class="sxs-lookup"><span data-stu-id="00500-118">To accomplish this, intercept operating system window messages in a window procedure and modify the Windows message.</span></span> <span data-ttu-id="00500-119">覆寫應用程式中的 [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) 來攔截這些訊息。</span><span class="sxs-lookup"><span data-stu-id="00500-119">Override [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) in your application to intercept these messages.</span></span> <span data-ttu-id="00500-120">下列 C \# 程式碼顯示如何啟用和停用觸控輸入使用者介面。</span><span class="sxs-lookup"><span data-stu-id="00500-120">The following C\# pseudo-code shows how to enable and disable the touch input user interface.</span></span> <span data-ttu-id="00500-121">程式碼也會顯示如何使用相同的技術來停用按住不放手勢。</span><span class="sxs-lookup"><span data-stu-id="00500-121">The code also shows using the same technique to disable the press-and-hold gesture.</span></span> <span data-ttu-id="00500-122">此方法也適用于停用手寫筆。</span><span class="sxs-lookup"><span data-stu-id="00500-122">This method also works for disabling the stylus.</span></span>


```C++
const int WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS = 716;

const uint SYSTEM_GESTURE_STATUS_NOHOLD           = 0x00000001;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON  = 0x00000100;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF = 0x00000200;

protected override void WndProc(ref Message msg)
{
    switch (msg.Msg)
    {
        case WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS:
        {
            uint result = 0;
            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_NOHOLD;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF;
            }

            msg.Result = (IntPtr)result;
        }
        break;

        default:
            base.WndProc(ref msg);
            break;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="00500-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="00500-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00500-124">Windows Touch</span><span class="sxs-lookup"><span data-stu-id="00500-124">Windows Touch</span></span>](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
