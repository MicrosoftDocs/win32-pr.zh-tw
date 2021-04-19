---
description: 為安裝應用程式撰寫 INF 檔案時，您也應該參考 INF 檔案格式，該檔案格式記載于 INF 檔案和 INF 檔案區段的一般指導方針，以及 Microsoft Windows 2000 驅動程式開發工具組的指示詞。
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: 撰寫 INF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73807f919a016f414a248f47e53f27d5b079bb33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970395"
---
# <a name="authoring-an-inf-file"></a>撰寫 INF 檔案

為安裝應用程式撰寫 INF 檔案時，您也應該參考 INF 檔案格式，該檔案格式記載于 INF 檔案和 *inf 檔案區段* 的 *一般指導方針*，以及 Microsoft Windows 2000 驅動程式開發工具組的指示詞。

針對安裝應用程式撰寫 INF 檔案時，請遵守下列規則。

-   每個 INF 檔案中都需要 **版本** 區段。
-   區段的開頭必須是以方括弧括住的區段名稱 (\[ \]) 。
-   **DestinationDirs**、 **SourceDisksFiles**、 **SourceDisksNames**、 **Strings** 和 **Version** 區段的名稱必須與區段型別相同。 例如，使用 \[ DestinationDirs \] 。 作者可以指定其他類型的區段名稱。
-   **SourceDisksNames** 和 **SourceDisksFiles** 區段的名稱可以附加平臺特定的尾碼。 例如，若要顯示 Intel 特定的 **SourceDisksNames** 區段，請使用 \[ SourceDisksNames。 \] 如果安裝函式找到符合使用者平臺的平臺特定 **SourceDisksNames** 和 **SourceDisksFiles** 區段，則這些函式會使用平臺特定區段。 否則，安裝程式函數會使用非尾碼的 **SourceDisksNames** 和 **SourceDisksFiles** 區段。 安裝函式可以用程式設計的方式決定使用者的系統。 請參閱 [INF SourceDisksNames 和 SourceDisksFiles 章節範例](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md)。
-   值可以使用%*strkey*% 形式以可替換的字串表示。 若要在字串中使用% 字元，請使用%%。 Strkey 必須定義在 INF 檔案的 **字串** 區段中。

 

 



