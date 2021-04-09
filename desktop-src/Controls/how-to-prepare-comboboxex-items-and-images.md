---
title: 如何準備 ComboBoxEx 專案和影像
description: 本主題將示範如何將專案加入至 ComboBoxEx 控制項。
ms.assetid: 2603DFBE-9E7A-4B2F-BE33-418997D323B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7474b46e5227d91b1cc2b51462a43a0fb75d8b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842759"
---
# <a name="how-to-prepare-comboboxex-items-and-images"></a><span data-ttu-id="79d61-103">如何準備 ComboBoxEx 專案和影像</span><span class="sxs-lookup"><span data-stu-id="79d61-103">How to Prepare ComboBoxEx Items and Images</span></span>

<span data-ttu-id="79d61-104">本主題將示範如何將專案加入至 ComboBoxEx 控制項。</span><span class="sxs-lookup"><span data-stu-id="79d61-104">This topic demonstrates how to add items to a ComboBoxEx control.</span></span>

<span data-ttu-id="79d61-105">若要將專案加入至 ComboBoxEx 控制項，請先定義 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) 結構。</span><span class="sxs-lookup"><span data-stu-id="79d61-105">To add an item to a ComboBoxEx control, first define a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span> <span data-ttu-id="79d61-106">然後，設定結構的 **遮罩** 成員，以指出您希望控制項使用哪些成員。</span><span class="sxs-lookup"><span data-stu-id="79d61-106">Then, set the **mask** member of the structure to indicate which members you want the control to use.</span></span> <span data-ttu-id="79d61-107">最後，將結構的指定成員設定為所需的值，然後傳送 [**CBEM \_ INSERTITEM**](cbem-insertitem.md) 訊息，將專案加入至控制項。</span><span class="sxs-lookup"><span data-stu-id="79d61-107">Finally, set the specified members of the structure to the desired values and send the [**CBEM\_INSERTITEM**](cbem-insertitem.md) message to add the item to the control.</span></span>

<span data-ttu-id="79d61-108">下列應用程式定義函數會將15個專案加入至現有的 ComboBoxEx 控制項。</span><span class="sxs-lookup"><span data-stu-id="79d61-108">The following application-defined function adds 15 items to an existing ComboBoxEx control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="79d61-109">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="79d61-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="79d61-110">技術</span><span class="sxs-lookup"><span data-stu-id="79d61-110">Technologies</span></span>

-   [<span data-ttu-id="79d61-111">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="79d61-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="79d61-112">必要條件</span><span class="sxs-lookup"><span data-stu-id="79d61-112">Prerequisites</span></span>

-   <span data-ttu-id="79d61-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="79d61-113">C/C++</span></span>
-   <span data-ttu-id="79d61-114">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="79d61-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="79d61-115">指示</span><span class="sxs-lookup"><span data-stu-id="79d61-115">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="79d61-116">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="79d61-116">Step 1:</span></span>

<span data-ttu-id="79d61-117">若要將專案加入至 ComboBoxEx 控制項，請先定義 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) 結構。</span><span class="sxs-lookup"><span data-stu-id="79d61-117">To add an item to a ComboBoxEx control, first define a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span>


```C++
COMBOBOXEXITEM cbei;
int iCnt;


typedef struct {
    int iImage;
    int iSelectedImage;
    int iIndent;
    LPTSTR pszText;
} ITEMINFO, *PITEMINFO;

ITEMINFO IInf[ ] = {
    { 0, 3,  0, L"first"}, 
    { 1, 4,  1, L"second"},
    { 2, 5,  2, L"third"},
    { 0, 3,  0, L"fourth"},
    { 1, 4,  1, L"fifth"},
    { 2, 5,  2, L"sixth"},
    { 0, 3,  0, L"seventh"},
    { 1, 4,  1, L"eighth"},
    { 2, 5,  2, L"ninth"},
    { 0, 3,  0, L"tenth"},
    { 1, 4,  1, L"eleventh"},
    { 2, 5,  2, L"twelfth"},
    { 0, 3,  0, L"thirteenth"},
    { 1, 4,  1, L"fourteenth"},
    { 2, 5,  2, L"fifteenth"}
};
```



### <a name="step-2"></a><span data-ttu-id="79d61-118">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="79d61-118">Step 2:</span></span>

