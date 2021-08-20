---
description: Msitran.exe 使用 MsiDatabaseGenerateTransform、MsiCreateTransformSummaryInfo 和 MsiDatabaseApplyTransform 來產生或套用轉換檔案。此工具僅適用于 Windows Installer 開發人員的 Windows SDK 元件。
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09803623024bb593897411a5e852aa953335c31fd88f9e2e1922b89b53e9abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944266"
---
# <a name="msitranexe"></a>Msitran.exe

Msitran.exe 使用 [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)、 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)和 [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) 來產生或套用轉換檔案。

此工具僅適用于[Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

## <a name="syntax"></a>Syntax

使用下列語法來產生轉換。

**msitran.exe-g** *{base db} {ref db} {轉換檔案名} \[ {錯誤條件/驗證條件} \]*

使用下列語法來套用轉換

**msitran.exe-a** *{轉換} {資料庫} \[ {錯誤條件} \]*

## <a name="command-line-options"></a>命令列選項

Msitran.exe 會使用下列不區分大小寫的命令列選項。 斜線分隔符號也可以用來取代虛線。



| 選項 | 描述            |
|--------|------------------------|
| -g     | 轉換產生。  |
| -a     | 轉換應用程式。 |



 

套用轉換時，可能會隱藏下列錯誤。 若要隱藏錯誤，請在 {error 條件} 引數中包含適當的字元。 以-g 指定的條件會放置在轉換的摘要資訊中，但在使用-a 來套用轉換時不會使用。 如需詳細資訊，請參閱 [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)。



| 選項 | 隱藏的錯誤           |
|--------|----------------------------|
| a      | 加入現有的資料列。          |
| b      | 刪除不存在的資料列。   |
| c      | 加入現有的資料表。        |
| d      | 刪除非現有的資料表。 |
| e      | 修改現有的資料列。       |
| f      | 變更字碼頁。           |



 

下列驗證條件可用來指出何時可以將轉換套用至封裝。 您可以使用-g 來指定這些條件，但不能指定-a。



| 選項 | 驗證條件                                  |
|--------|-------------------------------------------------------|
| g      | 檢查升級程式碼。                                   |
| l      | 檢查語言。                                       |
| p      | 檢查平臺。                                       |
| r      | 檢查產品。                                        |
| s      | 僅檢查主要版本。                             |
| t      | 僅檢查主要和次要版本。                  |
| u      | 檢查主要、次要和升級版本。             |
| v      | 應用 < 基底資料庫版本的資料庫版本。  |
| w      | 應用 <的資料庫版本 = 基底資料庫版本。 |
| x      | 套用的資料庫版本 = 基底資料庫版本。     |
| y      | 應用 >的資料庫版本 = 基底資料庫版本。 |
| z      | 應用 > 基底資料庫版本的資料庫版本。  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows安裝程式開發工具](windows-installer-development-tools.md)
</dt> <dt>

[資料庫轉換](database-transforms.md)
</dt> <dt>

[自訂轉換範例](a-customization-transform-example.md)
</dt> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



