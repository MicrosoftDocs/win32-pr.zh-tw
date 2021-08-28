---
title: EventManifest 架構
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: 深入瞭解： EventManifest 架構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8b282a3570c7ddc510f55c012a13b9438108693a3b6abba06de08ce1da59d734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055846"
---
# <a name="eventmanifest-schema"></a>EventManifest 架構

EventManifest 架構會定義您用來撰寫檢測資訊清單的下列元素和類型：

-   [EventManifestSchema 元素](eventmanifestschema-elements.md)
-   [EventManifestSchema 簡單類型](eventmanifestschema-simple-types.md)
-   [EventManifestSchema 複雜類型](eventmanifestschema-complex-types.md)

Elements 區段包含您在資訊清單中使用的元素名稱;不過，若要取得每個專案的詳細資料，請參閱包含元素的複雜類型。

檢測資訊清單是一種 XML 檔案，可定義事件提供者、寫入事件的通道、事件本身、事件篩選準則（例如層級、工作和 opcode），以及轉譯事件時使用的當地語系化字串。 慣例是使用. man 做為資訊清單檔的副檔名。 如需寫入資訊清單的詳細資訊，請參閱 [撰寫檢測資訊清單](writing-an-instrumentation-manifest.md)。

Windows SDK 包含 \\ 包含 Eventman .xsd 檔案中的架構。 \\ 您可以使用 XSD 來驗證您的資訊清單。

除了 EventManifest 架構之外，Windows 事件記錄檔也會定義下列架構：

-   [事件架構](eventschema-schema.md)：定義用來呈現事件的元素和類型。
-   [查詢架構](queryschema-schema.md)：定義用來撰寫查詢以從一或多個通道取出事件的元素和類型。

 

 




