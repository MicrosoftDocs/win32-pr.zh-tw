---
description: 說明如何建立數學輸入控制項。
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: 建立數學輸入控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5084f29943395bc6781fe20598f86bdc08c6c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561519"
---
# <a name="creating-a-math-input-control"></a>建立數學輸入控制項

若要建立數學輸入控制項，您必須：

-   [包含數學輸入控制項的標頭和程式庫](#include-headers-and-libraries-for-the-math-input-control)
-   [宣告控制項指標並呼叫控制項指標上的 CoInitialize](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [顯示控制項](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a>包含數學輸入控制項的標頭和程式庫

下列程式碼應該放在您將使用數學輸入控制項的程式碼頂端。


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



此程式碼會將數學輸入控制項的支援新增至您的應用程式。

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a>宣告控制項指標並呼叫控制項指標上的 CoInitialize

在您包含控制項的標頭之後，您可以宣告控制項指標，並可在其上呼叫 CoInitialize 來建立數學輸入控制項介面的控制碼。 下列程式碼可以放置於類別中，或做為應用程式執行中的全域變數：


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



下列程式碼顯示如何在控制項指標上呼叫 CoInitialize。


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



呼叫控制項指標上的 CoInitialize 之後，您就會有控制項的參考，而且可以存取控制項的方法。 例如，您可以啟用一組延伸的控制項，如下列範例所示。


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a>顯示控制項

建立控制項之後，將不會自動顯示該控制項。 若要顯示控制項，請呼叫您在上一個步驟中建立的控制項參考上的 [**show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) 方法。 下列程式碼會示範如何呼叫 [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) 方法。


```
   hr = g_spMIC->Show();
   
```



控制項顯示之後，看起來會像下圖。

![顯示數學輸入控制項的螢幕擷取畫面](images/mic.png)

請注意，我已啟用一組延伸的按鈕，讓您可以使用 **重做** 和 **復原** 。

 

 
