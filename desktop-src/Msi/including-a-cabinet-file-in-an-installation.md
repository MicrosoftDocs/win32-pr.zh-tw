---
description: 本節說明如何在安裝中包含封包檔。 如需詳細資訊，請參閱使用封包和壓縮的來源。
ms.assetid: 17ea7f76-90b2-48fb-8187-64dc6d294443
title: 在安裝中包含封包檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0970d87b8b219e1558c6b3f1daf78a6a01100a7bc41f9ae1dad51a25048b46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787338"
---
# <a name="including-a-cabinet-file-in-an-installation"></a>在安裝中包含封包檔

本節說明如何在安裝中包含封包檔。 如需詳細資訊，請參閱 [使用封包和壓縮的來源](using-cabinets-and-compressed-sources.md)。

**若要在安裝套件中包含封包檔**

1.  使用封包建立工具，將來源檔案壓縮成封包檔。 請參閱封 [包](cabinet-files.md)檔。
2.  封包檔必須位於 .msi 檔案內部的資料流程中，或位於 [目錄資料表](directory-table.md)所指定來源樹狀結構根目錄的個別封包檔中。
3.  判斷來源是否為壓縮類型，或是同時具有未壓縮和壓縮檔案的混合類型。 請參閱 [壓縮和未壓縮的來源](compressed-and-uncompressed-sources.md)。 視來源影像的類型而定，設定 [ [**字數統計摘要**](word-count-summary.md) ] 屬性的壓縮或未壓縮旗標位。
4.  針對封包中的每個檔案，將記錄新增至檔案 [資料表](file-table.md) 。 在 [檔案] 欄中輸入檔案索引鍵，其完全符合封包中檔案的檔案索引鍵。 檔案索引鍵會區分大小寫。 檔案資料表和封包中的檔案安裝順序也必須相同。 檔案順序是由 [順序] 資料行中的序號所指定。 若要抵達封包中第一個檔案的序號，請執行下列動作。 在 [DiskID] 資料行中，尋找 [媒體資料表](media-table.md) 中具有最大值的現有記錄。 此記錄的 LastSequence 欄位會提供媒體上所使用的最後一個檔案序號。 在 File 資料表中，將新封包的第一個檔案指派為大於此值的序號。 依照封包檔中的相同順序，將序號指派給其餘所有檔案。 如需其餘記錄欄位的說明，請參閱檔案 [資料表](file-table.md)。
5.  將記錄加入至封包的 [媒體資料表](media-table.md) 。 在新記錄的 DiskID 欄位中，指定大於資料表中現有最大 DiskID 值的值。 將封包的名稱放入 [封包] 欄位中。 這個名稱必須是封 [包](cabinet.md) 資料類型的形式。 \#如果封包是儲存在 .msi 檔案中的資料流程，請在名稱前面加上數位記號 ""。 請注意，如果封包是資料流程，封包的名稱會區分大小寫。 如果封包是個別的檔案，則檔案的名稱不區分大小寫。
6.  藉由檢查已更新檔案資料表的 [順序] 資料行，在新的封包中判斷最大的檔案序號。 在 [媒體] 資料表的新記錄的 [LastSequence] 欄位中輸入大於此值的值。 如需其餘記錄欄位的說明，請參閱 [媒體資料表](media-table.md)。
7.  您可以使用工具（例如 Msidb.exe）或使用安裝程式的 [資料庫](database-functions.md)函式，將封包檔儲存在安裝套件中。 下列四個步驟說明如何使用資料庫函數，從程式新增封包。
8.  若要從程式將封包新增至安裝套件，請使用 [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)在資料庫的 [ \_ 資料流程資料表](-streams-table.md)上開啟一個 view。
9.  使用 [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) 將資料流程資料表的 [名稱] 資料行，設定 \_ 為在 [Media 資料表](media-table.md)的 [封包] 資料行中顯示的名稱。 省略數位記號： \# 。
10. 使用 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) 將資料流程資料表的資料行設定 \_ 為封包的資料。
11. 使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 來更新資料流程資料表中的記錄 \_ 。
12. 若要使用 Msidb.exe 將封包檔 Mycab.cab 新增至名為 Mydatabase.msi 的安裝套件，請使用下列命令列： Msidb.exe-d mydatabase.msi-a mycab.cab。 在此情況下，媒體資料表的 [封包] 資料行應該包含 [字串： \#mycab.cab]。

 

 



