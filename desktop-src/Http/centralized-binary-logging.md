---
title: 集中式二進位記錄
description: 集中式二進位記錄是一種可在伺服器會話上啟用的伺服器端記錄類型。
ms.assetid: 957a7bc4-9db3-4153-b0a9-e53b3cc514c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bc7bdc6f7a5fce78ff66e58b4c50eac36be3f9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314962"
---
# <a name="centralized-binary-logging"></a>集中式二進位記錄

集中式二進位記錄是一種可在伺服器會話上啟用的伺服器端記錄類型。 集中式二進位記錄功能可做為伺服器會話下建立之所有 URL 群組的集中式記錄，並允許伺服器會話下的所有 URL 群組將二進位、未格式化的記錄資料傳送至單一記錄檔。 這種類型的記錄只能在伺服器會話上啟用;無法在 URL 群組上啟用。

## <a name="when-to-use-centralized-binary-logging"></a>使用集中式二進位記錄的時機

當伺服器會話中有多個 URL 群組時，為個別的 URL 群組建立數百個格式化記錄檔，並將記錄資料寫入磁片的程式，可快速取用寶貴的 CPU 和記憶體資源，進而建立效能和擴充性問題。 集中式二進位記錄可將用於記錄的系統資源量降至最低，同時也能為需要的組織提供詳細的記錄資料。

集中式二進位記錄是一種伺服器會話屬性，在啟用時，會為伺服器會話下的所有 URL 群組設定記錄。 啟用集中式二進位記錄時，無法針對個別的 URL 群組錄製或格式化資料。 集中式二進位記錄記錄檔 ( ibl) 副檔名。 此副檔名可確保文字公用程式不會嘗試開啟並讀取中央二進位記錄記錄檔。

## <a name="extracting-data-from-the-centralized-binary-log-file"></a>從集中式二進位記錄檔解壓縮資料

執行下列步驟以從原始記錄檔中取出資料：

-   建立工具，從原始檔案尋找並解壓縮您想要的資料，並將資料轉換成格式化的文字。 您可以在 MSDN 上的 IIS 6.0 軟體發展工具組中，查看標頭檔和記錄檔格式描述。
-   使用記錄剖析器工具，從原始檔案解壓縮資料。 記錄剖析器工具及其隨附的使用者檔包含在 IIS 6.0 資源套件工具中。

## <a name="centralized-binary-logging-file-format"></a>集中式二進位記錄檔案格式

原始的集中式二進位記錄記錄檔是由固定長度的記錄或包含字串識別碼的索引記錄所組成。 出現索引記錄的原因是，為了盡可能記錄最多的資訊，可變長度的字串欄位會被數位識別碼（索引）取代，這會將可變長度的字串對應至記錄的識別碼。

未經處理的記錄檔不是人類可讀取的檔案，而且無法使用大部分可用的記錄分析器來讀取。 若要從原始記錄檔將資料解壓縮，您可以建立工具來尋找並解壓縮資料，然後將它轉換成格式化的文字。

如需詳細資訊，請參閱 Microsoft TechNet 上的 [集中式二進位記錄](/previous-versions/windows/it-pro/windows-server-2003/cc758733(v=ws.10)) 。

 

 