---
description: 此範例會藉由整合 PenInputPanel 物件，以自動宣告表單範例為基礎。 此範例位於 \# AutoClaims 資料夾的 C PIPanel 目錄中。
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: PenInputPanel 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d60f33ff3f61e1a2930841e5fd3d3ce3f9fc5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979368"
---
# <a name="peninputpanel-sample"></a><span data-ttu-id="eb978-104">PenInputPanel 範例</span><span class="sxs-lookup"><span data-stu-id="eb978-104">PenInputPanel Sample</span></span>

<span data-ttu-id="eb978-105">此範例會藉由整合 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件，以自動宣告表單範例為基礎。</span><span class="sxs-lookup"><span data-stu-id="eb978-105">This sample builds on the Auto Claims Form sample by integrating the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="eb978-106">此範例位於 \# AutoClaims 資料夾的 C PIPanel 目錄中。</span><span class="sxs-lookup"><span data-stu-id="eb978-106">The sample is in the C\# PIPanel directory in the AutoClaims folder.</span></span>

> [!Note]  
> <span data-ttu-id="eb978-107">此範例會要求您的系統配備了畫筆裝置。</span><span class="sxs-lookup"><span data-stu-id="eb978-107">This sample requires that your system is equipped with a pen device.</span></span> <span data-ttu-id="eb978-108">如果您只是使用滑鼠 (或其他非人力介面裝置 (隱藏) 指向裝置) [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 不會出現。</span><span class="sxs-lookup"><span data-stu-id="eb978-108">If you are using just a mouse (or other non-human interface device (HID) pointing device) the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) does not appear.</span></span>

 

<span data-ttu-id="eb978-109">如需自動宣告表單範例的詳細資訊，請參閱 [自動宣告表單範例](auto-claims-form-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="eb978-109">For more information about the Auto Claims Form sample, see [Auto Claims Form Sample](auto-claims-form-sample.md).</span></span> <span data-ttu-id="eb978-110">如需 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件的詳細資訊，請參閱 [使用 PenInputPanel 類別設計輸入面板](programming-the-input-panel-using-the-peninputpanel-class.md)。</span><span class="sxs-lookup"><span data-stu-id="eb978-110">For more information about the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, see [Programming the Input Panel Using the PenInputPanel Class](programming-the-input-panel-using-the-peninputpanel-class.md).</span></span>

<span data-ttu-id="eb978-111">在此範例中，「自動宣告」表單包含五個欄位，要求使用者將相關資訊放入與該宣告相關的資訊：原則號碼、保險名稱、年份、製作和汽車型號。</span><span class="sxs-lookup"><span data-stu-id="eb978-111">In the sample, the Auto Claims Form contains five fields into which the user is asked to put information relevant to the claim: policy number, insured name, the year, make, and model of the car.</span></span> <span data-ttu-id="eb978-112">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))物件會附加至每個輸入欄位，以提供使用畫筆輸入值的簡單方法。</span><span class="sxs-lookup"><span data-stu-id="eb978-112">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is attached to each input field to provide an easy means for entering values with a pen.</span></span>

<span data-ttu-id="eb978-113">有兩種技巧可將 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件附加至表單上的輸入欄位。</span><span class="sxs-lookup"><span data-stu-id="eb978-113">There are two techniques for attaching a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to the input fields on your form.</span></span> <span data-ttu-id="eb978-114">第一個技巧是在設計階段將物件的個別實例指派給每個輸入欄位。</span><span class="sxs-lookup"><span data-stu-id="eb978-114">The first technique is to assign a separate instance of the object to each input field at design time.</span></span> <span data-ttu-id="eb978-115">第二種方式是建立物件的單一實例，然後在執行時間將該物件實例附加至接收焦點的欄位。</span><span class="sxs-lookup"><span data-stu-id="eb978-115">The second is to create a single instance of the object and then attach that object instance at run time to a field when it receives focus.</span></span> <span data-ttu-id="eb978-116">這個範例會示範這兩種技術。</span><span class="sxs-lookup"><span data-stu-id="eb978-116">This sample demonstrates both techniques.</span></span>

