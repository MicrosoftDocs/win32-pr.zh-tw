---
title: 生成
description: 此系列中每個程式碼範例的 makefile 都是一般 Microsoft Win32 makefile，而且是要從命令提示字元視窗建立。
ms.assetid: f9944069-b536-4ae2-8411-f02c3a78978c
keywords:
- Makefile 結構化儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a15fef5818c28986232e8c2a648f43bdc096832f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311582"
---
# <a name="makefiles"></a>生成

此系列中每個程式碼範例的 makefile 都是一般 Microsoft Win32 makefile，而且是要從命令提示字元視窗建立。 它們會假設 Microsoft 編譯器和連結器工具，而且可能需要進行一些修改才能與其他工具搭配使用。 大部分的編譯器/連結器命令列參數都是由 Win32 中定義的宏指定，也就是平臺軟體發展工具組 (SDK) 隨附的檔案。

Makeall.bat 檔案，以及每個個別的程式碼範例 makefile，都支援下表所列的常見選項，以便從 [命令提示字元] 視窗用來控制組建的本質。



| Nmake 調用        | Makeall 調用          | 效果                       |
|-------------------------|-----------------------------|------------------------------|
| **Nmake**               | **makeall**                 | 使用 debug 資訊編譯。     |
| **nmake** **nodebug = 1** | **makeall** **"nodebug = 1"** | 編譯而不含 debug 資訊。  |
| **nmake** **設定檔 = 1** | **makeall** **"profile = 1"** | 使用程式碼剖析資訊進行編譯。 |
| **nmake** **微調 = 1**    | **makeall** **"微調 = 1"**    | 使用工作集調諧器資訊。 |
| **nmake** **unicode = 1** | **makeall** **"unicode = 1"** | 針對 Unicode 編譯。         |
| **nmake** **清除**     | **makeall** **clean**       | 刪除暫存二進位檔。   |
| **nmake** **cleanall**  | **makeall** **cleanall**    | 刪除所有產生的檔案。  |



 

針對 Makeall.bat 調用，您必須擁有引號，如下所示。 **Nodebug**、**設定檔** 和 **微調** 選項都是互斥的：您只能針對指定的編譯/連結，使用其中一個（或無）。 若要編譯範例以使用 Unicode 字串執行，請使用 **"Unicode = 1"** 選項。 預設值是針對傳統的 ANSI 字串支援進行編譯，因為您接著可以在任何32位的 Windows 作業系統上執行。 您可以在 Windows Server 2003 和更新版本以及 Windows 2000 和更新版本上，自由編譯和執行，或不使用 Unicode。 請注意，APPUTIL 一律會使用與其他程式碼範例相同的選項進行編譯，您可能會另外進行編譯。 這對 **"unicode = 1"** 選項而言更是如此。

您可以使用已安裝的32位 c + + 整合式開發環境 (IDE) 使用提供的一般 makefile 來建立範例。 若要這樣做，您必須在 IDE 中，將一般 makefile 處理為「外部」 makefile。 提供的 makefile 需要 Microsoft NMAKE 相容的建立公用程式。

大部分的 c + + Ide 可以將這些 makefile 辨識為外部，但仍提供許多 IDE 的編輯-組建-debug 的優點。 例如，在 Microsoft Visual Studio 97 或更新版本中，您可以使用 [檔案] 功能表 [開啟工作區] 選項來產生工作區，方法是開啟適當命名的複製 (例如程式碼範例 Win32 makefile 的 Exeskel. mak) 。

 

 




