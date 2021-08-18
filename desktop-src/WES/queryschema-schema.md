---
title: 查詢架構
ms.assetid: 5710231b-5195-413e-8953-e47a411897a6
description: 深入瞭解：查詢架構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 14beeaf8c4d739e490de972107fedf279e16e75b5401f63a709d43b03c338c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005168"
---
# <a name="query-schema"></a>查詢架構

查詢架構會定義下列專案和類型，您可用來撰寫結構化 XML 查詢，以從通道或記錄檔抓取事件：

-   [QuerySchema 元素](queryschema-elements.md)
-   [QuerySchema 複雜類型](queryschema-complex-types.md)

Elements 區段包含您在查詢中使用的元素名稱;不過，若要取得每個專案的詳細資料，請參閱包含元素的複雜類型。

查詢可包含一或多個用來在查詢結果集中包含或排除事件的 XPath 運算式。 您可以從多個通道或記錄檔查詢事件，但是不能混用通道和記錄檔。 您可以在任何採用 XPath (的函式中使用查詢，例如， [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) 或 [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) 函數) 。 您指定的每個 XPath 都會限制為32個運算式。 如需範例，請參閱 [使用事件](consuming-events.md)。

Windows SDK 包括 \\ Include 查詢 .xsd 檔中的架構 \\ 。

除了查詢架構之外，Windows 事件記錄檔也會定義下列架構：

-   [EventManifest 架構](eventmanifestschema-schema.md)：定義用來寫入檢測資訊清單的元素和類型。
-   [事件架構](eventschema-schema.md)：定義用來呈現事件的元素和類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用事件](consuming-events.md)
</dt> </dl>

 

 