<span data-ttu-id="eb978-117">決定要使用的技巧有一些取捨。</span><span class="sxs-lookup"><span data-stu-id="eb978-117">There are tradeoffs involved in deciding which technique to use.</span></span> <span data-ttu-id="eb978-118">在載入表單時，為每個表單欄位建立物件的唯一實例，需要更多的記憶體。</span><span class="sxs-lookup"><span data-stu-id="eb978-118">Creating a unique instance of the object for each form field requires slightly more memory when the form is loaded.</span></span> <span data-ttu-id="eb978-119">但是，它可以節省在執行時間將單一實例指派給目前欄位的欄位處理焦點事件。</span><span class="sxs-lookup"><span data-stu-id="eb978-119">However, it saves having to handle focus events for the fields to assign a single instance to the current field at run time.</span></span>

<span data-ttu-id="eb978-120">由於 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件只在平板電腦上受到支援，因此此範例會在例外狀況處理區塊內建立 PenInputPanel 物件。</span><span class="sxs-lookup"><span data-stu-id="eb978-120">Because the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is supported only on a Tablet PC, the sample creates the PenInputPanel objects within an exception-handling block.</span></span>

## <a name="one-object-per-field"></a><span data-ttu-id="eb978-121">每個欄位一個物件</span><span class="sxs-lookup"><span data-stu-id="eb978-121">One Object per Field</span></span>

