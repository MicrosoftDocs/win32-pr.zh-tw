---
description: 描述如何建立 PenInputPanel 物件。
ms.assetid: fd9ce912-5cec-4bec-b7d8-5a4f71000c95
title: 建立 PenInputPanel 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072d5dca28801ee45b7747504a93d755443cfb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986273"
---
# <a name="creating-a-peninputpanel-object"></a>建立 PenInputPanel 物件

\[[**PenInputPanel**](peninputpanel-class.md) 已被 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 和 [>textinput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90))取代。 請參閱 [文字輸入面板](programming-the-text-input-panel.md)的程式設計。\]

Managed 程式碼的函式會提供便利的方式來建立 [PenInputPanel](/previous-versions/ms583923(v=vs.100)) 物件，並在一個步驟中將它附加至控制項。 此 C \# 範例會建立 PenInputPanel 物件，並使用一行程式碼將它附加至現有的 [InkEdit](/previous-versions/ms835842(v=msdn.10)) 控制項 `InkEdit1` 。


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



Visual Basic .NET 中的相同範例看起來像這樣：


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



當某個 [PenInputPanel](/previous-versions/ms583923(v=vs.100)) 物件在其存留期內會與單一控制項相關聯時，這項技術會很有用。 如果您想要使用一個 PenInputPanel 物件，並將它與多個控制項相關聯（如 [PenInputPanel 範例](peninputpanel-sample.md)所示），請使用 [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) 屬性來變更 PenInputPanel 物件所關聯的控制項。

若要在不使用函數的情況下將 [PenInputPanel](/previous-versions/ms583923(v=vs.100)) 物件附加至控制項，請使用 [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) 屬性。 針對不支援 managed 的函式（例如 c + +）的語言，請使用此技術。

 

 
