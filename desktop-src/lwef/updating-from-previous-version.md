---
title: 從舊版更新
description: 從舊版更新
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de894f220db7ee09847a8fa767e1f99c38cee8014cb86b65c1251e0579eaabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745721"
---
# <a name="updating-from-previous-version"></a>從舊版更新

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

使用1.5 舊版 Microsoft 代理程式建立和編譯的應用程式，應該在新的2.0 版本下執行，而不需要修改。 [**連接**](connected-property.md)的屬性不能再設為 **False**;已取代的 SpeechInput 物件的某些屬性仍存在，但不再開啟任何值，而且伺服器不會再引發 [**重新開機**](https://www.bing.com/search?q=**Restart**)和 [**關閉**](https://www.bing.com/search?q=**Shutdown**)事件。

但是，如果您將應用程式更新為使用代理程式2.0 控制項，您可能必須修改程式碼。 如果您已安裝2.0 版的 Microsoft 代理程式並載入 Visual Basic 專案，請使用舊版的 Agent 控制項，Visual Basic 包含的選項會自動顯示一則訊息，指出它偵測到新版本的控制項。 為了確保應用程式能正常運作，請一律選擇使用較新的版本。

針對其他程式設計語言 (例如 Microsoft Office 97 VBA) ），您可能必須先移除 1.5 Agent 控制項並儲存您的程式碼，才能更新控制項。 然後，結束程式設計環境、重新開機程式設計環境、重載您的程式碼，然後插入新的控制項。 避免在您要編輯已啟用代理程式1.5 的應用程式之相同程式設計環境的實例中，編輯已啟用代理程式2.0 的應用程式。 某些程式設計環境可能不會處理兩種版本的控制項之間的差異。

安裝代理程式2.0 版之後，您應該能夠在系統上卸載代理程式1.5 版本。 不過，如果代理程式1.5 是透過2.0 版安裝，您可能必須重新安裝2.0。

 

 




