---
description: 說明如何建立數學輸入控制項。
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: 建立數學輸入控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5084f29943395bc6781fe20598f86bdc08c6c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561519"
---
# <a name="creating-a-math-input-control"></a><span data-ttu-id="79a0b-103">建立數學輸入控制項</span><span class="sxs-lookup"><span data-stu-id="79a0b-103">Creating a Math Input Control</span></span>

<span data-ttu-id="79a0b-104">若要建立數學輸入控制項，您必須：</span><span class="sxs-lookup"><span data-stu-id="79a0b-104">To create the math input control, you must:</span></span>

-   [<span data-ttu-id="79a0b-105">包含數學輸入控制項的標頭和程式庫</span><span class="sxs-lookup"><span data-stu-id="79a0b-105">Include Headers and Libraries for the Math Input Control</span></span>](#include-headers-and-libraries-for-the-math-input-control)
-   [<span data-ttu-id="79a0b-106">宣告控制項指標並呼叫控制項指標上的 CoInitialize</span><span class="sxs-lookup"><span data-stu-id="79a0b-106">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [<span data-ttu-id="79a0b-107">顯示控制項</span><span class="sxs-lookup"><span data-stu-id="79a0b-107">Show the Control</span></span>](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a><span data-ttu-id="79a0b-108">包含數學輸入控制項的標頭和程式庫</span><span class="sxs-lookup"><span data-stu-id="79a0b-108">Include Headers and Libraries for the Math Input Control</span></span>

<span data-ttu-id="79a0b-109">下列程式碼應該放在您將使用數學輸入控制項的程式碼頂端。</span><span class="sxs-lookup"><span data-stu-id="79a0b-109">The following code should be placed at the top of your code where you will be using the math input control.</span></span>


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



<span data-ttu-id="79a0b-110">此程式碼會將數學輸入控制項的支援新增至您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="79a0b-110">This code will add support for the math input control to your application.</span></span>

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a><span data-ttu-id="79a0b-111">宣告控制項指標並呼叫控制項指標上的 CoInitialize</span><span class="sxs-lookup"><span data-stu-id="79a0b-111">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>

<span data-ttu-id="79a0b-112">在您包含控制項的標頭之後，您可以宣告控制項指標，並可在其上呼叫 CoInitialize 來建立數學輸入控制項介面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="79a0b-112">After you have included the headers for your control, you can declare the control pointer and can call CoInitialize on it to create a handle to the math input control interface.</span></span> <span data-ttu-id="79a0b-113">下列程式碼可以放置於類別中，或做為應用程式執行中的全域變數：</span><span class="sxs-lookup"><span data-stu-id="79a0b-113">The following code can be placed in a class or as a global variable in your application's implementation:</span></span>


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



<span data-ttu-id="79a0b-114">下列程式碼顯示如何在控制項指標上呼叫 CoInitialize。</span><span class="sxs-lookup"><span data-stu-id="79a0b-114">The following code shows how you can call CoInitialize on the control pointer.</span></span>


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



<span data-ttu-id="79a0b-115">呼叫控制項指標上的 CoInitialize 之後，您就會有控制項的參考，而且可以存取控制項的方法。</span><span class="sxs-lookup"><span data-stu-id="79a0b-115">After calling CoInitialize on the control pointer, you have a reference to the control and can access the control's methods.</span></span> <span data-ttu-id="79a0b-116">例如，您可以啟用一組延伸的控制項，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="79a0b-116">For example, you could enable the extended set of controls as shown in the following example.</span></span>


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a><span data-ttu-id="79a0b-117">顯示控制項</span><span class="sxs-lookup"><span data-stu-id="79a0b-117">Show the Control</span></span>

<span data-ttu-id="79a0b-118">建立控制項之後，將不會自動顯示該控制項。</span><span class="sxs-lookup"><span data-stu-id="79a0b-118">The control will not automatically appear after you create it.</span></span> <span data-ttu-id="79a0b-119">若要顯示控制項，請呼叫您在上一個步驟中建立的控制項參考上的 [**show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) 方法。</span><span class="sxs-lookup"><span data-stu-id="79a0b-119">To show the control, call the [**Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) method on the control reference that you created in the previous step.</span></span> <span data-ttu-id="79a0b-120">下列程式碼會示範如何呼叫 [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) 方法。</span><span class="sxs-lookup"><span data-stu-id="79a0b-120">The following code demonstrates how the [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) method can be called.</span></span>


```
   hr = g_spMIC->Show();
   
```



<span data-ttu-id="79a0b-121">控制項顯示之後，看起來會像下圖。</span><span class="sxs-lookup"><span data-stu-id="79a0b-121">After the control shows, it will look something like the following illustration.</span></span>

![顯示數學輸入控制項的螢幕擷取畫面](images/mic.png)

<span data-ttu-id="79a0b-123">請注意，我已啟用一組延伸的按鈕，讓您可以使用 **重做** 和 **復原** 。</span><span class="sxs-lookup"><span data-stu-id="79a0b-123">Note that I have enabled the extended set of buttons so that **Redo** and **Undo** are available.</span></span>

 

 
