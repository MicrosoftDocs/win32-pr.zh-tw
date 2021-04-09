---
description: 如果這兩個檔案都有版本號碼，Windows Installer 會使用下列流程圖所示的邏輯來判斷是否要取代屬於元件的所有已安裝檔案。
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: 這兩個檔案都有版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb52c7333e5455d40475c9f845643535b271d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848946"
---
# <a name="both-files-have-a-version"></a>這兩個檔案都有版本

如果要安裝之元件的金鑰檔 (copy-A) 與已安裝在目標位置中的檔案具有相同的名稱 (copy-B) ，安裝程式會比較兩個檔案的版本號碼和語言。

如果這兩個檔案都有版本號碼，則安裝程式會使用下列流程圖所示的邏輯，判斷是否要取代所有已安裝的檔案屬於元件。 因為安裝程式只會安裝整個元件，所以如果已取代已安裝的金鑰檔，則會取代所有元件的檔案。

請注意，下圖說明預設檔案 [版本控制規則](file-versioning-rules.md)，可以藉由設定 [**REINSTALLMODE**](reinstallmode.md) 屬性來覆寫這些規則。 **REINSTALLMODE** 屬性的預設值為 "omus reinstall"。

![當兩個檔案都有相同的名稱或版本號碼時，預設檔案版本控制規則](images/waiflow1.png)

上圖也可以搭配未指定語言的檔案使用。 如果複製-A 具有指定的語言，而複製-B 沒有指定的語言，則會以複製-B 取代複製-B。 如果 copy A 和 copy-B 都未指定任何語言，則不會取代 copy B。

請參閱 [取代現有](replacing-existing-files.md)檔案的預設檔案版本控制範例。

-   [這兩個檔案都沒有版本](neither-file-has-a-version.md)
-   [這兩個檔案都沒有具有檔案雜湊檢查的版本](neither-file-has-a-version-with-file-hash-check.md)
-   [一個檔案有版本](one-file-has-a-version.md)

 

 



