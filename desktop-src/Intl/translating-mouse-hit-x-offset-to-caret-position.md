---
description: 傳統上，使用者可以選取插入號位置 (cp) ，方法是按一下尾端的字元 &\# 0034; cp-1&\# 0034; 或字元開頭的一半 &\# 0034; cp&\# 0034;。
ms.assetid: 36b6ff00-7ea8-40e5-90f7-917cef117d4a
title: 將滑鼠點擊次數 X 位移轉換成插入號位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f993de35ebffac4740b367927d1a8edf864a813e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849474"
---
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a>將滑鼠點擊次數 X 位移轉換成插入號位置

傳統上，使用者可以選取插入號位置 (cp) ，方法是按一下尾端的字元 "cp-1" 或字元 "cp" 的尾端半形。 應用程式可以依照下列方式，將滑鼠點擊的 x 位移轉譯成插入號：


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



針對將插入號貼到叢集界限的腳本， [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) 的呼叫會傳回，而 *fTrailing* 會在程式碼點中設定為0或叢集的寬度。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



