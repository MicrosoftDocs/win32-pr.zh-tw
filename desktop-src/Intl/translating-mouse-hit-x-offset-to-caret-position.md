---
description: 傳統上，使用者可以選取插入號位置 (cp) ，方法是按一下尾端的字元 &\# 0034; cp-1&\# 0034; 或字元開頭的一半 &\# 0034; cp&\# 0034;。
ms.assetid: 36b6ff00-7ea8-40e5-90f7-917cef117d4a
title: 將滑鼠點擊次數 X 位移轉換成插入號位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e135efaccb6454e55999d21f00e762d749eb380751848aef88cf4b4e5b8e913
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693178"
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

 

 



