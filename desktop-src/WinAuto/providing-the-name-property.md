---
title: 提供 Name 屬性
description: 在建立預先定義和通用的控制項時，伺服器開發人員必須小心，以確保 Microsoft Active Accessibility 可以公開控制項的 [名稱] 屬性。
ms.assetid: 2b4ec5ae-bda1-41e6-9387-6ee3cb6c3163
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c93205430f3063b993c49a7145658d7748aac0e697257789c31ac0653d6189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052546"
---
# <a name="providing-the-name-property"></a>提供 Name 屬性

在建立預先定義和通用的控制項時，伺服器開發人員必須小心，以確保 Microsoft Active Accessibility 可以公開控制項的 [ [名稱] 屬性](name-property.md) 。 根據控制項的類型，[名稱] 屬性的文字來自下列其中一項：

-   控制項的視窗文字 (或標題) 
-   標記控制項的靜態文字

若要尋找控制項的視窗文字，Microsoft Active Accessibility 將 [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) 訊息傳送至控制項。 此文字對應至控制項的資源定義語句中的 text 參數。 對於某些控制項（例如按鈕），這是與控制項一起顯示的相同文字。 若為其他控制項（例如工具列），則不會顯示此文字。 因此，伺服器開發人員必須在控制項的資源定義語句中提供有意義的文字，以協助用戶端公用程式的使用者識別控制項。

若要尋找控制項的標籤，Microsoft Active Accessibility 使用 GW HWNDPREV 旗標呼叫 [**GetWindow**](/windows/desktop/api/winuser/nf-winuser-getwindow) 來搜尋靜態文字控制項 \_ 。 如果找到靜態文字控制項，或如果遇到具有視窗樣式 WS \_ GROUP ws TABSTOP 的控制項，則會停止搜尋 \| \_ 。 此搜尋順序對應至對話方塊上的反向定位順序。 伺服器開發人員必須在建立控制項時觀察定位順序，如此一來，靜態文字控制項就會緊接在其所標記的控制項之前。

如需 Microsoft Active Accessibility 用來公開 [Name 屬性](name-property.md)之技巧的詳細資訊，請參閱 [消費者介面元素參考](user-interface-element-reference.md)。

 

 