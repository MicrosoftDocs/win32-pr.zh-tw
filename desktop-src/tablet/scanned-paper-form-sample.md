---
description: 在此 C \# 範例中，檔表單已掃描為可移植網狀圖形 (PNG) 檔案，並在執行時間指定為 InkPicture 控制項的背景影像。 此範例會使用訊息方塊來顯示手寫辨識結果。
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: 掃描的紙張表單範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d60e1d62a4e023ba38e9a1fd2c4890288a542d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984602"
---
# <a name="scanned-paper-form-sample"></a><span data-ttu-id="c5c98-104">掃描的紙張表單範例</span><span class="sxs-lookup"><span data-stu-id="c5c98-104">Scanned Paper Form Sample</span></span>

<span data-ttu-id="c5c98-105">在此 C \# 範例中，檔表單已掃描為可移植網狀圖形 (PNG) 檔案，並在執行時間指定為 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項的背景影像。</span><span class="sxs-lookup"><span data-stu-id="c5c98-105">In this C\# sample, a paper form has been scanned as a Portable Network Graphics (PNG) file and specified as the background image at run time for a [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span> <span data-ttu-id="c5c98-106">此範例會使用訊息方塊來顯示手寫辨識結果。</span><span class="sxs-lookup"><span data-stu-id="c5c98-106">The sample uses a message box to display handwriting recognition results.</span></span>

<span data-ttu-id="c5c98-107">此範例包含可延伸標記語言 (XML)  (XML) 檔，Formdata.xml。</span><span class="sxs-lookup"><span data-stu-id="c5c98-107">The sample includes an Extensible Markup Language (XML) file, Formdata.xml.</span></span> <span data-ttu-id="c5c98-108">XML 檔案包含 PNG 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5c98-108">The XML file contains the name of the PNG file.</span></span> <span data-ttu-id="c5c98-109">它也包含可 `FieldInfo` 在表單上定義矩形區域的專案，使用者可以在表單上輸入筆跡。</span><span class="sxs-lookup"><span data-stu-id="c5c98-109">It also contains `FieldInfo` elements that define rectangular regions on the form where a user can enter ink.</span></span> <span data-ttu-id="c5c98-110">`FieldInfo`下列範例會顯示元素中的資訊：</span><span class="sxs-lookup"><span data-stu-id="c5c98-110">The information in the `FieldInfo` element is shown in the following example:</span></span>


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



<span data-ttu-id="c5c98-111">左、上、右和下的元素是每個欄位的圖元座標定義。</span><span class="sxs-lookup"><span data-stu-id="c5c98-111">The Left, Top, Right, and Bottom elements are definitions of pixel coordinates for each field.</span></span>

<span data-ttu-id="c5c98-112">此範例會使用 Formdata.xml 中包含的資料來初始化新的 [資料集](/dotnet/api/system.data.dataset?view=netcore-3.1) ：</span><span class="sxs-lookup"><span data-stu-id="c5c98-112">The sample initializes a new [DataSet](/dotnet/api/system.data.dataset?view=netcore-3.1) with the data contained in Formdata.xml:</span></span>


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



<span data-ttu-id="c5c98-113">Formdata.xml 中指定的表單影像會以 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項的背景載入：</span><span class="sxs-lookup"><span data-stu-id="c5c98-113">The form image specified in Formdata.xml is loaded as the background of the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



