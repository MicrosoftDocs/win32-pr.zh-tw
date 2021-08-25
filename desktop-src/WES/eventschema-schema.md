---
title: 事件結構描述
ms.assetid: 36037697-b777-4e5c-99af-77964200a3e4
description: 深入瞭解：事件架構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c08e22ad44cb1eec461ebe70361a8ee4640a7fdf5a7eb7040b2774a520be7a05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904358"
---
# <a name="event-schema"></a>事件結構描述

事件架構會定義下列專案和類型，以識別已記錄事件的元素和屬性：

-   [EventSchema 元素](eventschema-elements.md)
-   [EventSchema 簡單類型](eventschema-simple-types.md)
-   [EventSchema 複雜類型](eventschema-complex-types.md)

Elements 區段包含您會在記錄的事件中尋找的元素名稱;不過，若要取得每個專案的詳細資料，請參閱包含元素的複雜類型。

Windows SDK 包含 \\ include 事件 .xsd 檔中的架構 \\ 。

您可以在呼叫 [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) 函式以轉譯事件的特定區段或屬性時，使用此架構來識別元素和屬性。 如需顯示如何在轉譯事件時使用這個架構的範例，請參閱轉譯 [事件](rendering-events.md)。

除了事件架構之外，Windows 事件記錄檔也會定義下列架構：

-   [EventManifest 架構](eventmanifestschema-schema.md)：定義用來寫入檢測資訊清單的元素和類型。
-   [查詢架構](queryschema-schema.md)：定義用來撰寫查詢以從一或多個通道取出事件的元素和類型。

 

 




