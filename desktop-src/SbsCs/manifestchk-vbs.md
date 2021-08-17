---
description: VBScript 檔案 Manifestchk.vbs 是 Microsoft Windows 軟體開發套件 (SDK) 所提供的驗證工具，可驗證應用程式和組件資訊清單檔。
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686843d1b4ab099d44a33b715f65564a12834f54ed6e8f62310df0aedbe53de1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142051"
---
# <a name="manifestchkvbs"></a>Manifestchk.vbs

VBScript 檔案 Manifestchk.vbs 是 Microsoft Windows 軟體開發套件 (SDK) 所提供的驗證工具，可驗證應用程式和組件資訊清單檔。

執行此範例需要 Windows 腳本主機。 如需 Windows 腳本主機的詳細資訊，請參閱 Windows SDK 的 Windows 腳本主機一節。 Windows腳本主機實際上是兩個主機。 CScript.exe 是可讓您從命令提示字元執行腳本的版本。 CScript.exe 提供命令列參數來設定腳本屬性。

命令列格式如下所示：

**Cscript//nologo manifestchk.vbs/s：** *\[ drive： \] \[ path \] schemafilename* **/m：** *\[ drive： \] \[ path \] manifestfilename* **\[ /q \] /t：** *選項*

下表說明為 Manifestchk.vbs 定義的旗標。



| 旗標 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /s   | 指定要對其驗證資訊清單的資訊清單架構檔案名。 請參閱 [資訊清單檔案架構](manifest-file-schema.md)中的架構。                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| /m   | 指定要驗證的資訊清單檔案名。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| /q   | 抑制主控台的所有輸出。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| /t   | 指定資訊清單檔的類型。 有效值為： AM 驗證[組件資訊清單](assembly-manifests.md)或[應用程式指令](application-manifests.md)清單的[資訊清單檔架構](manifest-file-schema.md)<br/> 電腦驗證[發行者設定檔](publisher-configuration-files.md)的[發行者設定檔架構](publisher-configuration-file-schema.md)<br/> AC 驗證 [應用程式佈建檔](application-configuration-files.md)的應用程式佈建檔架構。<br/> |



 

如果未指定/q 旗標，Manifestchk.vbs 會顯示檔案中第一個錯誤的詳細資訊，並顯示一則訊息，指出驗證程式是否成功。

此公用程式會檢查下列各項：

-   有效的命令列。
-   已安裝 MSXML 第3版。
-   資訊清單會使用格式正確的 XML。
-   資訊清單同意提供的架構。 請注意，Manifestchk.vbs 只會根據提供的架構中指定的內容來驗證資訊清單檔。 如需資訊清單架構的範例，請參閱 [資訊清單檔案架構](manifest-file-schema.md)。

如果驗證程式成功，Cscript.exe 會傳回值0，如果失敗，則傳回1。 如果命令列引數中有錯誤，則會傳回2。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[並存元件開發工具](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




