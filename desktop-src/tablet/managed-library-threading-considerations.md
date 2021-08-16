---
description: 下列 Tablet PC 執行緒的考慮是受管理的程式庫所特有。
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Managed 程式庫執行緒考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60908618fe3b566a552167f3448ee1d4269f9246c7b08f9bb1acf3269cf2ae77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031706"
---
# <a name="managed-library-threading-considerations"></a>Managed 程式庫執行緒考慮

下列 Tablet PC 執行緒的考慮是受管理的程式庫所特有。

-   [執行緒安全性](#thread-safety)
-   [STA 和 MTA 應用程式](#sta-and-mta-applications)
-   [Windows表單執行緒考慮](#windows-forms-threading-considerations)
-   [剪貼簿考慮](#clipboard-considerations)
-   [事件處理常式內的例外狀況](#exceptions-within-event-handlers)
-   [處置物件和控制項](#disposing-objects-and-controls)
-   [StylusInput Api](#stylusinput-apis)

## <a name="thread-safety"></a>Thread-Safety

Tablet PC 平臺的 Managed 程式庫類別通常不是安全線程。 下列集合是成員層級上的安全線程;但是，如果另一個執行緒同時在集合上操作，則這些集合不保證會保護列舉值：

-   [CursorButtons](/previous-versions/ms839506(v=msdn.10))
-   [資料指標](/previous-versions/ms839493(v=msdn.10))
-   [DivisionUnits](/previous-versions/ms837954(v=msdn.10))
-   [RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))
-   [辨識器](/previous-versions/ms828520(v=msdn.10))
-   [平板電腦](/previous-versions/ms827599(v=msdn.10))

## <a name="sta-and-mta-applications"></a>STA 和 MTA 應用程式

使用 Microsoft Visual Studio .net 中包含的嚮導所建立的受控應用程式，預設是單一執行緒的單元 (STA) 。 您可以藉由在應用程式的進入點上設定 STA 執行緒或多執行緒單元 (MTA) thread 屬性，來變更應用程式的單元。

如果您的應用程式是在 MTA 中執行，您必須撰寫安全線程的程式碼;不過，藉由這麼做，您就可以改善某些事件處理效能問題。

如需 STA 執行緒和 MTA 執行緒屬性的詳細資訊，請參閱 [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) 類別和 [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) 類別。

## <a name="windows-forms-threading-considerations"></a>Windows表單執行緒考慮

[InkPicture](/previous-versions/aa514604(v=msdn.10))和[InkEdit](/previous-versions/ms552265(v=vs.100))控制項會擴充 Windows Forms 控制項。 WindowsForms 控制項使用單一執行緒的單元 (STA) 模型，因為 Windows Forms 是以原本就是單一執行緒的原生 Win32 視窗為基礎。 在 managed 程式碼中，筆墨控制項應該在與表單主執行緒相同的執行緒中建立。

在 STA 應用程式中，某些事件會發生在應用程式的使用者介面以外的執行緒上， (UI) 執行緒。 從 Tablet PC 事件處理常式內呼叫任何 Windows Forms 物件或控制項（包括[InkPicture](/previous-versions/aa514604(v=msdn.10))和[InkEdit](/previous-versions/ms552265(v=vs.100))控制項）時，請使用物件或控制項的繼承[控制項。 Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1)方法。 [System.windows.forms.control.invokerequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1)屬性（繼承自 Control 類別）可以用來判斷是否需要此屬性。

例如 [，在下列辨識事件的](/previous-versions/ms829424(v=msdn.10)) 事件處理常式中，會測試 [system.windows.forms.control.invokerequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) 屬性，如果是 **TRUE**，就會從使用者介面執行緒重新叫用事件處理常式。


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



如果您將 [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) 放到 awebpagein 瀏覽器 (查看) 的 [Web 控制項](web-controls.md) ，則會以 STA 應用程式的形式執行。 針對智慧型用戶端應用程式 (看 [不到任何 Touch 部署](no-touch-deployment.md)) ，開發人員可以完全掌控 [system.threading.thread.apartmentstate](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1)。  (預設值通常是 STA，但可以是 MTA （視您的 CLR 版本而定）。 ) 涉及 [**RealTimeStylus**](realtimestylus-class.md)的執行緒問題，請參閱 [StylusInput Api 的執行緒考慮](threading-considerations-for-the-stylusinput-apis.md)。

如需從 MTA 應用程式呼叫 Windows Forms 的詳細資訊，請參閱[多執行緒 Windows Forms 控制項範例](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71))。

## <a name="clipboard-considerations"></a>剪貼簿考慮

[剪貼](../dataxchg/clipboard.md)簿物件僅適用于 STA 執行緒。 嘗試從不是 STA 的執行緒複製或貼上剪貼簿時，您會收到 [system.threading.threadstateexception](/previous-versions/windows/)。 如果您的應用程式是 MTA，請建立 STA 執行緒來處理剪貼簿的方法呼叫，以及您應用程式的一些其他 UI 層面。

## <a name="exceptions-within-event-handlers"></a>事件處理常式內的例外狀況

無法從 Tablet PC 事件處理常式中擲回例外狀況。 例如，如果 Tablet PC 物件或集合的事件處理常式委派有三個已註冊的處理常式，而第一個處理常式擲回例外狀況，則會發生下列順序：

1.  第一個處理常式會結束。
2.  例外狀況會遺失。
3.  不會叫用剩餘的處理常式。

## <a name="disposing-objects-and-controls"></a>處置物件和控制項

若要避免記憶體流失，您必須在物件或控制項超出範圍之前，于已附加事件處理常式的任何 Tablet PC 物件或控制項上明確呼叫 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法。

若要改善應用程式的效能，請在不再需要物件或控制項時，手動處置任何執行 [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法的 Tablet PC 物件或控制項。

## <a name="stylusinput-apis"></a>StylusInput Api

如需有關 [**RealTimeStylus**](realtimestylus-class.md) 物件的執行緒考慮和 StylusInput 應用程式設計介面 (api 的詳細資訊) 參閱 [StylusInput Api 的執行緒考慮](threading-considerations-for-the-stylusinput-apis.md)。

 

 
