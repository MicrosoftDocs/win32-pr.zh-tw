---
description: 檔案雜湊適用于 Windows Installer。 如需詳細資訊，請參閱 MsiGetFileHash 和 MsiFileHash 資料表。 MsiFileHash 資料表只能搭配未建立版本檔使用。
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: 這兩個檔案都沒有具有檔案雜湊檢查的版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb874cdc29c56f34be2d4ec8604c2436892744e44581258ec237f515600f9024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869191"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a>這兩個檔案都沒有具有檔案雜湊檢查的版本

檔案雜湊適用于 Windows Installer。 如需詳細資訊，請參閱 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) 和 [MsiFileHash 資料表](msifilehash-table.md)。 MsiFileHash 資料表只能搭配未建立版本檔使用。

如果要安裝之元件的金鑰檔 (copy-A) 與已安裝在目標位置中的檔案具有相同的名稱 (copy-B) ，安裝程式會比較兩個檔案的版本號碼、日期和語言。

如果這兩個檔案都沒有版本號碼，則安裝程式會使用下列流程圖所示的邏輯，判斷是否要取代所有已安裝的檔案屬於元件。 因為安裝程式只會安裝整個元件，所以如果已取代已安裝的金鑰檔，則會取代所有元件的檔案。

請注意，下圖說明預設檔案 [版本控制規則](file-versioning-rules.md)，可以藉由設定 [**REINSTALLMODE**](reinstallmode.md) 屬性來覆寫這些規則。 **REINSTALLMODE** 屬性的預設值為 "omus reinstall"。

![reinstallmode 屬性設定覆寫時的預設檔案版本控制規則](images/waiflow2b.png)

請參閱 [取代現有](replacing-existing-files.md)檔案的預設檔案版本控制範例。

-   [這兩個檔案都有版本](both-files-have-a-version.md)
-   [這兩個檔案都沒有版本](neither-file-has-a-version.md)
-   [一個檔案有版本](one-file-has-a-version.md)

 

 