<span data-ttu-id="eb978-122">此範例會示範第一種技術 (每個欄位) 一個 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件，方法是指派原則編號的輸入欄位 (`inkEdPolicyNumber`) 和保險名稱 (`inkEdName`) PenInputPanel 物件的唯一實例。</span><span class="sxs-lookup"><span data-stu-id="eb978-122">The sample demonstrates the first technique (one [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object per field) by assigning the input fields for policy number (`inkEdPolicyNumber`) and insured name (`inkEdName`) a unique instance of the PenInputPanel object.</span></span> <span data-ttu-id="eb978-123">PenInputPanel 物件的多載函式可以採用輸入控制項的名稱做為引數，進而使控制項產生關聯。</span><span class="sxs-lookup"><span data-stu-id="eb978-123">An overloaded constructor for the PenInputPanel object can take the name of the input control as an argument, thus associating the controls.</span></span> <span data-ttu-id="eb978-124">表單的 [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) 事件處理常式中的下列幾行顯示如下：</span><span class="sxs-lookup"><span data-stu-id="eb978-124">The following lines from the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler shows this:</span></span>


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a><span data-ttu-id="eb978-125">每個表單一個物件</span><span class="sxs-lookup"><span data-stu-id="eb978-125">One Object per Form</span></span>

<span data-ttu-id="eb978-126">第二個技術也會顯示在範例中： [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件的單一實例，在 `pipShared` Year、Make 和 Model 輸入欄位之間共用。</span><span class="sxs-lookup"><span data-stu-id="eb978-126">The second technique is also shown in the sample: a single instance of a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, `pipShared`, is shared between the Year, Make, and Model input fields.</span></span> <span data-ttu-id="eb978-127">共用物件是使用預設的函式建立的。</span><span class="sxs-lookup"><span data-stu-id="eb978-127">The shared object is created by using the default constructor.</span></span>


```C++
pipShared = new PenInputPanel();
```



<span data-ttu-id="eb978-128">使用這項技術需要您的表單只有 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件的單一實例。</span><span class="sxs-lookup"><span data-stu-id="eb978-128">Using this technique requires that your form have only a single instance of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="eb978-129">這樣可以節省記憶體，但是當輸入欄位收到焦點時，您必須加入程式碼來處理事件。</span><span class="sxs-lookup"><span data-stu-id="eb978-129">This saves memory, but you must add code to handle the event when an input field receives focus.</span></span> <span data-ttu-id="eb978-130">當使用 PenInputPanel 物件之共用實例的控制項取得焦點時，請將 PenInputPanel 物件的 [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) 屬性設定為該控制項。</span><span class="sxs-lookup"><span data-stu-id="eb978-130">When a control that uses a shared instance of a PenInputPanel object gets focus, set the PenInputPanel object's [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) property to that control.</span></span> <span data-ttu-id="eb978-131">下列程式碼顯示 Year、Make 和 Model 欄位之事件的事件處理常式 `Enter` 。</span><span class="sxs-lookup"><span data-stu-id="eb978-131">The following code shows an event handler for the Year, Make, and Model fields' `Enter` events.</span></span>


```C++
private void inkEdYear_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Year field
    pipShared.AttachedEditControl = inkEdYear;

    // set the NUMBER factoid to bias recognition for numbers
    pipShared.Factoid = "NUMBER";

    // Enable correction UI on the inkEdYear field
    pipShared.EnableTsf(true);
}

private void inkEdMake_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Make field
    pipShared.AttachedEditControl = inkEdMake;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdMake field
    pipShared.EnableTsf(true);
}
private void inkEdModel_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Model field
    pipShared.AttachedEditControl = inkEdModel;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdModel field
    pipShared.EnableTsf(true);
}
```



<span data-ttu-id="eb978-132">當焦點變更至新的控制項時，請務必設定任何需要設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="eb978-132">Be sure to set any properties that need to be set when focus changes to a new control.</span></span> <span data-ttu-id="eb978-133">例如，在先前的事件處理常式中，會適當地設定 [模擬](/previous-versions/ms571978(v=vs.100)) 程式屬性。</span><span class="sxs-lookup"><span data-stu-id="eb978-133">In the previous event handlers, for example, the [Factoid](/previous-versions/ms571978(v=vs.100)) property is set as appropriate.</span></span>

## <a name="usability-considerations"></a><span data-ttu-id="eb978-134">可用性考慮</span><span class="sxs-lookup"><span data-stu-id="eb978-134">Usability Considerations</span></span>

<span data-ttu-id="eb978-135">在您的應用程式中使用 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件時，請記住下列可用性考慮。</span><span class="sxs-lookup"><span data-stu-id="eb978-135">Keep the following usability considerations in mind when using the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object in your application.</span></span>

### <a name="positioning-the-peninputpanel"></a><span data-ttu-id="eb978-136">定位 PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="eb978-136">Positioning the PenInputPanel</span></span>

<span data-ttu-id="eb978-137">因為欄位在此範例中的表單上會垂直配置，所以每個輸入控制項的 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 使用者介面都會放在輸入控制項的右邊，使其更容易使用。</span><span class="sxs-lookup"><span data-stu-id="eb978-137">Because the fields are laid out vertically on the form in this sample, the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) user interface for each input control is positioned slightly to the right of the input control to make it easier to use.</span></span> <span data-ttu-id="eb978-138">這可防止 PenInputPanel 涵蓋下一個編輯方塊，讓您更輕鬆地以下一個編輯方塊為目標。</span><span class="sxs-lookup"><span data-stu-id="eb978-138">This prevents the PenInputPanel from covering up the next edit box, making it easier to target the next edit box.</span></span>


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a><span data-ttu-id="eb978-139">選取要顯示的輸入面板</span><span class="sxs-lookup"><span data-stu-id="eb978-139">Selecting Input Panel to Display</span></span>

<span data-ttu-id="eb978-140">由於原則號碼通常是數位、字母和其他字元的組合，因此很容易辨識錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb978-140">Because policy numbers are often combinations of numbers, letters, and other characters, they can be prone to recognition errors.</span></span> <span data-ttu-id="eb978-141">因此，此範例會將 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件所顯示的預設面板，設定為附加至 [原則號碼] 欄位時的鍵盤。</span><span class="sxs-lookup"><span data-stu-id="eb978-141">Therefore, the sample sets the default panel displayed by the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to be the keyboard when it is attached to the policy number field.</span></span>


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



<span data-ttu-id="eb978-142">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))物件的預設行為是使用使用者最後選取的面板。</span><span class="sxs-lookup"><span data-stu-id="eb978-142">The default behavior of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is to use the panel the user selected last.</span></span>

### <a name="text-services-framework-correction-user-interface"></a><span data-ttu-id="eb978-143">文字服務架構更正消費者介面</span><span class="sxs-lookup"><span data-stu-id="eb978-143">Text Services Framework Correction User Interface</span></span>

