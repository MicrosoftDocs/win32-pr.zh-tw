---
description: 下列各節中的流程圖說明當所安裝元件的金鑰檔與已安裝在目標位置中的檔案同名時，所使用的預設檔案版本控制規則。
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: 預設檔案版本控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850244"
---
# <a name="default-file-versioning"></a>預設檔案版本控制

下列各節中的流程圖說明當所安裝元件的金鑰檔與已安裝在目標位置中的檔案同名時，所使用的預設檔案版本控制規則。 [取代現有](replacing-existing-files.md)的檔案也會說明預設檔案版本控制。

請注意，使用 Windows Installer 時，可使用檔案雜湊來優化檔案的複製。 如需詳細資訊，請參閱 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) 和 [MsiFileHash 資料表](msifilehash-table.md)。 MsiFileHash 資料表只能搭配未建立版本檔使用。

-   [這兩個檔案都有版本](both-files-have-a-version.md)
-   [這兩個檔案都沒有版本](neither-file-has-a-version.md)
-   [這兩個檔案都沒有具有檔案雜湊檢查的版本](neither-file-has-a-version-with-file-hash-check.md)
-   [一個檔案有版本](one-file-has-a-version.md)

 

 



