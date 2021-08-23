---
description: 如果這兩個檔案都沒有版本號碼，則 Windows Installer 會使用下列流程圖所示的邏輯，判斷是否要取代所有已安裝的檔案屬於元件。
ms.assetid: 82cb0d96-f49f-408e-a8c6-a0d1ee9af8c7
title: 這兩個檔案都沒有版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68a6d74a26a810f2ddb33e1c13b2ed7b372a75d5b262a8b6d8d7ecaca1c99f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065930"
---
# <a name="neither-file-has-a-version"></a>這兩個檔案都沒有版本

如果要安裝之元件的金鑰檔 (copy-A) 與已安裝在目標位置中的檔案具有相同的名稱 (copy-B) ，安裝程式會比較兩個檔案的版本號碼、日期和語言。

如果這兩個檔案都沒有版本號碼，則安裝程式會使用下列流程圖所示的邏輯，判斷是否要取代所有已安裝的檔案屬於元件。 因為安裝程式只會安裝整個元件，所以如果已取代已安裝的金鑰檔，則會取代所有元件的檔案。

請注意，下圖說明預設檔案 [版本控制規則](file-versioning-rules.md)，可以藉由設定 [**REINSTALLMODE**](reinstallmode.md) 屬性來覆寫這些規則。 **REINSTALLMODE** 屬性的預設值為 "omus reinstall"。

![當兩個檔案都沒有版本號碼時，預設檔案版本控制規則](images/waiflow2.png)

請參閱 [取代現有](replacing-existing-files.md)檔案的預設檔案版本控制範例。

-   [這兩個檔案都有版本](both-files-have-a-version.md)
-   [這兩個檔案都沒有具有檔案雜湊檢查的版本](neither-file-has-a-version-with-file-hash-check.md)
-   [一個檔案有版本](one-file-has-a-version.md)

 

 



