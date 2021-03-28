---
description: 這一節的檔案類型和檔案關聯的組織方式如下：
ms.assetid: 45d8b729-1e9d-40c0-8306-9a475262ac40
title: 檔案類型和檔案關聯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf84bbf44475d32768d2359d3723952ada843c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192703"
---
# <a name="file-types-and-file-associations"></a>檔案類型和檔案關聯

這一節的檔案類型和檔案關聯的組織方式如下：

-   [應用程式註冊](app-registration.md)
-   [檔案類型](fa-file-types.md)
-   [如何選擇檔案類型延伸模組](how-to-choose-a-file-type-extension.md)
-   [如何定義檔案類型屬性](how-to-define-file-type-attributes.md)
-   [如何在 [開啟檔案] 對話方塊中加入應用程式](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [如何從非關聯檔案類型的開啟檔案對話方塊中排除應用程式](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)
-   [檔案關聯的運作方式](fa-how-work.md)
-   [依檔案類型或種類的內容視圖](prophand-content-view.md)
-   [如何註冊您的檔案類型的自訂屬性和版面配置](how-to-register-custom-properties-and-layout-for-your-file-type.md)
-   [檔案類型驗證器](file-type-verifier.md)
-   [如何使用檔案類型驗證器](how-to-use-the-file-type-verifier.md)
-   [檔案類型處理常式](fa-file-extensions.md)
-   [程式設計識別碼](fa-progids.md)
-   [如何註冊新應用程式的檔案類型](how-to-register-a-file-type-for-a-new-application.md)
-   [認知類型](fa-perceivedtypes.md)
-   [關聯陣列](fa-associationarray.md)

## <a name="additional-resources"></a>其他資源

-   設定程式存取和電腦預設值 (SPAD) 是 Windows 主控台，可讓具有系統管理許可權的使用者設定電腦預設值，以及隱藏或顯示應用程式。 媒體、郵件、瀏覽器、Messenger 和 JAVA 應用程式都是在 SPAD 中註冊之應用程式的範例。 設定您的預設程式 (SYDP) 是一種 Windows 主控台，它只適用于有限的許可權，並允許使用者設定使用者預設值。 任何應用程式都可以在 SYDP 中註冊。 如需 SPAD 和 SYDP 應用程式註冊的相關資訊，請參閱檔案 [關聯和預設程式的指導方針](appguide-fa-defpro.md)，以及 [設定程式存取和電腦預設值 (SPAD) ](cpl-setprogramaccess.md)。
-   如需相關的概念背景，請參閱 [動詞和檔案關聯的總覽](fa-verbs.md)。
-   若要建立 Shell 資料存放區，請參閱 [執行基本資料夾物件介面](nse-implement.md)。

如需相關的參考檔，請參閱下列主題：

-   若要在 Shell 專案上執行動詞命令，請參閱 [**InvokeVerb**](folderitem-invokeverb.md) 方法。
-   若要取得可在 Shell 專案上執行的動詞集合，請參閱 [**動詞**](folderitem-verbs.md) 方法。
-   若要在指定的檔案上執行作業，請參閱 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 或 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 函數。
-   如需預設感知類型的清單，請參閱 [**認知**](/windows/win32/api/shtypes/ne-shtypes-perceived) 的列舉。
-   若要根據檔案的副檔名抓取檔案的認知型別，請參閱 [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) 函數。

 

 



