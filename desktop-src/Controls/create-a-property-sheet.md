---
title: 如何建立屬性工作表
description: 本節中的範例會建立包含兩個郵件的屬性工作表，一個用於設定試算表中儲存格的字型屬性，另一個用來設定資料格的框線屬性。
ms.assetid: 61ACF87A-938C-4487-ACEB-484FCB677C6A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15abd44f3a583afd99c5d943b9105c8734b73c1
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106988228"
---
# <a name="how-to-create-a-property-sheet"></a><span data-ttu-id="c072b-103">如何建立屬性工作表</span><span class="sxs-lookup"><span data-stu-id="c072b-103">How to Create a Property Sheet</span></span>

<span data-ttu-id="c072b-104">本節中的範例會建立包含兩個頁面的屬性工作表：一個用來設定試算表中儲存格的字型屬性，另一個則用於設定資料格的框線屬性。</span><span class="sxs-lookup"><span data-stu-id="c072b-104">The example in this section creates a property sheet that contains two pages—one for setting the font properties of a cell in a spreadsheet, and another for setting the border properties of the cell.</span></span>

<span data-ttu-id="c072b-105">此範例會藉由填滿一對 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構，並在 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構中指定傳遞給 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 函式的位址，來定義頁面。</span><span class="sxs-lookup"><span data-stu-id="c072b-105">The example defines the pages by filling a pair of [**PROPSHEETPAGE**](pss-propsheetpage.md) structures and specifying the address in the [**PROPSHEETHEADER**](pss-propsheetheader.md) structure that is passed to the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c072b-106">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="c072b-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c072b-107">技術</span><span class="sxs-lookup"><span data-stu-id="c072b-107">Technologies</span></span>

-   [<span data-ttu-id="c072b-108">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="c072b-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c072b-109">必要條件</span><span class="sxs-lookup"><span data-stu-id="c072b-109">Prerequisites</span></span>

-   <span data-ttu-id="c072b-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="c072b-110">C/C++</span></span>
-   <span data-ttu-id="c072b-111">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="c072b-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c072b-112">指示</span><span class="sxs-lookup"><span data-stu-id="c072b-112">Instructions</span></span>

### <a name="create-a-property-sheet"></a><span data-ttu-id="c072b-113">建立屬性工作表</span><span class="sxs-lookup"><span data-stu-id="c072b-113">Create a Property Sheet</span></span>

<span data-ttu-id="c072b-114">下列程式碼範例示範如何建立兩頁的屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="c072b-114">The following code example demonstrates how to create a two–page property sheet.</span></span>


```C++
// DoPropertySheet - creates a property sheet that contains two pages.
//
// hwndOwner - handle to the owner window of the property sheet.
//
// Global variables
//     g_hinst - instance handle

extern HINSTANCE g_hinst;

VOID DoPropertySheet(HWND hwndOwner)
{
    PROPSHEETPAGE psp[2];
    
    PROPSHEETHEADER psh;
    
    psp[0].dwSize      = sizeof(PROPSHEETPAGE);
    psp[0].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[0].hInstance   = g_hinst;
    psp[0].pszTemplate = MAKEINTRESOURCE(DLG_FONT);
    psp[0].pszIcon     = MAKEINTRESOURCE(IDI_FONT);
    psp[0].pfnDlgProc  = FontDialogProc;
    psp[0].pszTitle    = MAKEINTRESOURCE(IDS_FONT)
    psp[0].lParam      = 0;
    psp[0].pfnCallback = NULL;
    psp[1].dwSize      = sizeof(PROPSHEETPAGE);
    psp[1].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[1].hInstance   = g_hinst;
    psp[1].pszTemplate = MAKEINTRESOURCE(DLG_BORDER);
    psp[1].pszIcon     = MAKEINTRESOURCE(IDI_BORDER);
    psp[1].pfnDlgProc  = BorderDialogProc;
    psp[1].pszTitle    = MAKEINTRESOURCE(IDS_BORDER);
    psp[1].lParam      = 0;
    psp[1].pfnCallback = NULL;
    
    psh.dwSize      = sizeof(PROPSHEETHEADER);
    psh.dwFlags     = PSH_USEICONID | PSH_PROPSHEETPAGE;
    psh.hwndParent  = hwndOwner;
    psh.hInstance   = g_hinst;
    psh.pszIcon     = MAKEINTRESOURCE(IDI_CELL_PROPERTIES);
    psh.pszCaption  = (LPSTR) "Cell Properties";
    psh.nPages      = sizeof(psp) / sizeof(PROPSHEETPAGE);
    psh.nStartPage  = 0;
    psh.ppsp        = (LPCPROPSHEETPAGE) &psp;
    psh.pfnCallback = NULL;
    
    PropertySheet(&psh);
    
    return;
}
```



## <a name="remarks"></a><span data-ttu-id="c072b-115">備註</span><span class="sxs-lookup"><span data-stu-id="c072b-115">Remarks</span></span>

<span data-ttu-id="c072b-116">頁面的對話方塊範本、圖示和標籤會從應用程式可執行檔中包含的資源載入。</span><span class="sxs-lookup"><span data-stu-id="c072b-116">The dialog box templates, icons, and labels for the pages are loaded from the resources contained in the application's executable file.</span></span> <span data-ttu-id="c072b-117">也會從應用程式的資源載入屬性工作表的圖示。</span><span class="sxs-lookup"><span data-stu-id="c072b-117">The icon for the property sheet is also loaded from the application's resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c072b-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="c072b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c072b-119">使用屬性工作表</span><span class="sxs-lookup"><span data-stu-id="c072b-119">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

[<span data-ttu-id="c072b-120">屬性範例</span><span class="sxs-lookup"><span data-stu-id="c072b-120">Property sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/property)
</dt> </dl>

 

 




