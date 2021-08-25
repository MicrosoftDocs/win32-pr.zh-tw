---
title: Windows事件記錄檔參考
description: 以下是您用來建立檢測資訊清單、從提供者使用的資訊清單建立資源、在執行時間取得檢測中繼資料，以及從通道和記錄檔查詢事件的程式設計項目
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6ce52f3756b8f33ac710e189677de053dc538339d0a0cdeb335410dd76a171
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957788"
---
# <a name="windows-event-log-reference"></a>Windows事件記錄檔參考

以下是您用來建立檢測資訊清單、從提供者使用的資訊清單建立資源、在執行時間取得檢測中繼資料，以及從通道和記錄檔查詢事件的程式設計項目：

-   [EventManifest 架構](eventmanifestschema-schema.md)
-   [事件架構](eventschema-schema.md)
-   [查詢架構](queryschema-schema.md)
-   [Windows事件記錄檔常數](windows-event-log-constants.md)
-   [Windows事件記錄檔資料類型](windows-event-log-data-types.md)
-   [Windows事件記錄檔列舉](windows-event-log-enumerations.md)
-   [Windows事件記錄檔函數](windows-event-log-functions.md)
-   [Windows事件記錄檔結構](windows-event-log-structures.md)
-   [Windows事件記錄檔工具](windows-event-log-tools.md)

針對使用 .net 語言（例如 c # 或 Visual Basic）撰寫的應用程式，請參閱下列命名空間：

-   若要寫入事件，請 [使用在 system.string 命名空間](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) 中定義的類別和方法。
-   若要使用 Windows 事件記錄檔通道或記錄檔中的事件，請使用在中定義[的類別](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true)和方法。

除了使用 [system.servicemodel 命名空間](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) 來寫入事件之外，您還可以使用 **-cs** 或 **-css** 引數，讓訊息編譯器產生程式碼來寫入事件。 如需詳細資訊，請參閱 [**訊息編譯器**](message-compiler--mc-exe-.md)。
