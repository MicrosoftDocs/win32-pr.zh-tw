---
description: Tablet PC 的文字服務架構總覽。
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: '文字服務架構 (Tablet PC) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25eb3e635ae7394502ed203cb9ea31e115dc09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981676"
---
# <a name="text-services-framework-tablet-pc"></a><span data-ttu-id="fd487-103">文字服務架構 (Tablet PC) </span><span class="sxs-lookup"><span data-stu-id="fd487-103">Text Services Framework (Tablet PC)</span></span>

<span data-ttu-id="fd487-104">當已附加[PenInputPanel](/previous-versions/aa514041(v=msdn.10))物件的控制項上啟用[文字服務架構 (TSF) ](../tsf/text-services-framework.md)時，PenInputPanel 物件可以直接插入文字。</span><span class="sxs-lookup"><span data-stu-id="fd487-104">When the [Text Services Framework (TSF)](../tsf/text-services-framework.md) is enabled on a control with a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached, the PenInputPanel object can insert text directly.</span></span> <span data-ttu-id="fd487-105">如果控制項不支援文字服務架構 (TSF) ，則 PenInputPanel 物件必須使用 [SendInput 函數](/windows/win32/api/winuser/nf-winuser-sendinput) 來插入文字。</span><span class="sxs-lookup"><span data-stu-id="fd487-105">If the control does not support Text Services Framework (TSF), the PenInputPanel object must resort to using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) to insert text.</span></span>

<span data-ttu-id="fd487-106">直接插入文字的功能對於輸入東亞字元而言非常重要，因為使用 [SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) 函式可能會產生不正確的字元。</span><span class="sxs-lookup"><span data-stu-id="fd487-106">The ability to insert text directly becomes very important for those inputting East Asian characters, where using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) can produce incorrect characters.</span></span>

<span data-ttu-id="fd487-107">TSF 提供可更正辨識錯誤的介面，讓使用者能夠更正、重寫或甚至聽寫適當的文字。</span><span class="sxs-lookup"><span data-stu-id="fd487-107">TSF provides an interface for correcting recognition errors enabling the end user to correct, rewrite, or even dictate the proper text.</span></span>

<span data-ttu-id="fd487-108">藉由呼叫 [EnableTsf](/previous-versions/ms569656(v=vs.100)) 方法，並將 *enable* 參數設定為 **TRUE**，即可啟用 TSF。</span><span class="sxs-lookup"><span data-stu-id="fd487-108">TSF is enabled by calling the [EnableTsf](/previous-versions/ms569656(v=vs.100)) method with the *enable* parameter set to **TRUE**.</span></span>

<span data-ttu-id="fd487-109">\[C\#\]</span><span class="sxs-lookup"><span data-stu-id="fd487-109">\[C\#\]</span></span>


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



<span data-ttu-id="fd487-110">附加至[InkEdit](/previous-versions/ms552265(v=vs.100))控制項的[PenInputPanel](/previous-versions/aa514041(v=msdn.10))物件可提供健全的使用者經驗，因為 InkEdit 支援 TSF。</span><span class="sxs-lookup"><span data-stu-id="fd487-110">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached to a [InkEdit](/previous-versions/ms552265(v=vs.100)) control provides a robust user experience because the InkEdit supports TSF.</span></span> <span data-ttu-id="fd487-111">不過，請務必將 InkEdit 控制項上的 [InkMode](/previous-versions/ms835850(v=msdn.10)) 屬性設定為 [InkMode](/previous-versions/ms827399(v=msdn.10)) ，如 [最佳作法](best-practices.md) 主題所述。</span><span class="sxs-lookup"><span data-stu-id="fd487-111">However, be sure to set the [InkMode](/previous-versions/ms835850(v=msdn.10)) property to [Microsoft.Ink.InkMode.Ink](/previous-versions/ms827399(v=msdn.10)) on the InkEdit control as mentioned in the [Best Practices](best-practices.md) topic.</span></span>

<span data-ttu-id="fd487-112">[PenInputPanel 範例](peninputpanel-sample.md)提供啟用 TSF 的範例。</span><span class="sxs-lookup"><span data-stu-id="fd487-112">The [PenInputPanel Sample](peninputpanel-sample.md) provides an example of enabling TSF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd487-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="fd487-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd487-114">Text Services Framework (TSF)</span><span class="sxs-lookup"><span data-stu-id="fd487-114">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
