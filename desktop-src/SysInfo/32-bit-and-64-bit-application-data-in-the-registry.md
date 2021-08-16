---
description: 在64位 Windows 中，會分別為32位應用程式和64位應用程式儲存部分的登錄專案，並使用登錄重新導向程式和登錄反映將其對應到個別的邏輯登錄視圖，因為應用程式的64位版本可能會使用不同的登錄機碼和值，而不是使用32位版本。 也有共用的登錄機碼不會重新導向或反映。
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: 登錄中的32位和64位應用程式資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87d5177eb48a5497e321b47bb0da96874a0e6522360f2dc519dc72df3dcdf89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764982"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a>登錄中的32位和64位應用程式資料

在64位 Windows 中，會分別為32位應用程式和64位應用程式儲存部分的登錄專案，並使用登錄[重定向](/windows/desktop/WinProg64/registry-redirector)程式和登錄[反映](/windows/desktop/WinProg64/registry-reflection)將其對應到個別的邏輯登錄視圖，因為應用程式的64位版本可能會使用不同的登錄機碼和值，而不是使用32位版本。 也有共用的登錄機 [碼](/windows/desktop/WinProg64/shared-registry-keys) 不會重新導向或反映。

每個64位登錄節點的父系都是 Image-Specific 節點。 登錄重新導向程式會以透明的方式，將應用程式的登錄存取導向適當的節點。 WOW64 元件會使用名稱 **Wow6432Node** 自動建立登錄樹狀結構中的重新導向子節點。 因此，不需要為您建立的任何登錄機碼命名 **Wow6432Node**。

KEY \_ wow64 \_ 64KEY 和 key \_ wow64 \_ 32KEY 旗標分別啟用對64位登錄視圖和32位視圖的明確存取權。 如需詳細資訊，請參閱 [存取替代登錄視圖](/windows/desktop/WinProg64/accessing-an-alternate-registry-view)。

若要停用並啟用特定索引鍵的登錄反映，請使用 [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) 和 [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) 函數。 應用程式應該只針對其所建立的登錄機碼停用反映，而不會嘗試停用預先定義之索引鍵的反映，例如 **HKEY \_ 本機 \_ 電腦** 或 **HKEY \_ 目前的 \_ 使用者**。 若要判斷反映清單上有哪些索引鍵，請使用 [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) 函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[登錄重新導向程式](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[登錄反映](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
