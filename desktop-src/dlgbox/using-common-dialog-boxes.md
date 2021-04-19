---
title: 使用通用對話方塊
description: 本節涵蓋叫用通用對話方塊的工作。
ms.assetid: ba038bc1-fb5c-4576-be80-7eae7339ba05
keywords:
- 通用對話方塊程式庫、工作
- 通用對話方塊，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a973fee7c8f7cd88abad3097edfc0349cc9118c1
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/19/2020
ms.locfileid: "106968125"
---
# <a name="using-common-dialog-boxes"></a><span data-ttu-id="c7a18-105">使用通用對話方塊</span><span class="sxs-lookup"><span data-stu-id="c7a18-105">Using Common Dialog Boxes</span></span>

<span data-ttu-id="c7a18-106">本節涵蓋的工作會叫用通用對話方塊：</span><span class="sxs-lookup"><span data-stu-id="c7a18-106">This section covers tasks that invoke common dialog boxes:</span></span>

-   [<span data-ttu-id="c7a18-107">選擇色彩</span><span class="sxs-lookup"><span data-stu-id="c7a18-107">Choosing a Color</span></span>](#choosing-a-color)
-   [<span data-ttu-id="c7a18-108">選擇字型</span><span class="sxs-lookup"><span data-stu-id="c7a18-108">Choosing a Font</span></span>](#choosing-a-font)
-   [<span data-ttu-id="c7a18-109">開啟檔案</span><span class="sxs-lookup"><span data-stu-id="c7a18-109">Opening a File</span></span>](#opening-a-file)
-   <span data-ttu-id="c7a18-110">[顯示 [列印] 對話方塊](#displaying-the-print-dialog-box)</span><span class="sxs-lookup"><span data-stu-id="c7a18-110">[Displaying the Print Dialog Box](#displaying-the-print-dialog-box)</span></span>
-   [<span data-ttu-id="c7a18-111">使用列印屬性工作表</span><span class="sxs-lookup"><span data-stu-id="c7a18-111">Using the Print Property Sheet</span></span>](#using-the-print-property-sheet)
-   [<span data-ttu-id="c7a18-112">設定列印頁面</span><span class="sxs-lookup"><span data-stu-id="c7a18-112">Setting Up the Printed Page</span></span>](#setting-up-the-printed-page)
-   [<span data-ttu-id="c7a18-113">尋找文字</span><span class="sxs-lookup"><span data-stu-id="c7a18-113">Finding Text</span></span>](#finding-text)

## <a name="choosing-a-color"></a><span data-ttu-id="c7a18-114">選擇色彩</span><span class="sxs-lookup"><span data-stu-id="c7a18-114">Choosing a Color</span></span>

<span data-ttu-id="c7a18-115">本主題說明顯示 [ **色彩** ] 對話方塊的範例程式碼，讓使用者可以選取色彩。</span><span class="sxs-lookup"><span data-stu-id="c7a18-115">This topic describes sample code that displays a **Color** dialog box so that a user can select a color.</span></span> <span data-ttu-id="c7a18-116">範例程式碼會先初始化 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) 結構，然後再呼叫 [**CHOOSECOLOR**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) 函數來顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c7a18-116">The sample code first initializes a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure, and then calls the [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) function to display the dialog box.</span></span> <span data-ttu-id="c7a18-117">如果函式傳回 **TRUE**，表示使用者已選取色彩，範例程式碼會使用選取的色彩來建立新的實心筆刷。</span><span class="sxs-lookup"><span data-stu-id="c7a18-117">If the function returns **TRUE**, indicating that the user selected a color, the sample code uses the selected color to create a new solid brush.</span></span>

<span data-ttu-id="c7a18-118">這個範例會使用 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) 結構來初始化對話方塊，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c7a18-118">This example uses the [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure to initialize the dialog box as follows:</span></span>

-   <span data-ttu-id="c7a18-119">使用值的靜態陣列指標，初始化 **lpCustColors** 成員。</span><span class="sxs-lookup"><span data-stu-id="c7a18-119">Initializes the **lpCustColors** member with a pointer to a static array of values.</span></span> <span data-ttu-id="c7a18-120">陣列中的色彩一開始是黑色，但是靜態陣列會保留使用者所建立的自訂色彩，以進行後續的 [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="c7a18-120">The colors in the array are initially black, but the static array preserves custom colors created by the user for subsequent [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) calls.</span></span>
-   <span data-ttu-id="c7a18-121">設定 **CC \_ RGBINIT** 旗標，並初始化 **rgbResult** 成員，以指定對話方塊開啟時最初選取的色彩。</span><span class="sxs-lookup"><span data-stu-id="c7a18-121">Sets the **CC\_RGBINIT** flag and initializes the **rgbResult** member to specify the color that is initially selected when the dialog box opens.</span></span> <span data-ttu-id="c7a18-122">如果未指定，則初始選項為黑色。</span><span class="sxs-lookup"><span data-stu-id="c7a18-122">If not specified, the initial selection is black.</span></span> <span data-ttu-id="c7a18-123">此範例會使用 *rgbCurrent* 靜態變數，在 [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))的呼叫之間保留選取的值。</span><span class="sxs-lookup"><span data-stu-id="c7a18-123">The example uses the *rgbCurrent* static variable to preserve the selected value between calls to [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).</span></span>
-   <span data-ttu-id="c7a18-124">設定 **CC \_ FULLOPEN** 旗標，因此一律會顯示對話方塊的自訂色彩延伸。</span><span class="sxs-lookup"><span data-stu-id="c7a18-124">Sets the **CC\_FULLOPEN** flag so the custom colors extension of the dialog box is always displayed.</span></span>


```
CHOOSECOLOR cc;                 // common dialog box structure 
static COLORREF acrCustClr[16]; // array of custom colors 
HWND hwnd;                      // owner window
HBRUSH hbrush;                  // brush handle
static DWORD rgbCurrent;        // initial color selection

// Initialize CHOOSECOLOR 
ZeroMemory(&cc, sizeof(cc));
cc.lStructSize = sizeof(cc);
cc.hwndOwner = hwnd;
cc.lpCustColors = (LPDWORD) acrCustClr;
cc.rgbResult = rgbCurrent;
cc.Flags = CC_FULLOPEN | CC_RGBINIT;
 
if (ChooseColor(&cc)==TRUE) 
{
    hbrush = CreateSolidBrush(cc.rgbResult);
    rgbCurrent = cc.rgbResult; 
}
```



## <a name="choosing-a-font"></a><span data-ttu-id="c7a18-125">選擇字型</span><span class="sxs-lookup"><span data-stu-id="c7a18-125">Choosing a Font</span></span>

<span data-ttu-id="c7a18-126">本主題說明顯示 [ **字型** ] 對話方塊的範例程式碼，讓使用者可以選擇字型的屬性。</span><span class="sxs-lookup"><span data-stu-id="c7a18-126">This topic describes sample code that displays a **Font** dialog box so that a user can choose the attributes of a font.</span></span> <span data-ttu-id="c7a18-127">範例程式碼會先初始化 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 結構，然後再呼叫 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 函數來顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c7a18-127">The sample code first initializes a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure, and then calls the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to display the dialog box.</span></span>

<span data-ttu-id="c7a18-128">此範例會設定 **CF \_ SCREENFONTS** 旗標，以指定對話方塊只顯示幕幕字型。</span><span class="sxs-lookup"><span data-stu-id="c7a18-128">This example sets the **CF\_SCREENFONTS** flag to specify that the dialog box should display only screen fonts.</span></span> <span data-ttu-id="c7a18-129">它會設定 **CF \_ 效果** 旗標，以顯示可讓使用者選取刪除線、底線和色彩選項的控制項。</span><span class="sxs-lookup"><span data-stu-id="c7a18-129">It sets the **CF\_EFFECTS** flag to display controls that allow the user to select strikeout, underline, and color options.</span></span>

<span data-ttu-id="c7a18-130">如果 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)傳回 **TRUE**，表示使用者按下 [**確定]** 按鈕， [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構就會包含描述使用者所選取之字型和字型屬性的資訊，包括 **lpLogFont** 成員所指向之 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的成員。</span><span class="sxs-lookup"><span data-stu-id="c7a18-130">If [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) returns **TRUE**, indicating that the user clicked the **OK** button, the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure contains information that describes the font and font attributes selected by the user, including the members of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure pointed to by the **lpLogFont** member.</span></span> <span data-ttu-id="c7a18-131">**RgbColors** 成員包含選取的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="c7a18-131">The **rgbColors** member contains the selected text color.</span></span> <span data-ttu-id="c7a18-132">範例程式碼會使用此資訊來設定與擁有者視窗相關聯之裝置內容的字型和文字色彩。</span><span class="sxs-lookup"><span data-stu-id="c7a18-132">The sample code uses this information to set the font and text color for the device context associated with the owner window.</span></span>


```
HWND hwnd;                // owner window
HDC hdc;                  // display device context of owner window

CHOOSEFONT cf;            // common dialog box structure
static LOGFONT lf;        // logical font structure
static DWORD rgbCurrent;  // current text color
HFONT hfont, hfontPrev;
DWORD rgbPrev;

// Initialize CHOOSEFONT
ZeroMemory(&cf, sizeof(cf));
cf.lStructSize = sizeof (cf);
cf.hwndOwner = hwnd;
cf.lpLogFont = &lf;
cf.rgbColors = rgbCurrent;
cf.Flags = CF_SCREENFONTS | CF_EFFECTS;

if (ChooseFont(&cf)==TRUE)
{
    hfont = CreateFontIndirect(cf.lpLogFont);
    hfontPrev = SelectObject(hdc, hfont);
    rgbCurrent= cf.rgbColors;
    rgbPrev = SetTextColor(hdc, rgbCurrent);
 .
 .
 .
}
```



## <a name="opening-a-file"></a><span data-ttu-id="c7a18-133">開啟檔案</span><span class="sxs-lookup"><span data-stu-id="c7a18-133">Opening a File</span></span>

> [!Note]  
> <span data-ttu-id="c7a18-134">從 Windows Vista 開始，一般的 [檔案] 對話方塊會在用來開啟檔案時由 [一般專案] 對話方塊取代。</span><span class="sxs-lookup"><span data-stu-id="c7a18-134">Starting with Windows Vista, the Common File Dialog has been superseded by the Common Item Dialog when used to open a file.</span></span> <span data-ttu-id="c7a18-135">建議您使用通用專案對話方塊 API，而不是一般檔案對話 API。</span><span class="sxs-lookup"><span data-stu-id="c7a18-135">We recommend that you use the Common Item Dialog API instead of the Common File Dialog API.</span></span> <span data-ttu-id="c7a18-136">如需詳細資訊，請參閱 [一般專案對話方塊](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c7a18-136">For more information, see [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span>

 

<span data-ttu-id="c7a18-137">本主題說明顯示 [ **開啟** ] 對話方塊的範例程式碼，讓使用者可以指定要開啟之檔案的磁片磁碟機、目錄和名稱。</span><span class="sxs-lookup"><span data-stu-id="c7a18-137">This topic describes sample code that displays an **Open** dialog box so that a user can specify the drive, directory, and name of a file to open.</span></span> <span data-ttu-id="c7a18-138">範例程式碼會先初始化 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) 結構，然後再呼叫 [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) 函數來顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c7a18-138">The sample code first initializes an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure, and then calls the [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function to display the dialog box.</span></span>

<span data-ttu-id="c7a18-139">在此範例中， **lpstrFilter** 成員是緩衝區的指標，此緩衝區會指定兩個檔案名篩選器，使用者可以選取這些篩選器來限制所顯示的檔案名。</span><span class="sxs-lookup"><span data-stu-id="c7a18-139">In this example, the **lpstrFilter** member is a pointer to a buffer that specifies two file name filters that the user can select to limit the file names that are displayed.</span></span> <span data-ttu-id="c7a18-140">緩衝區包含雙 null 結束的字串陣列，其中的每一對字串都會指定篩選。</span><span class="sxs-lookup"><span data-stu-id="c7a18-140">The buffer contains a double-null terminated array of strings in which each pair of strings specifies a filter.</span></span> <span data-ttu-id="c7a18-141">**NFilterIndex** 成員會指定在建立對話方塊時使用第一個模式。</span><span class="sxs-lookup"><span data-stu-id="c7a18-141">The **nFilterIndex** member specifies that the first pattern is used when the dialog box is created.</span></span>

<span data-ttu-id="c7a18-142">此範例會在 **旗標** 成員中設定 **OFN \_ PATHMUSTEXIST** 和 **OFN \_ FILEMUSTEXIST** 旗標。</span><span class="sxs-lookup"><span data-stu-id="c7a18-142">This example sets the **OFN\_PATHMUSTEXIST** and **OFN\_FILEMUSTEXIST** flags in the **Flags** member.</span></span> <span data-ttu-id="c7a18-143">這些旗標會在傳回之前，讓對話方塊確認使用者指定的路徑和檔案名確實存在。</span><span class="sxs-lookup"><span data-stu-id="c7a18-143">These flags cause the dialog box to verify, before returning, that the path and file name specified by the user actually exist.</span></span>

<span data-ttu-id="c7a18-144">如果使用者按一下 [**確定]** 按鈕，且指定的路徑和檔案名存在， [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)函式就會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="c7a18-144">The [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function returns **TRUE** if the user clicks the **OK** button and the specified path and file name exist.</span></span> <span data-ttu-id="c7a18-145">在此情況下， **lpstrFile** 成員所指向的緩衝區會包含路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="c7a18-145">In this case, the buffer pointed to by the **lpstrFile** member contains the path and file name.</span></span> <span data-ttu-id="c7a18-146">範例程式碼會在函式的呼叫中使用這項資訊來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="c7a18-146">The sample code uses this information in a call to the function to open the file.</span></span>

<span data-ttu-id="c7a18-147">雖然此範例不會設定 **OFN \_ explorer** 旗標，但它仍會顯示預設的 [explorer 樣式 **開啟** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c7a18-147">Although this example does not set the **OFN\_EXPLORER** flag, it still displays the default Explorer-style **Open** dialog box.</span></span> <span data-ttu-id="c7a18-148">但是，如果您想要提供攔截程式或自訂範本，而且您想要使用 Explorer 使用者介面，則必須設定 **OFN \_ Explorer** 旗標。</span><span class="sxs-lookup"><span data-stu-id="c7a18-148">However, if you want to provide a hook procedure or a custom template and you want the Explorer user interface, you must set the **OFN\_EXPLORER** flag.</span></span>

> [!Note]  
> <span data-ttu-id="c7a18-149">在 C 程式設計語言中，以引號括住的字串會以 null 終止。</span><span class="sxs-lookup"><span data-stu-id="c7a18-149">In the C programming language, a string enclosed in quotation marks is null-terminated.</span></span>

 


```
OPENFILENAME ofn;       // common dialog box structure
char szFile[260];       // buffer for file name
HWND hwnd;              // owner window
HANDLE hf;              // file handle

// Initialize OPENFILENAME
ZeroMemory(&ofn, sizeof(ofn));
ofn.lStructSize = sizeof(ofn);
ofn.hwndOwner = hwnd;
ofn.lpstrFile = szFile;
// Set lpstrFile[0] to '\0' so that GetOpenFileName does not 
// use the contents of szFile to initialize itself.
ofn.lpstrFile[0] = '\0';
ofn.nMaxFile = sizeof(szFile);
ofn.lpstrFilter = "All\0*.*\0Text\0*.TXT\0";
ofn.nFilterIndex = 1;
ofn.lpstrFileTitle = NULL;
ofn.nMaxFileTitle = 0;
ofn.lpstrInitialDir = NULL;
ofn.Flags = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;

// Display the Open dialog box. 

if (GetOpenFileName(&ofn)==TRUE) 
    hf = CreateFile(ofn.lpstrFile, 
                    GENERIC_READ,
                    0,
                    (LPSECURITY_ATTRIBUTES) NULL,
                    OPEN_EXISTING,
                    FILE_ATTRIBUTE_NORMAL,
                    (HANDLE) NULL);
```



## <a name="displaying-the-print-dialog-box"></a><span data-ttu-id="c7a18-150">顯示 [列印] 對話方塊</span><span class="sxs-lookup"><span data-stu-id="c7a18-150">Displaying the Print Dialog Box</span></span>

<span data-ttu-id="c7a18-151">本主題描述的範例程式碼會顯示 [ **列印** ] 對話方塊，讓使用者可以選取列印檔案的選項。</span><span class="sxs-lookup"><span data-stu-id="c7a18-151">This topic describes sample code that displays a **Print** dialog box so that a user can select options for printing a document.</span></span> <span data-ttu-id="c7a18-152">範例程式碼會先初始化 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構，然後再呼叫 [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函數來顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c7a18-152">The sample code first initializes a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure, and then calls the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="c7a18-153">這個範例會在 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構的 Flags 成員中設定 **PD \_ RETURNDC** 旗 **標**。</span><span class="sxs-lookup"><span data-stu-id="c7a18-153">This example sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="c7a18-154">這會導致 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 將裝置內容控制碼傳回至 **hDC** 成員中選取的印表機。</span><span class="sxs-lookup"><span data-stu-id="c7a18-154">This causes [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to return a device context handle to the selected printer in the **hDC** member.</span></span> <span data-ttu-id="c7a18-155">您可以使用此控制碼來呈現印表機上的輸出。</span><span class="sxs-lookup"><span data-stu-id="c7a18-155">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="c7a18-156">在輸入時，範例程式碼會將 **hDevMode** 和 **hDevNames** 成員設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c7a18-156">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="c7a18-157">如果函式傳回 **TRUE**，這些成員會傳回 [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) 結構的控制碼，其中包含使用者輸入以及印表機的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c7a18-157">If the function returns **TRUE**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures that contain the user input and information about the printer.</span></span> <span data-ttu-id="c7a18-158">您可以使用這份資訊來準備要傳送到所選印表機的輸出。</span><span class="sxs-lookup"><span data-stu-id="c7a18-158">You can use this information to prepare the output to be sent to the selected printer.</span></span>


```
PRINTDLG pd;
HWND hwnd;

// Initialize PRINTDLG
ZeroMemory(&pd, sizeof(pd));
pd.lStructSize = sizeof(pd);
pd.hwndOwner   = hwnd;
pd.hDevMode    = NULL;     // Don't forget to free or store hDevMode.
pd.hDevNames   = NULL;     // Don't forget to free or store hDevNames.
pd.Flags       = PD_USEDEVMODECOPIESANDCOLLATE | PD_RETURNDC; 
pd.nCopies     = 1;
pd.nFromPage   = 0xFFFF; 
pd.nToPage     = 0xFFFF; 
pd.nMinPage    = 1; 
pd.nMaxPage    = 0xFFFF; 

if (PrintDlg(&pd)==TRUE) 
{
    // GDI calls to render output. 

    // Delete DC when done.
    DeleteDC(pd.hDC);
}
```



## <a name="using-the-print-property-sheet"></a><span data-ttu-id="c7a18-159">使用列印屬性工作表</span><span class="sxs-lookup"><span data-stu-id="c7a18-159">Using the Print Property Sheet</span></span>

<span data-ttu-id="c7a18-160">本主題說明顯示 **列印** 屬性工作表的範例程式碼，讓使用者可以選取列印檔案的選項。</span><span class="sxs-lookup"><span data-stu-id="c7a18-160">This topic describes sample code that displays a **Print** property sheet so that a user can select options for printing a document.</span></span> <span data-ttu-id="c7a18-161">範例程式碼會先初始化 [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) 結構，然後再呼叫 [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函數來顯示內容表。</span><span class="sxs-lookup"><span data-stu-id="c7a18-161">The sample code first initializes a [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) structure, then calls the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the property sheet.</span></span>

<span data-ttu-id="c7a18-162">範例程式碼會在 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構的 Flags 成員中設定 **PD \_ RETURNDC** 旗 **標**。</span><span class="sxs-lookup"><span data-stu-id="c7a18-162">The sample code sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="c7a18-163">這會導致 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函式將裝置內容控制碼傳回至 **hDC** 成員中選取的印表機。</span><span class="sxs-lookup"><span data-stu-id="c7a18-163">This causes the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to return a device context handle to the selected printer in the **hDC** member.</span></span>

<span data-ttu-id="c7a18-164">在輸入時，範例程式碼會將 **hDevMode** 和 **hDevNames** 成員設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c7a18-164">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="c7a18-165">如果函式傳回 **S \_ OK**，這些成員會傳回 [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) 結構的控制碼，其中包含使用者輸入以及印表機的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c7a18-165">If the function returns **S\_OK**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="c7a18-166">您可以使用這份資訊來準備要傳送到所選印表機的輸出。</span><span class="sxs-lookup"><span data-stu-id="c7a18-166">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="c7a18-167">完成列印工作之後，範例程式碼會釋出 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)、 [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)和 [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) 緩衝區，然後呼叫 [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) 函數來刪除裝置內容。</span><span class="sxs-lookup"><span data-stu-id="c7a18-167">After the printing operation has been completed, the sample code frees the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames), and [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) buffers and calls the [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) function to delete the device context.</span></span>


```
// hWnd is the window that owns the property sheet.
HRESULT DisplayPrintPropertySheet(HWND hWnd)
{
    HRESULT hResult;
    PRINTDLGEX pdx = {0};
    LPPRINTPAGERANGE pPageRanges = NULL;

    // Allocate an array of PRINTPAGERANGE structures.
    pPageRanges = (LPPRINTPAGERANGE) GlobalAlloc(GPTR, 10 * sizeof(PRINTPAGERANGE));
    if (!pPageRanges)
        return E_OUTOFMEMORY;

    //  Initialize the PRINTDLGEX structure.
    pdx.lStructSize = sizeof(PRINTDLGEX);
    pdx.hwndOwner = hWnd;
    pdx.hDevMode = NULL;
    pdx.hDevNames = NULL;
    pdx.hDC = NULL;
    pdx.Flags = PD_RETURNDC | PD_COLLATE;
    pdx.Flags2 = 0;
    pdx.ExclusionFlags = 0;
    pdx.nPageRanges = 0;
    pdx.nMaxPageRanges = 10;
    pdx.lpPageRanges = pPageRanges;
    pdx.nMinPage = 1;
    pdx.nMaxPage = 1000;
    pdx.nCopies = 1;
    pdx.hInstance = 0;
    pdx.lpPrintTemplateName = NULL;
    pdx.lpCallback = NULL;
    pdx.nPropertyPages = 0;
    pdx.lphPropertyPages = NULL;
    pdx.nStartPage = START_PAGE_GENERAL;
    pdx.dwResultAction = 0;
    
    //  Invoke the Print property sheet.
    
    hResult = PrintDlgEx(&pdx);

    if ((hResult == S_OK) && pdx.dwResultAction == PD_RESULT_PRINT) 
    {
        // User clicked the Print button, so use the DC and other information returned in the 
        // PRINTDLGEX structure to print the document.
    }

    if (pdx.hDevMode != NULL) 
        GlobalFree(pdx.hDevMode); 
    if (pdx.hDevNames != NULL) 
        GlobalFree(pdx.hDevNames); 
    if (pdx.lpPageRanges != NULL)
        GlobalFree(pPageRanges);

    if (pdx.hDC != NULL) 
        DeleteDC(pdx.hDC);

    return hResult;
}
```



## <a name="setting-up-the-printed-page"></a><span data-ttu-id="c7a18-168">設定列印頁面</span><span class="sxs-lookup"><span data-stu-id="c7a18-168">Setting Up the Printed Page</span></span>

<span data-ttu-id="c7a18-169">本主題說明顯示 [版面 **設定** ] 對話方塊的範例程式碼，讓使用者可以選取列印頁面的屬性，例如紙張類型、紙張來源、頁面方向和頁面邊界。</span><span class="sxs-lookup"><span data-stu-id="c7a18-169">This topic describes sample code that displays a **Page Setup** dialog box so that a user can select the attributes of the printed page, such as the paper type, paper source, page orientation, and page margins.</span></span> <span data-ttu-id="c7a18-170">範例程式碼會先初始化 [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) 結構，然後再呼叫 [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函數來顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c7a18-170">The sample code first initializes a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure, and then calls the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="c7a18-171">此範例會在 **旗標** 成員中設定 **PSD \_ 邊界** 旗標，並使用 **rtMargin** 成員指定初始邊界值。</span><span class="sxs-lookup"><span data-stu-id="c7a18-171">This example sets the **PSD\_MARGINS** flag in the **Flags** member and uses the **rtMargin** member to specify the initial margin values.</span></span> <span data-ttu-id="c7a18-172">它會設定 **PSD \_ INTHOUSANDTHSOFINCHES** 旗標，以確保對話方塊會以一種英寸的萬分之一表示邊界維度。</span><span class="sxs-lookup"><span data-stu-id="c7a18-172">It sets the **PSD\_INTHOUSANDTHSOFINCHES** flag to ensure that the dialog box expresses margin dimensions in thousandths of an inch.</span></span>

<span data-ttu-id="c7a18-173">在輸入時，範例程式碼會將 **hDevMode** 和 **hDevNames** 成員設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c7a18-173">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="c7a18-174">如果函式傳回 **TRUE**，則函式會使用這些成員傳回 [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) 結構的控制碼，其中包含使用者輸入以及印表機的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c7a18-174">If the function returns **TRUE**, the function uses these members to return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="c7a18-175">您可以使用這份資訊來準備要傳送到所選印表機的輸出。</span><span class="sxs-lookup"><span data-stu-id="c7a18-175">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="c7a18-176">下列範例也會啟用 [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式，以自訂繪製範例頁面的內容。</span><span class="sxs-lookup"><span data-stu-id="c7a18-176">The following example also enables a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize drawing the contents of the sample page.</span></span>


```
PAGESETUPDLG psd;    // common dialog box structure
HWND hwnd;           // owner window

// Initialize PAGESETUPDLG
ZeroMemory(&psd, sizeof(psd));
psd.lStructSize = sizeof(psd);
psd.hwndOwner   = hwnd;
psd.hDevMode    = NULL; // Don't forget to free or store hDevMode.
psd.hDevNames   = NULL; // Don't forget to free or store hDevNames.
psd.Flags       = PSD_INTHOUSANDTHSOFINCHES | PSD_MARGINS | 
                  PSD_ENABLEPAGEPAINTHOOK; 
psd.rtMargin.top = 1000;
psd.rtMargin.left = 1250;
psd.rtMargin.right = 1250;
psd.rtMargin.bottom = 1000;
psd.lpfnPagePaintHook = PaintHook;

if (PageSetupDlg(&psd)==TRUE)
{
    // check paper size and margin values here.
}
```



<span data-ttu-id="c7a18-177">下列範例顯示在範例頁面區域中繪製邊界矩形的範例 [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式：</span><span class="sxs-lookup"><span data-stu-id="c7a18-177">The following example shows a sample [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that draws the margin rectangle in the sample page area:</span></span>


```
BOOL CALLBACK PaintHook(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    LPRECT lprc; 
    COLORREF crMargRect; 
    HDC hdc, hdcOld; 
 
    switch (uMsg) 
    { 
        // Draw the margin rectangle. 
        case WM_PSD_MARGINRECT: 
            hdc = (HDC) wParam; 
            lprc = (LPRECT) lParam; 
 
            // Get the system highlight color. 
            crMargRect = GetSysColor(COLOR_HIGHLIGHT); 
 
            // Create a dash-dot pen of the system highlight color and 
            // select it into the DC of the sample page. 
            hdcOld = SelectObject(hdc, CreatePen(PS_DASHDOT, .5, crMargRect)); 
 
            // Draw the margin rectangle. 
            Rectangle(hdc, lprc->left, lprc->top, lprc->right, lprc->bottom); 
 
            // Restore the previous pen to the DC. 
            SelectObject(hdc, hdcOld); 
            return TRUE; 
 
        default: 
            return FALSE; 
    } 
    return TRUE; 
}
```



## <a name="finding-text"></a><span data-ttu-id="c7a18-178">尋找文字</span><span class="sxs-lookup"><span data-stu-id="c7a18-178">Finding Text</span></span>

<span data-ttu-id="c7a18-179">本主題描述顯示和管理 [ **尋找** ] 對話方塊的範例程式碼，讓使用者可以指定搜尋作業的參數。</span><span class="sxs-lookup"><span data-stu-id="c7a18-179">This topic describes sample code that displays and manages a **Find** dialog box so that the user can specify the parameters of a search operation.</span></span> <span data-ttu-id="c7a18-180">此對話方塊會將訊息傳送至視窗程式，讓您可以執行搜尋作業。</span><span class="sxs-lookup"><span data-stu-id="c7a18-180">The dialog box sends messages to the window procedure so you can perform the search operation.</span></span>

<span data-ttu-id="c7a18-181">顯示和管理 **取代** 對話方塊的程式碼很類似，不同之處在于它會使用 [**replacer.replacetext**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) 函數來顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c7a18-181">The code for displaying and managing a **Replace** dialog box is similar, except that it uses the [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) function to display the dialog box.</span></span> <span data-ttu-id="c7a18-182">[ **取代** ] 對話方塊也會傳送訊息，以回應使用者按下 [ **取代** ] 和 [ **取代所有** ] 按鈕的動作。</span><span class="sxs-lookup"><span data-stu-id="c7a18-182">The **Replace** dialog box also sends messages in response to user clicks on the **Replace** and **Replace All** buttons.</span></span>

<span data-ttu-id="c7a18-183">若要使用 [ **尋找** 或 **取代** ] 對話方塊，您必須執行三個不同的工作：</span><span class="sxs-lookup"><span data-stu-id="c7a18-183">To use the **Find** or **Replace** dialog box, you must perform three separate tasks:</span></span>

1.  <span data-ttu-id="c7a18-184">取得 [**FINDMSGSTRING**](findmsgstring.md) 註冊之訊息的訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7a18-184">Get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>
2.  <span data-ttu-id="c7a18-185">顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c7a18-185">Display the dialog box.</span></span>
3.  <span data-ttu-id="c7a18-186">當對話方塊開啟時，處理 [**FINDMSGSTRING**](findmsgstring.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="c7a18-186">Process [**FINDMSGSTRING**](findmsgstring.md) messages when the dialog box is open.</span></span>

<span data-ttu-id="c7a18-187">當您初始化應用程式時，請呼叫 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) 函式來取得 [**FINDMSGSTRING**](findmsgstring.md) 已註冊訊息的訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7a18-187">When you initialize your application, call the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



<span data-ttu-id="c7a18-188">若要顯示 [ **尋找** ] 對話方塊，請先初始化 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) 結構，然後再呼叫 [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) 函數。</span><span class="sxs-lookup"><span data-stu-id="c7a18-188">To display a **Find** dialog box, first initialize a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure and then call the [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) function.</span></span> <span data-ttu-id="c7a18-189">請注意， **FINDREPLACE** 結構和搜尋字串的緩衝區應該是全域或靜態變數，使其不會在對話方塊關閉之前移出範圍。</span><span class="sxs-lookup"><span data-stu-id="c7a18-189">Note that the **FINDREPLACE** structure and the buffer for the search string should be a global or static variable so that it does not go out of scope before the dialog box closes.</span></span> <span data-ttu-id="c7a18-190">您必須設定 **hwndOwner** 成員，以指定接收已註冊之訊息的視窗。</span><span class="sxs-lookup"><span data-stu-id="c7a18-190">You must set the **hwndOwner** member to specify the window that receives the registered messages.</span></span> <span data-ttu-id="c7a18-191">建立對話方塊之後，您可以使用傳回的控制碼來移動或操作該對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c7a18-191">After you create the dialog box, you can move or manipulate it by using the returned handle.</span></span>


```
FINDREPLACE fr;       // common dialog box structure
HWND hwnd;            // owner window
CHAR szFindWhat[80];  // buffer receiving string
HWND hdlg = NULL;     // handle to Find dialog box

// Initialize FINDREPLACE
ZeroMemory(&fr, sizeof(fr));
fr.lStructSize = sizeof(fr);
fr.hwndOwner = hwnd;
fr.lpstrFindWhat = szFindWhat;
fr.wFindWhatLen = 80;
fr.Flags = 0;

hdlg = FindText(&fr);
```



<span data-ttu-id="c7a18-192">開啟對話方塊時，您的主要訊息迴圈必須包含 [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) 函數的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c7a18-192">When the dialog box is open, your main message loop must include a call to the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function.</span></span> <span data-ttu-id="c7a18-193">將控制碼傳遞至對話方塊，作為 **IsDialogMessage** 呼叫中的參數。</span><span class="sxs-lookup"><span data-stu-id="c7a18-193">Pass a handle to the dialog box as a parameter in the **IsDialogMessage** call.</span></span> <span data-ttu-id="c7a18-194">這樣可確保對話方塊正確處理鍵盤訊息。</span><span class="sxs-lookup"><span data-stu-id="c7a18-194">This ensures that the dialog box correctly processes keyboard messages.</span></span>

<span data-ttu-id="c7a18-195">若要監視從對話方塊傳送的訊息，您的視窗程式必須檢查 [**FINDMSGSTRING**](findmsgstring.md) 註冊的訊息，並處理在 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) 結構中傳遞的值，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="c7a18-195">To monitor messages sent from the dialog box, your window procedure must check for the [**FINDMSGSTRING**](findmsgstring.md) registered message and process the values passed in the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure as in the following example.</span></span>


```
LPFINDREPLACE lpfr;

if (message == uFindReplaceMsg)
{ 
    // Get pointer to FINDREPLACE structure from lParam.
    lpfr = (LPFINDREPLACE)lParam;

    // If the FR_DIALOGTERM flag is set, 
    // invalidate the handle that identifies the dialog box. 
    if (lpfr->Flags & FR_DIALOGTERM)
    { 
        hdlg = NULL; 
        return 0; 
    } 

    // If the FR_FINDNEXT flag is set, 
    // call the application-defined search routine
    // to search for the requested string. 
    if (lpfr->Flags & FR_FINDNEXT) 
    {
        SearchFile(lpfr->lpstrFindWhat,
                   (BOOL) (lpfr->Flags & FR_DOWN), 
                   (BOOL) (lpfr->Flags & FR_MATCHCASE)); 
    }

    return 0; 
}
```



 

 
