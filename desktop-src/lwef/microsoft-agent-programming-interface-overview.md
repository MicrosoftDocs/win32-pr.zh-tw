---
title: Microsoft 代理程式設計介面總覽
description: Microsoft 代理程式設計介面總覽
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4dc087064afb0e3beaaf97d987e496239d3fd378461acaf5601927ac6d929
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887918"
---
# <a name="microsoft-agent-programming-interface-overview"></a>Microsoft 代理程式設計介面總覽

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

Microsoft Agent API 提供支援動畫字元之顯示和動畫的服務。 Microsoft Agent 會實作為 OLE Automation (元件物件模型 \[ COM \]) server，可讓多個應用程式（稱為用戶端或用戶端應用程式）同時裝載和存取其動畫、輸入和輸出服務。 用戶端可以是連接至 Microsoft 代理程式 COM 介面的任何應用程式。

作為 COM 伺服器，只有在用戶端應用程式使用 COM 介面和要求連接到該伺服器時，Microsoft Agent 才會自動啟動。 它會繼續執行，直到所有用戶端關閉其連接為止。 如果沒有連線的用戶端，Microsoft 代理程式會自動結束。

雖然您可以直接呼叫 microsoft 代理程式的 COM 介面，但 microsoft 代理程式也包含 microsoft ActiveX 控制項。 此控制項可讓您輕鬆地從支援 ActiveX 控制介面的程式設計語言存取 Microsoft 代理程式的服務。

除了支援針對 Windows 所撰寫的獨立程式之外，也可以編寫代理程式來支援網頁，但前提是瀏覽器支援 ActiveX 介面。 Microsoft Internet Explorer 包含 ActiveX 的支援，以及可用於程式設計程式的指令碼語言。 如果您不是使用 Internet Explorer，請洽詢您的廠商或供應商，以瞭解瀏覽器對於 ActiveX 的支援。

下列資訊提供 Microsoft 代理程式軟體之程式設計介面的簡短總覽。

-   [動畫服務](animation-services.md)
-   [輸入服務](input-services.md)
-   [語音命令視窗](the-voice-commands-window.md)
-   [輸出服務](output-services.md)

 

 