<span data-ttu-id="c5c98-114">然後， [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項會啟用筆墨收集：</span><span class="sxs-lookup"><span data-stu-id="c5c98-114">Ink collection is then enabled for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a><span data-ttu-id="c5c98-115">功能表事件處理常式</span><span class="sxs-lookup"><span data-stu-id="c5c98-115">Menu Event Handlers</span></span>

<span data-ttu-id="c5c98-116">應用程式包括在表單頂端顯示之所有功能表的 click 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="c5c98-116">The application includes click event handlers for all of the menus displayed along the top of the form.</span></span>

### <a name="recognize-menu-item"></a><span data-ttu-id="c5c98-117">辨識功能表項目</span><span class="sxs-lookup"><span data-stu-id="c5c98-117">Recognize Menu Item</span></span>

<span data-ttu-id="c5c98-118">辨識功能表的 click 事件處理常式會停用控制項的筆墨集合，並檢查手寫辨識器。</span><span class="sxs-lookup"><span data-stu-id="c5c98-118">The Recognize menu click event handler disables ink collection for the control and checks for a handwriting recognizer.</span></span> <span data-ttu-id="c5c98-119">如果未安裝辨識器，則會顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c5c98-119">If no recognizer is installed, a dialog box is displayed.</span></span> <span data-ttu-id="c5c98-120">然後，使用者必須按一下 [筆跡] 或 [畫筆] 功能表選項，以重新啟用筆墨輸入的控制項。</span><span class="sxs-lookup"><span data-stu-id="c5c98-120">A user must then click the Ink or Pen menu option to re-enable the control for ink input.</span></span>

<span data-ttu-id="c5c98-121">如果已安裝辨識器，則函式會抓取為 `Recognize` 每個表單欄位指定圖元座標的 XML 資料。</span><span class="sxs-lookup"><span data-stu-id="c5c98-121">If a recognizer is installed, the `Recognize` function retrieves the XML data that specifies pixel coordinates for each form field.</span></span> <span data-ttu-id="c5c98-122">座標會轉換成筆墨空間座標，並為每個表單欄位定義一個矩形。</span><span class="sxs-lookup"><span data-stu-id="c5c98-122">The coordinates are converted to ink space coordinates, and a rectangle is defined for each form field.</span></span> <span data-ttu-id="c5c98-123">定義矩形之後，此函式會尋找在每個矩形內相交和落在每個矩形內的筆觸。</span><span class="sxs-lookup"><span data-stu-id="c5c98-123">After rectangles are defined, the function finds the strokes that intersect and lie within each rectangle.</span></span> <span data-ttu-id="c5c98-124">最後，它會執行筆墨的辨識，並在訊息方塊中顯示結果。</span><span class="sxs-lookup"><span data-stu-id="c5c98-124">Finally, it performs recognition on the ink and displays the results in a message box.</span></span>

### <a name="ink-menu-item"></a><span data-ttu-id="c5c98-125">筆墨功能表項目</span><span class="sxs-lookup"><span data-stu-id="c5c98-125">Ink Menu Item</span></span>

<span data-ttu-id="c5c98-126">筆墨功能表的 click 事件處理常式會啟用 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項。</span><span class="sxs-lookup"><span data-stu-id="c5c98-126">The Ink menu click event handler enables the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span>

### <a name="pen-menu-item"></a><span data-ttu-id="c5c98-127">畫筆功能表項目</span><span class="sxs-lookup"><span data-stu-id="c5c98-127">Pen Menu Item</span></span>

<span data-ttu-id="c5c98-128">畫筆功能表的 click 事件處理常式會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="c5c98-128">The Pen menu click event handler performs the following tasks:</span></span>

-   <span data-ttu-id="c5c98-129">在變更[system.windows.controls.inkcanvas.editingmode](/previous-versions/ms582189(v=vs.100))屬性) 之前，停用[InkPicture](/previous-versions/aa514604(v=msdn.10))控制項的筆墨集合 (這是必要的。</span><span class="sxs-lookup"><span data-stu-id="c5c98-129">Disables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control (which is necessary before changing the [EditingMode](/previous-versions/ms582189(v=vs.100)) property).</span></span>
-   <span data-ttu-id="c5c98-130">設定 [system.windows.controls.inkcanvas.editingmode](/previous-versions/ms582189(v=vs.100)) 屬性以收集筆跡。</span><span class="sxs-lookup"><span data-stu-id="c5c98-130">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to collect ink.</span></span>
-   <span data-ttu-id="c5c98-131">重新啟用 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項的筆墨集合，並切換畫筆、選取和橡皮擦功能表以指出現用模式。</span><span class="sxs-lookup"><span data-stu-id="c5c98-131">Re-enables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control and toggles the Pen, Select, and Eraser menus to indicate the active mode.</span></span>

### <a name="edit-menu-item"></a><span data-ttu-id="c5c98-132">編輯功能表項目</span><span class="sxs-lookup"><span data-stu-id="c5c98-132">Edit Menu Item</span></span>

<span data-ttu-id="c5c98-133">[編輯] 功能表 click 事件處理常式類似于 [畫筆] 功能表事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="c5c98-133">The Edit menu click event handler is similar to the Pen menu event handler.</span></span> <span data-ttu-id="c5c98-134">它會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="c5c98-134">It performs the following tasks:</span></span>

-   <span data-ttu-id="c5c98-135">停用筆墨收集。</span><span class="sxs-lookup"><span data-stu-id="c5c98-135">Disables ink collection.</span></span>
-   <span data-ttu-id="c5c98-136">將 [system.windows.controls.inkcanvas.editingmode](/previous-versions/ms582189(v=vs.100)) 屬性設定為 **Select**，讓使用者可以執行筆墨選取。</span><span class="sxs-lookup"><span data-stu-id="c5c98-136">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to **Select**, which enables the user to perform ink selection.</span></span>
-   <span data-ttu-id="c5c98-137">重新啟用筆墨集合，並切換畫筆、編輯和橡皮擦功能表以表示現用模式。</span><span class="sxs-lookup"><span data-stu-id="c5c98-137">Re-enables ink collection and toggles the Pen, Edit, and Eraser menus to indicate the active mode.</span></span>

### <a name="eraser-menu-item"></a><span data-ttu-id="c5c98-138">橡皮擦功能表項目</span><span class="sxs-lookup"><span data-stu-id="c5c98-138">Eraser Menu Item</span></span>

<span data-ttu-id="c5c98-139">橡皮擦功能表的 click 事件處理常式會將 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項 [System.windows.controls.inkcanvas.editingmode](/previous-versions/ms582189(v=vs.100)) 設定為 **Delete**，讓使用者可以清除筆跡。</span><span class="sxs-lookup"><span data-stu-id="c5c98-139">The Eraser menu click event handler sets the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control [EditingMode](/previous-versions/ms582189(v=vs.100)) to **Delete**, which enables a user to erase ink.</span></span> <span data-ttu-id="c5c98-140">它也會切換 [畫筆]、[編輯] 和 [橡皮擦] 功能表項目。</span><span class="sxs-lookup"><span data-stu-id="c5c98-140">It also toggles the Pen, Edit, and Eraser menu items.</span></span>

### <a name="clear-menu-item"></a><span data-ttu-id="c5c98-141">清除功能表項目</span><span class="sxs-lookup"><span data-stu-id="c5c98-141">Clear Menu Item</span></span>

<span data-ttu-id="c5c98-142">清除功能表的 click 事件處理常式會刪除[InkPicture](/previous-versions/aa514604(v=msdn.10))控制項目前的[筆劃](/previous-versions/ms552701(v=vs.100))集合，藉此清除表單上的所有筆墨。</span><span class="sxs-lookup"><span data-stu-id="c5c98-142">The Clear menu click event handler deletes the current [Strokes](/previous-versions/ms552701(v=vs.100)) collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control, thereby erasing all of the ink on the form.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="c5c98-143">關閉表單</span><span class="sxs-lookup"><span data-stu-id="c5c98-143">Closing the Form</span></span>

<span data-ttu-id="c5c98-144">在 Windows Form 設計工具產生的程式碼中， [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項會在表單初始化時加入表單的元件清單中。</span><span class="sxs-lookup"><span data-stu-id="c5c98-144">In the Windows Form Designer generated code, the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="c5c98-145">當表單關閉時，會以表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法處置 InkPicture 控制項，以及表單的其他元件。</span><span class="sxs-lookup"><span data-stu-id="c5c98-145">When the form closes, the InkPicture control is disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5c98-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5c98-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5c98-147">InkEdit 控制項</span><span class="sxs-lookup"><span data-stu-id="c5c98-147">InkEdit Control</span></span>](inkedit-control.md)
</dt> <dt>

[<span data-ttu-id="c5c98-148">InkPicture 控制項</span><span class="sxs-lookup"><span data-stu-id="c5c98-148">InkPicture Control</span></span>](inkpicture-control.md)
</dt> </dl>

 

 
