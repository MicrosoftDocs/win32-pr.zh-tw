---
title: 通用控制項的當地語系化支援
description: 本主題說明通用控制項內建的國家語言的支援。
ms.assetid: c5720198-9071-4213-8dad-50b4c015c5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccc307defa687c8640425dd781660641fe78a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932007"
---
# <a name="localization-support-for-common-controls"></a><span data-ttu-id="84ef2-103">通用控制項的當地語系化支援</span><span class="sxs-lookup"><span data-stu-id="84ef2-103">Localization Support for Common Controls</span></span>

<span data-ttu-id="84ef2-104">本主題說明通用控制項內建的國家語言的支援。</span><span class="sxs-lookup"><span data-stu-id="84ef2-104">This topic describes the support for national languages that is built into the common controls.</span></span> <span data-ttu-id="84ef2-105">內建的國家語言支援可簡化當地語系化應用程式的執行。</span><span class="sxs-lookup"><span data-stu-id="84ef2-105">The built-in national language support simplifies the implementation of localized applications.</span></span>

<span data-ttu-id="84ef2-106">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="84ef2-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="84ef2-107">指定通用控制項的語言</span><span class="sxs-lookup"><span data-stu-id="84ef2-107">Specifying a Language for the Common Controls</span></span>](#specifying-a-language-for-the-common-controls)
-   [<span data-ttu-id="84ef2-108">在對話方塊中指定控制項的語言</span><span class="sxs-lookup"><span data-stu-id="84ef2-108">Specifying a Language for Controls in a Dialog Box</span></span>](#specifying-a-language-for-controls-in-a-dialog-box)
-   [<span data-ttu-id="84ef2-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="84ef2-109">Related topics</span></span>](#related-topics)

## <a name="specifying-a-language-for-the-common-controls"></a><span data-ttu-id="84ef2-110">指定通用控制項的語言</span><span class="sxs-lookup"><span data-stu-id="84ef2-110">Specifying a Language for the Common Controls</span></span>

<span data-ttu-id="84ef2-111">如果您想要指定與系統語言不同之通用控制項的語言，請呼叫 [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage)。</span><span class="sxs-lookup"><span data-stu-id="84ef2-111">If you want to specify a language for the common controls that is different than the system language, call [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="84ef2-112">這個函式所指定的語言只會套用至呼叫函式的進程。</span><span class="sxs-lookup"><span data-stu-id="84ef2-112">The language specified by this function applies only to the process from which the function is called.</span></span>

<span data-ttu-id="84ef2-113">若要判斷通用控制項目前所使用的語言，請呼叫 [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage)。</span><span class="sxs-lookup"><span data-stu-id="84ef2-113">To determine the language currently being used by the common controls, call [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage).</span></span> <span data-ttu-id="84ef2-114">它會傳回先前呼叫 [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage)所設定的值。</span><span class="sxs-lookup"><span data-stu-id="84ef2-114">It returns the value that was set by a previous call to [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="84ef2-115">傳回的語言是針對呼叫它的進程所指定的語言。</span><span class="sxs-lookup"><span data-stu-id="84ef2-115">The language returned is the one that was specified for the process it is called from.</span></span> <span data-ttu-id="84ef2-116">如果尚未呼叫 **InitMUILanguage** ，或從另一個進程呼叫， **GetMUILanguage** 將會傳回預設值。</span><span class="sxs-lookup"><span data-stu-id="84ef2-116">If **InitMUILanguage** has not been called, or was called from another process, **GetMUILanguage** will return a default value.</span></span>

## <a name="specifying-a-language-for-controls-in-a-dialog-box"></a><span data-ttu-id="84ef2-117">在對話方塊中指定控制項的語言</span><span class="sxs-lookup"><span data-stu-id="84ef2-117">Specifying a Language for Controls in a Dialog Box</span></span>

<span data-ttu-id="84ef2-118">不同于通用控制項，預先定義的控制項（例如按鈕或編輯方塊）預設不會使用目前的系統語言。</span><span class="sxs-lookup"><span data-stu-id="84ef2-118">Unlike common controls, predefined controls such as buttons or edit boxes do not use the current system language by default.</span></span> <span data-ttu-id="84ef2-119">原生字型控制項是不可見的控制項，可在背景中運作，以允許對話方塊的預先定義控制項顯示目前的系統語言。</span><span class="sxs-lookup"><span data-stu-id="84ef2-119">The native font control is an invisible control that works in the background to allow a dialog box's predefined controls to display the current system language.</span></span>

<span data-ttu-id="84ef2-120">若要使用原生字型控制項，請遵循此程式。</span><span class="sxs-lookup"><span data-stu-id="84ef2-120">To use the native font control, follow this procedure.</span></span>

1.  <span data-ttu-id="84ef2-121">藉由呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)來初始化原生字型控制項。</span><span class="sxs-lookup"><span data-stu-id="84ef2-121">Initialize the native font control by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="84ef2-122">將 *lpInitCtrls* 所指向之 [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)結構的 **DWICC** 成員設定為 [ICC \_ NATIVEFNTCTL \_ 類別]。</span><span class="sxs-lookup"><span data-stu-id="84ef2-122">Set the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure pointed to by *lpInitCtrls* to ICC\_NATIVEFNTCTL\_CLASS.</span></span>
2.  <span data-ttu-id="84ef2-123">將控制項新增至對話方塊的資源腳本。</span><span class="sxs-lookup"><span data-stu-id="84ef2-123">Add the control to the resource script for the dialog box.</span></span> <span data-ttu-id="84ef2-124">設定下列一或多個樣式旗標，以指定將會影響哪些控制項。</span><span class="sxs-lookup"><span data-stu-id="84ef2-124">Set one or more of the following style flags to specify which controls will be affected.</span></span> 

    | <span data-ttu-id="84ef2-125">旗標</span><span class="sxs-lookup"><span data-stu-id="84ef2-125">Flag</span></span>              | <span data-ttu-id="84ef2-126">適用於</span><span class="sxs-lookup"><span data-stu-id="84ef2-126">Applies to</span></span>                                                                                                                                                                                                                                                       |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="84ef2-127">NFS \_ 編輯</span><span class="sxs-lookup"><span data-stu-id="84ef2-127">NFS\_EDIT</span></span>         | <span data-ttu-id="84ef2-128">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="84ef2-128">Edit controls</span></span>                                                                                                                                                                                                                                                    |
    | <span data-ttu-id="84ef2-129">NFS \_ 靜態</span><span class="sxs-lookup"><span data-stu-id="84ef2-129">NFS\_STATIC</span></span>       | <span data-ttu-id="84ef2-130">靜態控制項</span><span class="sxs-lookup"><span data-stu-id="84ef2-130">Static controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="84ef2-131">NFS \_ LISTCOMBO</span><span class="sxs-lookup"><span data-stu-id="84ef2-131">NFS\_LISTCOMBO</span></span>    | <span data-ttu-id="84ef2-132">清單、ComboBox、清單視圖和 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="84ef2-132">List, ComboBox, List-View, and ComboBoxEx controls</span></span>                                                                                                                                                                                                               |
    | <span data-ttu-id="84ef2-133">NFS \_ 按鈕</span><span class="sxs-lookup"><span data-stu-id="84ef2-133">NFS\_BUTTON</span></span>       | <span data-ttu-id="84ef2-134">按鈕控制項</span><span class="sxs-lookup"><span data-stu-id="84ef2-134">Button controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="84ef2-135">NFS \_ 全部</span><span class="sxs-lookup"><span data-stu-id="84ef2-135">NFS\_ALL</span></span>          | <span data-ttu-id="84ef2-136">所有控制項</span><span class="sxs-lookup"><span data-stu-id="84ef2-136">All controls</span></span>                                                                                                                                                                                                                                                     |
    | <span data-ttu-id="84ef2-137">NFS \_ USEFONTASSOC</span><span class="sxs-lookup"><span data-stu-id="84ef2-137">NFS\_USEFONTASSOC</span></span> | <span data-ttu-id="84ef2-138">東亞平臺。</span><span class="sxs-lookup"><span data-stu-id="84ef2-138">East Asian platform.</span></span> <span data-ttu-id="84ef2-139">控制項使用字型關聯功能，而不是切換至原生字型。</span><span class="sxs-lookup"><span data-stu-id="84ef2-139">The control uses the font association feature instead of switching to the native font.</span></span> <span data-ttu-id="84ef2-140">所有其他平臺會忽略它。</span><span class="sxs-lookup"><span data-stu-id="84ef2-140">All other platforms ignore it.</span></span> <span data-ttu-id="84ef2-141">Windows Vista 的這項功能已被取代，comctl v6 則不支援。</span><span class="sxs-lookup"><span data-stu-id="84ef2-141">This is deprecated for Windows Vista, and is not supported in comctl v6.</span></span> <span data-ttu-id="84ef2-142">基於舊版原因，這存在於 comctl v5 中。</span><span class="sxs-lookup"><span data-stu-id="84ef2-142">This exists in comctl v5 for legacy reasons.</span></span> |

    

     

<span data-ttu-id="84ef2-143">下列範例說明如何將原生字型控制項新增至資源腳本。</span><span class="sxs-lookup"><span data-stu-id="84ef2-143">The following example illustrates how to add a native font control to a resource script.</span></span> <span data-ttu-id="84ef2-144">它會讓對話方塊的編輯、列出和下拉式方塊控制項使用目前的系統語言來顯示文字。</span><span class="sxs-lookup"><span data-stu-id="84ef2-144">It causes the dialog box's edit, list, and combo box controls to display text using the current system language.</span></span>


```
CONTROL    "",-1,"NativeFontCtl",NFS_EDIT|NFS_LISTCOMBO,0,0,0,0
```



## <a name="related-topics"></a><span data-ttu-id="84ef2-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="84ef2-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84ef2-146">關於通用控制項</span><span class="sxs-lookup"><span data-stu-id="84ef2-146">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 




