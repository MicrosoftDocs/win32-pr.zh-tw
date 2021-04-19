---
description: 疑難排解秘訣
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: 疑難排解秘訣
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0280702c7ce2131d1252ec75b8bee4be231e29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993192"
---
# <a name="troubleshooting-tips"></a>疑難排解秘訣

下列秘訣可協助您避免在您的 DirectShow 應用程式中發生鎖死或損毀。

**全域物件**

全域 c + + 物件不應該在其函式方法中建立 DirectShow 物件，或在其函式方法中釋放它們。 這樣做可能會導致應用程式無限期地封鎖，原因如下：

執行緒無法在 DLL 的進入點函數內結束。 核心32會在進入點函式期間保存全域程式鎖定，而且鎖定會防止執行緒結束。 因為某些 DirectShow 物件擁有線程，所以如果是從 DLL 進入點函式內釋出，就可以封鎖它們。 如果應用程式有全域 c + + 物件，則在卸載 DLL 時，C 執行時間 DLL 會呼叫物件的「函式」。 如果函式會釋出 DirectShow 物件，它可以封鎖結果。

基於類似的原因，DLL 不應該在其進入點常式中建立或釋放 DirectShow 物件。

**釋放介面**

當您的應用程式仍在處理訊息時，您應該釋放所有的 DirectShow 介面指標，然後才結束訊息迴圈。 否則，您可能會看到各種判斷提示，因為某些 DirectShow 物件會在其清除常式期間傳送訊息。

 (為必然結果，如果您使用 ATL **CWindowImpl** 類別，請勿等候 **OnFinalMessage** 釋放介面。 相反地，當您處理 WM 關閉訊息時，請釋放這些專案 \_ 。 ) 

**參考計數**

當 Quartz.dll 卸載的偵錯工具時，它會檢查是否有任何 DirectShow 物件具有未釋放的參考計數。 如果是，則會擲回判斷提示：


```C++
g_cFGObjects == 0 
```



當此判斷提示失敗時，表示您的應用程式已洩漏參考計數。 請檢查您的程式碼，並確定您已釋放所有介面指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 中進行調試](debugging-in-directshow.md)
</dt> </dl>

 

 



