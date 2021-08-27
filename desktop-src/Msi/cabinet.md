---
description: 您必須在媒體資料表的 [封包] 資料行中使用 [封包] 資料類型。
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: 內閣
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16acfd031a6580f898d4cb464a15c895644995a2499a62ac79c9adeced8ccec1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105358"
---
# <a name="cabinet"></a>內閣

您必須在 [媒體資料表](media-table.md)的 [封包] 資料行中使用 [封包] 資料類型。

如果封包名稱前面加上數位記號，封包會以資料流程的形式儲存在封裝內。 後面的字元字串 \# 是此資料流程的 [識別碼](identifier.md) 。 請注意，如果封包是儲存為數據流，封包的名稱會區分大小寫。

如果封包名稱前面沒有數位記號 \# ，封包會儲存在 [目錄資料表](directory-table.md)所指定來源樹狀結構的根目錄中的個別檔案中。 封包檔必須使用由八個字元名稱、句號和三個字元副檔名組成的簡短檔案名語法。 封包資料類型無法針對檔案名使用簡短的 \| longname 語法。 如果封包檔儲存為個別的檔案，封包檔的名稱不會區分大小寫。

為了節省磁碟空間，安裝程式會在快取使用者電腦上的安裝封裝之前，先移除任何內嵌于 .msi 檔案中的封包。

請參閱 [在安裝中包含封包](including-a-cabinet-file-in-an-installation.md)檔。

 

 



