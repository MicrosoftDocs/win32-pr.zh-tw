---
description: 如果只有其中一個檔案有版本號碼，Windows Installer 會使用下列流程圖所示的邏輯來判斷是否要取代屬於元件的所有已安裝檔案。
ms.assetid: 1eda5521-6e23-49b8-9870-f5370def487e
title: 一個檔案有版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417060119f8b13b1545161faa80552c79e8ca9aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114168"
---
# <a name="one-file-has-a-version"></a>一個檔案有版本

如果要安裝之元件的金鑰檔 (copy-A) 與已安裝在目標位置中的檔案具有相同的名稱 (copy-B) ，安裝程式會比較兩個檔案的版本號碼、日期和語言。

如果只有其中一個檔案有版本號碼，則安裝程式會使用下列流程圖所示的邏輯來判斷是否要取代屬於該元件的所有已安裝檔案。 因為安裝程式只會安裝整個元件，所以如果已取代已安裝的金鑰檔，則會取代所有元件的檔案。

請注意，下圖說明預設檔案 [版本控制規則](file-versioning-rules.md)，可以藉由設定 [**REINSTALLMODE**](reinstallmode.md) 屬性來覆寫這些規則。 **REINSTALLMODE** 屬性的預設值為 "omus reinstall"。

![只有一個檔案有版本號碼時的預設檔案版本控制規則](images/waiflow3.png)

請參閱 [取代現有](replacing-existing-files.md)檔案的預設檔案版本控制範例。

-   [這兩個檔案都有版本](both-files-have-a-version.md)
-   [這兩個檔案都沒有版本](neither-file-has-a-version.md)
-   [這兩個檔案都沒有具有檔案雜湊檢查的版本](neither-file-has-a-version-with-file-hash-check.md)

 

 



