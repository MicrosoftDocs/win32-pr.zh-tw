---
title: 'Windows 事件記錄檔 (的新功能) '
description: 此頁面摘要說明針對每個版本新增至 Windows 事件記錄檔 API 的新功能。
ms.assetid: 90adf08c-177f-46ae-82e1-f7cca5a46db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652d82f67292316dd7aec599955d69dd70ab39a3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106965270"
---
# <a name="whats-new-windows-event-log"></a>Windows 事件記錄檔 (的新功能) 

此頁面摘要說明針對每個版本新增至 Windows 事件記錄檔 API 的新功能。

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 與 Windows Server 2008 R2

以下是對 [EventManifest](eventmanifestschema-schema.md) 架構進行的變更：

-   已移除 [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) 複雜類型。 若要提供相同的功能，請使用工作特定的作業碼 (查看 [**TaskType**](eventmanifestschema-tasktype-complextype.md)複雜 **類型的 opcode 元素。**
-   新增 [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md)、 [**filePath**](eventmanifestschema-filepath-simpletype.md)和 [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) 簡單類型，以限制指派給這些類型之屬性的值。
-   將 **篩選** 屬性加入至 [**ProviderType**](eventmanifestschema-providertype-complextype.md) 複雜類型。 提供者可以使用篩選器，就像提供者使用層級和關鍵字來判斷是否應該撰寫事件一樣。
-   新增下列輸出類型，您可以為事件資料範本中定義的資料項目指定這些輸出類型：
    -   win： DateTimeCultureInsensitive
    -   win： HResult
    -   win： NTSTATUS
-   輸出類型現在已被接受，但在忽略之前。

Windows 7 版 Windows SDK 隨附的 [**訊息編譯器**](message-compiler--mc-exe-.md) 版本已進行下列變更：

-   已新增引數，讓編譯器根據您的資訊清單產生記錄程式碼。 您也可以要求編譯器產生程式碼，以在 Windows Vista 之前的作業系統上記錄事件。 如需引數的清單，請參閱 [**訊息編譯器**](message-compiler--mc-exe-.md) 主題的「產生用來記錄事件的程式碼特定的引數」一節。
-   編譯器現在會在資訊清單上強制執行更嚴格的語法和語意驗證。 這可能會導致在舊版訊息編譯器上成功編譯的一些資訊清單需要變更，才能使用最新版本順利進行編譯。
