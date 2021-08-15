---
description: WMI 所實行的技術，可讓多個當地語系化版本的相同類別儲存在存放庫中。
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: 當地語系化 WMI 類別資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3784128c48282d05620faf470217b195b26614d81b5b847e7a7a8ad6b9252f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131210"
---
# <a name="localizing-wmi-class-information"></a>當地語系化 WMI 類別資訊

WMI 所實行的技術，可讓多個當地語系化版本的相同類別儲存在存放庫中。

類別定義會分成下列版本：

-   僅包含基本類別定義的非語言相關版本。
-   包含當地語系化資訊的特定語言版本，例如地區設定特有的屬性描述。

特定語言的類別定義會儲存在包含非語言相關基本類別定義的命名空間底下的子命名空間中。

當您針對特定地區設定要求當地語系化的類別定義時，WMI 會結合基本類別定義和當地語系化類別資訊來形成完整的當地語系化類別。 您可以在連線至 WMI 時指定地區設定，並設定指出您要當地語系化資訊的旗標，以取得 WMI 類別的當地語系化版本。 WMI 接著會合並語言中立的資訊，以及類別定義的語言特定版本，以形成當地語系化的類別。

包含當地語系化資訊的 WMI 類別會以 **修訂** 辨識符號標示，並稱為修改過的類別;類別支援當地語系化的資訊（如果有此限定詞的話）。 您可以藉由檢查另一個稱為 [**地區**](swbemobjectpath-locale.md)設定的辨識符號，判斷類別已當地語系化的地區設定。 地區設定辨識符號包含當地語系化識別碼 (Windows 識別地區設定的 LCID) 。 例如，美式英文的地區設定是0x409。 如果修改過的類別中的辨識符號包含當地語系化的資訊，它就會包含 **修改** 過的辨識符號類別。

WMI 當地語系化包含下列工作：

-   [建立當地語系化的類別定義](creating-localized-class-definitions.md)
-   [編譯當地語系化的 MOF 檔案](compiling-localized-mof-files.md)
-   [當地語系化屬性值](localizing-property-values.md)
-   [正在抓取修改過的類別](retrieving-amended-classes.md)

如需詳細資訊，請參閱修改過的 [類別考慮](amended-class-considerations.md)。

 

 



