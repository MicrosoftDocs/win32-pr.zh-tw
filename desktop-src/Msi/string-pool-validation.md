---
description: Windows Installer 會將所有資料庫字串儲存在單一的共用字串集區中，以減少資料庫的大小並改善效能。
ms.assetid: b627f3da-3545-4c1a-85b0-d8845fdac621
title: String-Pool 驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e895a9e9032cb0cf5d94b5a8c3c9070c46fe79041dee41e4ea10366043b4af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627358"
---
# <a name="string-pool-validation"></a>String-Pool 驗證

Windows Installer 會將所有資料庫字串儲存在單一的共用字串集區中，以減少資料庫的大小並改善效能。 驗證字串集區的唯一方法是使用 Windows Installer SDK 中找到的 MsiInfo 工具。

字串集區驗證由兩個主要檢查組成：

-   [DBCS 字串測試](#dbcs-string-tests)
-   [參考計數驗證](#reference-count-verification)

## <a name="dbcs-string-tests"></a>DBCS 字串測試

DBCS 字串測試會掃描資料庫中的每個字串是否有兩個準則：適用于標記為中性字碼頁的封裝，如果有任何字元是擴充字元 (大於 127) ，則會標示字串並顯示訊息，指出資料庫的字碼頁是不正確，因為這些字元需要在所有系統上一致地呈現特定的字碼頁。

如果資料庫具有字碼頁，就會掃描每個字串中是否有不正確 DBCS 指標。 如果非中性字元串標示錯誤，字元將無法正確轉譯。  (這種情況最常見的原因，是使用 \_ 資料庫中已有非中性字元串的 ForceCodepage 資料表，強制字碼頁使用特定的值。 ) 請注意，這項檢查要求系統上必須安裝資料庫的字碼頁。

如果有字碼頁問題，使用者可以使用 \_ ForceCodepage 資料表來強制執行資料庫的字碼頁，使其成為適當的值，以修正錯誤。 如需詳細資訊，請參閱 [字碼頁處理](code-page-handling-windows-installer-.md)。

## <a name="reference-count-verification"></a>參考計數驗證

為了確認所有字串的參考計數，會掃描每個資料表中的字串值，並保留每個相異字串的計數，並將結果與資料庫字串集區中的預存參考計數進行比較。

如果有字串參考計數問題，使用者應該立即使用 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)來匯出資料庫的每個資料表、建立新的資料庫，然後使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)將資料表匯入到新的資料庫。 然後，新的資料庫會有與舊資料庫相同的內容，但字串參考計數是正確的。 從具有損毀字串集區的資料庫中新增或刪除資料可能會導致資料庫損毀和資料遺失，因此，快速採取這些步驟是為了避免資料遺失的問題。

重建資料庫時，請記得在新的資料庫中內嵌任何必要的儲存體和資料流程 (查看[ \_ 串流資料表](-streams-table.md)和[ \_ 儲存體資料表](-storages-table.md)) 並留意程式字碼頁面問題。 也請記得設定每個必要的 [摘要資訊資料流程](summary-information-stream.md) 屬性。

 

 



