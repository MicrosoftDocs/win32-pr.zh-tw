---
description: 合併模組基本上是簡化的 .msi 檔案，也就是 Windows Installer 安裝套件的副檔名。 標準合併模組的副檔名為 .msm。
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: 關於合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70d416b89f0979d5651480a05052e95b4d32e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319044"
---
# <a name="about-merge-modules"></a>關於合併模組

合併模組基本上是簡化的 .msi 檔案，也就是 Windows Installer 安裝套件的副檔名。 標準合併模組的副檔名為 .msm。

無法單獨安裝合併模組，因為它缺少安裝資料庫中有的一些重要資料庫資料表。 合併模組也包含本身特有的其他資料表。 若要安裝合併模組與應用程式所提供的資訊，模組必須先合併到應用程式的 .msi 檔案中。

合併模組包含下列部分：

-   [合併模組資料庫](merge-module-database.md)，包含合併模組所傳遞的安裝屬性和安裝邏輯。
-   描述模組的 [合併模組摘要資訊資料流程參考](merge-module-summary-information-stream-reference.md) 。
-   [MergeModule.CABinet](mergemodule-cabinet.md)封包檔儲存為合併模組內的資料流程。 此封包包含合併模組所傳遞的元件所需的所有檔案。

[多個語言合併模組](multiple-language-merge-modules.md) 可將元件傳遞至多個語言的安裝套件。 在多個語言合併模組中，資料庫包含多個語言的安裝屬性和邏輯，而 MergeModule.CABinet 封包包含安裝元件所需的所有檔案，以及模組支援的所有語言。

 

 



