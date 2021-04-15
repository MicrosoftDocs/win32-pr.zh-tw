---
description: Tablet PC 的筆墨控制項總覽。
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: 筆墨控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511305"
---
# <a name="ink-controls"></a>筆墨控制項

Tablet PC 平臺提供兩種控制項： [InkEdit](inkedit-control.md) 和 [InkPicture](inkpicture-control.md)，可讓您輕鬆地將筆跡和手寫辨識新增到 Tablet PC 應用程式。 InkEdit 控制項具有 [managed](/previous-versions/ms835842(v=msdn.10))、 [ActiveX](inkedit-control-reference.md) 和 Win32 版本，而 InkPicture 只有 managed [InkPicture](/previous-versions/ms583740(v=vs.100)) 和 [activex](inkpicture-control-reference.md) 版本。

控制項之間的主要差異在於資料的儲存方式。 [InkEdit](inkedit-control.md)控制項會依預設將筆墨儲存為文字，而[InkPicture](inkpicture-control.md)則會將筆墨儲存為筆跡。

[InkEdit](inkedit-control.md)控制項適用于透過手寫辨識的文字輸入。 [InkPicture](inkpicture-control.md) 適用于批註 (例如，標示簡報投影片或其他圖片) 。

在 managed 程式碼中，在與表單主執行緒相同的執行緒中建立筆墨控制項。 如果在不同的執行緒中建立 [InkEdit](inkedit-control.md) 或 [InkPicture](inkpicture-control.md) 控制項，則您的應用程式可能無法正確回應。

建立筆墨控制項之前，您應該明確地將執行緒模型變更為單一線程的單元 (STA) 。 這會導致在主執行緒上建立控制項。 您可以使用下列 Managed c + + 程式碼來明確設定執行緒模型。


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



您可以使用下列程式碼，在 C 中執行相同的動作 \# 。


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



在 managed 程式碼中，若要避免記憶體流失，您必須在控制項超出範圍之前，于已附加事件處理常式的任何 Tablet PC 控制項上明確呼叫 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法。

下列各節說明筆墨控制項，以及在應用程式中使用筆墨控制項的方式：

-   [將筆墨控制項新增至專案](adding-ink-controls-to-a-project.md)
-   [InkEdit 控制項](inkedit-control.md)
-   [InkPicture 控制項](inkpicture-control.md)

 

 