<span data-ttu-id="79d61-119">設定結構的 **遮罩** 成員，以指出您希望控制項使用哪些成員。</span><span class="sxs-lookup"><span data-stu-id="79d61-119">Set the **mask** member of the structure to indicate which members you want the control to use.</span></span> <span data-ttu-id="79d61-120">請注意， [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的 **mask** 成員包含旗標值，這些值會告訴控制項顯示每個專案的影像。</span><span class="sxs-lookup"><span data-stu-id="79d61-120">Note that the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure includes flag values that tell the control to display images for each item.</span></span>


```C++
// Set the mask common to all items.
cbei.mask = CBEIF_TEXT | CBEIF_INDENT |
            CBEIF_IMAGE| CBEIF_SELECTEDIMAGE;
```



### <a name="step-3"></a><span data-ttu-id="79d61-121">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="79d61-121">Step 3:</span></span>

<span data-ttu-id="79d61-122">將結構的指定成員設為您想要的值，然後傳送 [**CBEM \_ INSERTITEM**](cbem-insertitem.md) 訊息，將專案加入至控制項。</span><span class="sxs-lookup"><span data-stu-id="79d61-122">Set the specified members of the structure to the values you want, and then send the [**CBEM\_INSERTITEM**](cbem-insertitem.md) message to add the item to the control.</span></span>


```C++
for(iCnt=0;iCnt<MAX_ITEMS;iCnt++){
    // Initialize the COMBOBOXEXITEM struct.
    cbei.iItem          = iCnt;
    cbei.pszText        = IInf[iCnt].pszText;
    cbei.cchTextMax     = sizeof(IInf[iCnt].pszText);
    cbei.iImage         = IInf[iCnt].iImage;
    cbei.iSelectedImage = IInf[iCnt].iSelectedImage;
    cbei.iIndent        = IInf[iCnt].iIndent;

    
    // Tell the ComboBoxEx to add the item. Return FALSE if 
    // this fails.
    if(SendMessage(hwndCB,CBEM_INSERTITEM,0,(LPARAM)&cbei) == -1)
        return FALSE;
```



### <a name="step-4"></a><span data-ttu-id="79d61-123">步驟 4：</span><span class="sxs-lookup"><span data-stu-id="79d61-123">Step 4:</span></span>

<span data-ttu-id="79d61-124">將現有的影像清單指派給 ComboBoxEx 控制項，並設定控制項的大小。</span><span class="sxs-lookup"><span data-stu-id="79d61-124">Assign the existing image list to the ComboBoxEx control and set the size of control.</span></span>


```C++
// Assign the existing image list to the ComboBoxEx control 
// and return TRUE. 
// g_himl is the handle to the existing image list
SendMessage(hwndCB,CBEM_SETIMAGELIST,0,(LPARAM)g_himl);

// Set size of control to make sure it's displayed correctly now
// that the image list is set.
SetWindowPos(hwndCB,NULL,20,20,250,120,SWP_NOACTIVATE);

return TRUE; 
```



## <a name="complete-example"></a><span data-ttu-id="79d61-125">完整範例</span><span class="sxs-lookup"><span data-stu-id="79d61-125">Complete example</span></span>


```C++
// AddItems - Uses the CBEM_INSERTITEM message to add items to an
// existing ComboBoxEx control.

BOOL WINAPI AddItems(HWND hwndCB)
{
    
    //  Declare and init locals.
    COMBOBOXEXITEM cbei;
    int iCnt;
    

    typedef struct {
        int iImage;
        int iSelectedImage;
        int iIndent;
        LPTSTR pszText;
    } ITEMINFO, *PITEMINFO;

    ITEMINFO IInf[ ] = {
        { 0, 3,  0, L"first"}, 
        { 1, 4,  1, L"second"},
        { 2, 5,  2, L"third"},
        { 0, 3,  0, L"fourth"},
        { 1, 4,  1, L"fifth"},
        { 2, 5,  2, L"sixth"},
        { 0, 3,  0, L"seventh"},
        { 1, 4,  1, L"eighth"},
        { 2, 5,  2, L"ninth"},
        { 0, 3,  0, L"tenth"},
        { 1, 4,  1, L"eleventh"},
        { 2, 5,  2, L"twelfth"},
        { 0, 3,  0, L"thirteenth"},
        { 1, 4,  1, L"fourteenth"},
        { 2, 5,  2, L"fifteenth"}
    };

    // Set the mask common to all items.
    cbei.mask = CBEIF_TEXT | CBEIF_INDENT |
                CBEIF_IMAGE| CBEIF_SELECTEDIMAGE;

    for(iCnt=0;iCnt<MAX_ITEMS;iCnt++){
        // Initialize the COMBOBOXEXITEM struct.
        cbei.iItem          = iCnt;
        cbei.pszText        = IInf[iCnt].pszText;
        cbei.cchTextMax     = sizeof(IInf[iCnt].pszText);
        cbei.iImage         = IInf[iCnt].iImage;
        cbei.iSelectedImage = IInf[iCnt].iSelectedImage;
        cbei.iIndent        = IInf[iCnt].iIndent;
    
        
        // Tell the ComboBoxEx to add the item. Return FALSE if 
        // this fails.
        if(SendMessage(hwndCB,CBEM_INSERTITEM,0,(LPARAM)&cbei) == -1)
            return FALSE;
    }
    // Assign the existing image list to the ComboBoxEx control 
    // and return TRUE. 
    // g_himl is the handle to the existing image list
    SendMessage(hwndCB,CBEM_SETIMAGELIST,0,(LPARAM)g_himl);

    // Set size of control to make sure it's displayed correctly now
    // that the image list is set.
    SetWindowPos(hwndCB,NULL,20,20,250,120,SWP_NOACTIVATE);

    return TRUE; 
}
```



## <a name="related-topics"></a><span data-ttu-id="79d61-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="79d61-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79d61-127">關於 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="79d61-127">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="79d61-128">ComboBoxEx 控制項參考</span><span class="sxs-lookup"><span data-stu-id="79d61-128">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="79d61-129">使用 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="79d61-129">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="79d61-130">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="79d61-130">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 