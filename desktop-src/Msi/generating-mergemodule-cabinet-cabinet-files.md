---
description: 合併模組傳遞至目標安裝套件的每個檔案都必須儲存在 .msm 檔案內內嵌為數據流的封包檔中。 此封包的名稱一律 MergeModule.CABinet。
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: 產生 MergeModule.CABinet 封包檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a26eb9bb3daf92d81e21267b2f56706b74d9179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975161"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a>產生 MergeModule.CABinet 封包檔

合併模組傳遞至目標安裝套件的每個檔案都必須儲存在 .msm 檔案內內嵌為數據流的封包檔中。 此封包的名稱一律 MergeModule.CABinet。

MergeModule.CABinet 中的檔案名必須符合合併模組的檔案 [資料表](file-table.md) 中所使用的主鍵，而且必須遵守在 [合併模組資料庫中命名主鍵](naming-primary-keys-in-merge-module-databases.md)所述的慣例。

安裝程式會略過包含在 MergeModule.CABinet 中的額外檔案，這些檔案未列在合併模組的檔案 [資料表](file-table.md)中。 檔案資料表中指定的檔案序號不需要連續，但它們的順序必須與 MergeModule.CABinet 內儲存的檔案相同。 如需詳細資訊，請參閱 [撰寫合併模組檔案資料表](authoring-merge-module-file-tables.md)。

這表示單一封包檔可以包含合併模組支援多種語言所需的所有檔案。 所有語言檔案都可在封包中提供唯一的序號，然後您可以使用語言轉換來新增或移除檔案資料表中的檔案，以取得特定語言的合併模組。 如需詳細資訊，請參閱 [撰寫多個語言合併模組](authoring-multiple-language-merge-modules.md)。

您可以藉由開啟暫存[ \_ 資料流程資料表](-streams-table.md)，將 MergeModule.CABinet 加入至合併模組。 例如，Windows Installer SDK 提供的工具 Msidb.exe 可以用來將 MergeModule.CABinet 加入至合併模組。 如需詳細資訊，請參閱 [在安裝中包含封包](including-a-cabinet-file-in-an-installation.md)檔。

 

 



