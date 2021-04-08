---
description: 原始產品 MNP2000 的協同功能檔案包含 Concert.txt 檔案中的錯誤。
ms.assetid: 4289bd0c-bdf3-4747-9287-94f737ce4f5c
title: 規劃小型更新修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f15f3667c6a18ab7a71e86997091bd76d4b15577
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103853516"
---
# <a name="planning-a-small-update-patch"></a>規劃小型更新修補程式

原始產品 MNP2000 的協同功能檔案包含 Concert.txt 檔案中的錯誤。 因為 Windows Installer 用於安裝和設定應用程式，所以應用程式的次要修正可能會藉由安裝小型更新修補程式套件來處理。 [小型更新](small-updates.md)會變更一或多個太小的應用程式檔，以變更產品代碼。 下列範例會示範如何建立 Windows Installer 修補程式套件，以套用小型更新並提供 MNP2000 產品的快速修正。

若要建立 small update，請先取得 MNP2000 產品的完整未壓縮映射，其中包含 Concert.txt 中的錯誤。 映射必須包含 MNP2000.msi 以及 [規劃安裝](planning-the-installation.md)中所述的所有來源檔案。 在以下討論中，這稱為目標映射。 目標映射必須完整解壓縮，因為修補程式建立程式無法針對壓縮于封包中的檔案產生二進位修補程式。 將目標映射的 .msi 檔案和所有來源檔案放在名為 Target 的資料夾中。

接下來，使用固定的 Concert.txt 檔案取得 MNP2000 產品的完整未壓縮映射。 這在下列討論中稱為升級的映射。 使用安裝資料庫編輯工具（例如 Orca）來更新 .msi 檔案。 例如，如果已更正 Concert.txt 的大小小於原始的大小，請務必在升級映射之 File 資料表的 [FileSize] 欄位中輸入新的大小。 請注意，由於套件已變更，您必須在 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性中指派新的封裝程式碼。 將已升級影像的 .msi 檔案和所有原始程式檔放入名為 [已升級] 的資料夾中。

基於此範例的目的，假設 Concert.txt 檔案的大小變更。 這表示目標和升級資料庫之檔案資料表中的 FileSize 欄位包含不同的資料。

下列檔案 [資料表](file-table.md) 會從目標影像中識別記錄。



| 檔案        | 元件\_ | FileName    | FileSize | 版本 | 語言 | 屬性 | 順序 |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | 演唱會     | Concert.txt | 1000     |         |          | 0          | 1        |



 

下列檔案資料表會從升級的映射中識別記錄。



| 檔案        | 元件\_ | FileName    | FileSize | 版本 | 語言 | 屬性 | 順序 |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | 演唱會     | Concert.txt | 900      |         |          | 0          | 1        |



 

> [!Note]
> 檔案在目標映射和更新的映射的檔案 [資料表](file-table.md) 中必須有相同的索引鍵。 這兩個數據表的 File 資料行中的字串值必須相同。 大寫和小寫也必須相同。
> 
> 遵循 [建立修補程式套件](creating-a-patch-package.md)中所述的指導方針。 請勿使用只有大小寫不同的檔案 [資料表](file-table.md) 索引鍵來撰寫套件，因為 [Msimsp.exe](msimsp-exe.md) 和 [Patchwiz.dll](patchwiz-dll.md) 呼叫 Makecab.exe （不區分大小寫且修補程式產生失敗）。

[繼續](creating-a-patch-creation-properties-file.md)

 

 



