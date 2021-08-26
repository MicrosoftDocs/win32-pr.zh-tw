---
description: 此範例會藉由整合 PenInputPanel 物件，以自動宣告表單範例為基礎。 此範例位於 \# AutoClaims 資料夾的 C PIPanel 目錄中。
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: PenInputPanel 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c464be52fd08c6c461ba094428a1868fbb51fb328e1a3c88a2d0949a6ae581e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934738"
---
# <a name="peninputpanel-sample"></a>PenInputPanel 範例

此範例會藉由整合 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件，以自動宣告表單範例為基礎。 此範例位於 \# AutoClaims 資料夾的 C PIPanel 目錄中。

> [!Note]  
> 此範例會要求您的系統配備了畫筆裝置。 如果您只是使用滑鼠 (或其他非人力介面裝置 (隱藏) 指向裝置) [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 不會出現。

 

如需自動宣告表單範例的詳細資訊，請參閱 [自動宣告表單範例](auto-claims-form-sample.md)。 如需 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件的詳細資訊，請參閱 [使用 PenInputPanel 類別設計輸入面板](programming-the-input-panel-using-the-peninputpanel-class.md)。

在此範例中，「自動宣告」表單包含五個欄位，要求使用者將相關資訊放入與該宣告相關的資訊：原則號碼、保險名稱、年份、製作和汽車型號。 [PenInputPanel](/previous-versions/aa514041(v=msdn.10))物件會附加至每個輸入欄位，以提供使用畫筆輸入值的簡單方法。

有兩種技巧可將 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件附加至表單上的輸入欄位。 第一個技巧是在設計階段將物件的個別實例指派給每個輸入欄位。 第二種方式是建立物件的單一實例，然後在執行時間將該物件實例附加至接收焦點的欄位。 這個範例會示範這兩種技術。

決定要使用的技巧有一些取捨。 在載入表單時，為每個表單欄位建立物件的唯一實例，需要更多的記憶體。 但是，它可以節省在執行時間將單一實例指派給目前欄位的欄位處理焦點事件。

由於 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件只在平板電腦上受到支援，因此此範例會在例外狀況處理區塊內建立 PenInputPanel 物件。

## <a name="one-object-per-field"></a>每個欄位一個物件

此範例會示範第一種技術 (每個欄位) 一個 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件，方法是指派原則編號的輸入欄位 (`inkEdPolicyNumber`) 和保險名稱 (`inkEdName`) PenInputPanel 物件的唯一實例。 PenInputPanel 物件的多載函式可以採用輸入控制項的名稱做為引數，進而使控制項產生關聯。 表單的 [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) 事件處理常式中的下列幾行顯示如下：


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a>每個表單一個物件

第二個技術也會顯示在範例中： [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件的單一實例，在 `pipShared` Year、Make 和 Model 輸入欄位之間共用。 共用物件是使用預設的函式建立的。


```C++
pipShared = new PenInputPanel();
```



使用這項技術需要您的表單只有 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件的單一實例。 這樣可以節省記憶體，但是當輸入欄位收到焦點時，您必須加入程式碼來處理事件。 當使用 PenInputPanel 物件之共用實例的控制項取得焦點時，請將 PenInputPanel 物件的 [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) 屬性設定為該控制項。 下列程式碼顯示 Year、Make 和 Model 欄位之事件的事件處理常式 `Enter` 。


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



當焦點變更至新的控制項時，請務必設定任何需要設定的屬性。 例如，在先前的事件處理常式中，會適當地設定 [模擬](/previous-versions/ms571978(v=vs.100)) 程式屬性。

## <a name="usability-considerations"></a>可用性考慮

在您的應用程式中使用 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件時，請記住下列可用性考慮。

### <a name="positioning-the-peninputpanel"></a>定位 PenInputPanel

因為欄位在此範例中的表單上會垂直配置，所以每個輸入控制項的 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 使用者介面都會放在輸入控制項的右邊，使其更容易使用。 這可防止 PenInputPanel 涵蓋下一個編輯方塊，讓您更輕鬆地以下一個編輯方塊為目標。


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a>選取要顯示的輸入面板

由於原則號碼通常是數位、字母和其他字元的組合，因此很容易辨識錯誤。 因此，此範例會將 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件所顯示的預設面板，設定為附加至 [原則號碼] 欄位時的鍵盤。


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



[PenInputPanel](/previous-versions/aa514041(v=msdn.10))物件的預設行為是使用使用者最後選取的面板。

### <a name="text-services-framework-correction-user-interface"></a>文字服務架構更正消費者介面

在此範例中，所有的輸入欄位都是 [InkEdit](/previous-versions/ms552265(v=vs.100)) 控制項。 這是很重要的，因為 InkEdit 控制項內建支援 [文字服務架構](../tsf/text-services-framework.md) (TSF) ，因此能夠支援從 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件接收之輸入的就地更正使用者介面。

[EnableTsf](/previous-versions/ms569656(v=vs.100))的預設值為 **TRUE**。 這會導致 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件嘗試啟動附加控制項上的文字服務架構 (TSF) 。 如果成功，更正使用者介面會顯示在控制項中，並允許存取辨識替代項。 以 **FALSE** 參數呼叫這個方法時，會嘗試關閉附加控制項上的 TSF。

[InkEdit](/previous-versions/ms552265(v=vs.100))控制項已經提供更正的使用者介面，但在範例 [EnableTsf](/previous-versions/ms569656(v=vs.100))中，是用來讓 [PenInputPanel](/previous-versions/aa514041(v=msdn.10))使用 TSF 插入辨識器內容，而不是 [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput)函式，將手寫辨識結果傳送至控制項。 結果就是即使欄位不再具有焦點，也可以插入文字。


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a>關閉表單

在 Windows 表單設計工具產生的程式碼中，會在表單初始化時，將[InkEdit](/previous-versions/ms552265(v=vs.100))和[InkPicture](/previous-versions/aa514604(v=msdn.10))控制項加入表單的元件清單中。 當表單關閉時，會以表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法處置 InkEdit 和 InkPicture 控制項，以及表單的其他元件。 表單的 Dispose 方法也會處置為表單建立的 [筆墨](/previous-versions/aa515768(v=msdn.10)) 物件。

 

 
