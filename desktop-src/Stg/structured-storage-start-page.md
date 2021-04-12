---
title: 結構化儲存體
description: 結構化儲存區藉由將單一檔案作為結構化的物件集合（稱為儲存和資料流程）來處理，以提供 COM 中的檔案和資料持續性。
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- 結構化儲存體 Strctd Stg。
- 結構化儲存體 Strctd Stg.，起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315706"
---
# <a name="structured-storage"></a>結構化儲存體

## <a name="purpose"></a>目的

結構化儲存區藉由將單一檔案作為結構化的物件集合（稱為儲存和資料流程）來處理，以提供 COM 中的檔案和資料持續性。

結構化儲存區的目的是要降低在單一檔案中儲存個別物件的效能損失和負擔。 結構化儲存體提供方案，方法是定義如何將單一檔案實體處理為兩種類型之物件的結構化集合，以及透過標準的實作為（稱為複合檔案）進行串流處理。 這可讓使用者與複合檔案進行互動及管理，就像是單一檔案，而不是個別物件的嵌套階層一樣。

## <a name="where-applicable"></a>適用時

結構化儲存體可用於以 Microsoft COM 為基礎的作業系統上。

## <a name="developer-audience"></a>開發人員對象

結構化儲存體檔適用于有經驗的 C 和 c + + 程式設計人員，以及以 COM 為基礎的系統開發人員。

結構化儲存體主要支援 C 和 c + + 程式設計語言，但任何以 COM 為基礎的技術也會支援任何使用介面指標的程式設計語言。

強烈瞭解 COM 技術是開發使用結構化儲存體的必要條件。

## <a name="run-time-requirements"></a>執行階段需求求

如需有關使用特定 API 專案所需之作業系統的詳細資訊，請參閱元素檔集的需求一節。

## <a name="in-this-section"></a>本節內容



| 主題                                                               | 描述                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [概觀](about-structured-storage.md)<br/>                 | 結構化儲存體的一般資訊。<br/>                                                                                                                                                                                                                                                 |
| [使用結構化儲存體](using-structured-storage.md)<br/> | 使用結構化儲存體的資訊。<br/>                                                                                                                                                                                                                                                     |
| [參考](structured-storage-reference.md)<br/>            | 結構化儲存體特定介面、函數、結構和列舉的檔。<br/>                                                                                                                                                                                             |
| [範例](samples.md)<br/>                                   | 以 c + + 撰寫的程式碼範例。 如需詳細資訊，請參閱 [IStorage](names-in-istorage.md)中的名稱、 [屬性集標頭](property-set-header.md)、 [區段](section.md)、 [儲存屬性集](storing-property-sets.md)，以及 [使用結構化儲存體](using-structured-storage.md)。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[元件物件模型](../com/the-component-object-model.md)
</dt> </dl>

 