<span data-ttu-id="eb978-144">在此範例中，所有的輸入欄位都是 [InkEdit](/previous-versions/ms552265(v=vs.100)) 控制項。</span><span class="sxs-lookup"><span data-stu-id="eb978-144">In this sample all of the input fields are [InkEdit](/previous-versions/ms552265(v=vs.100)) controls.</span></span> <span data-ttu-id="eb978-145">這是很重要的，因為 InkEdit 控制項內建支援 [文字服務架構](../tsf/text-services-framework.md) (TSF) ，因此能夠支援從 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件接收之輸入的就地更正使用者介面。</span><span class="sxs-lookup"><span data-stu-id="eb978-145">This is significant because the InkEdit control has built-in support for the [Text Services Framework](../tsf/text-services-framework.md) (TSF) and is thus capable of supporting the in-place correction user interface for input received from the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span>

<span data-ttu-id="eb978-146">[EnableTsf](/previous-versions/ms569656(v=vs.100))的預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="eb978-146">The default value for [EnableTsf](/previous-versions/ms569656(v=vs.100)) is **TRUE**.</span></span> <span data-ttu-id="eb978-147">這會導致 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件嘗試啟動附加控制項上的文字服務架構 (TSF) 。</span><span class="sxs-lookup"><span data-stu-id="eb978-147">This causes the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to attempt to start the Text Services Framework (TSF) on the attached control.</span></span> <span data-ttu-id="eb978-148">如果成功，更正使用者介面會顯示在控制項中，並允許存取辨識替代項。</span><span class="sxs-lookup"><span data-stu-id="eb978-148">If successful, the correction user interface shows in the control, and it allows access to recognition alternates.</span></span> <span data-ttu-id="eb978-149">以 **FALSE** 參數呼叫這個方法時，會嘗試關閉附加控制項上的 TSF。</span><span class="sxs-lookup"><span data-stu-id="eb978-149">Calling this method with a **FALSE** parameter attempts to shut down TSF on the attached control.</span></span>

<span data-ttu-id="eb978-150">[InkEdit](/previous-versions/ms552265(v=vs.100))控制項已經提供更正的使用者介面，但在範例 [EnableTsf](/previous-versions/ms569656(v=vs.100))中，是用來讓 [PenInputPanel](/previous-versions/aa514041(v=msdn.10))使用 TSF 插入辨識器內容，而不是 [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput)函式，將手寫辨識結果傳送至控制項。</span><span class="sxs-lookup"><span data-stu-id="eb978-150">The [InkEdit](/previous-versions/ms552265(v=vs.100)) control already provides a correction user interface, but in the sample [EnableTsf](/previous-versions/ms569656(v=vs.100)) is used to enable the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) to use the TSF insertion recognizer context rather than the [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) function to send the handwriting recognition results into the control.</span></span> <span data-ttu-id="eb978-151">結果就是即使欄位不再具有焦點，也可以插入文字。</span><span class="sxs-lookup"><span data-stu-id="eb978-151">The result is that text can be inserted even if the field no longer has focus.</span></span>


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a><span data-ttu-id="eb978-152">關閉表單</span><span class="sxs-lookup"><span data-stu-id="eb978-152">Closing the Form</span></span>

<span data-ttu-id="eb978-153">在 Windows Form 設計工具產生的程式碼中，會在表單初始化時，將 [InkEdit](/previous-versions/ms552265(v=vs.100)) 和 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項加入表單的元件清單中。</span><span class="sxs-lookup"><span data-stu-id="eb978-153">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms552265(v=vs.100)) and [InkPicture](/previous-versions/aa514604(v=msdn.10)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="eb978-154">當表單關閉時，會以表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法處置 InkEdit 和 InkPicture 控制項，以及表單的其他元件。</span><span class="sxs-lookup"><span data-stu-id="eb978-154">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span> <span data-ttu-id="eb978-155">表單的 Dispose 方法也會處置為表單建立的 [筆墨](/previous-versions/aa515768(v=msdn.10)) 物件。</span><span class="sxs-lookup"><span data-stu-id="eb978-155">The form's Dispose method also disposes the [Ink](/previous-versions/aa515768(v=msdn.10)) objects that are created for the form.</span></span>

 

 
