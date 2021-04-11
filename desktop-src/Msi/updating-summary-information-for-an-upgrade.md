---
description: 升級套件的封裝程式碼必須與原始產品的封裝碼變更。
ms.assetid: 786e864a-93e0-4ea6-adab-e87afbdd6ac2
title: 更新升級的摘要資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9bee3457b9ebbe0264d569f37d8ed5a3e372df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027445"
---
# <a name="updating-summary-information-for-an-upgrade"></a>更新升級的摘要資訊

升級套件的封裝程式碼必須與原始產品的封裝碼變更。 封裝程式碼會儲存在 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性中。 如需詳細資訊，請參閱 [套件代碼](package-codes.md)。 使用 Msiinfo.exe 或其他編輯器來變更 MNP2001.msi 的摘要資訊，如 [新增摘要資訊](adding-summary-information.md)中所述。



| 摘要資訊屬性                                                   | 資料                                                                             | 備註                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**範本**](template-summary.md) (平臺和語言) <br/>         | ; 1033                                                                            | 資料庫使用的平臺和語言。 如果 [**範本**](template-summary.md) 摘要屬性值中缺少平臺規格，則安裝程式會假設採用 Intel 架構。 資料庫中的 [**ProductLanguage**](productlanguage.md) 屬性通常用於這個摘要屬性。 範例的語言識別項表示封裝使用的是美國英文。 |
|  (套件程式碼) 的 [**修訂編號**](revision-number-summary.md)<br/>    | {A0EC5348-1D02-4FF6-93F5-61BD7AC1772E}                                           | 這是可唯一識別範例套件的封裝程式碼 [GUID](guid.md) 。 如果您重現此範例，請使用 GUIDGEN 之類的公用程式，為您的套件產生不同的 GUID。 GUIDGEN 的結果包含小寫字元，請注意，您必須將有效封裝程式碼的所有小寫字元變更為大寫。                                                     |
| [**頁面計數**](page-count-summary.md) (最小安裝程式版本) <br/> | 200                                                                              | 針對最低 Windows Installer 版本2.0，這個屬性應該設定為整數200。                                                                                                                                                                                                                                                                                                         |
| 來源) 的 [**字數統計**](word-count-summary.md) (類型<br/>            | 0                                                                                | 封裝的全域來源類型是完整的檔案名和未壓縮的名稱。 如需詳細資訊，請參閱 [壓縮和未壓縮的來源](compressed-and-uncompressed-sources.md) ，以及檔案 [資料表](file-table.md)之屬性資料行的描述。                                                                                                                               |
| [**標題**](title-summary.md)                                                 | 安裝資料庫                                                            | 通知使用者此資料庫適用于安裝，而不是轉換或修補程式。                                                                                                                                                                                                                                                                                                          |
| [**主體**](subject-summary.md)                                             | MNP2001                                                                          | 檔案瀏覽器可以將此資料庫顯示為與此資料庫一起安裝的產品。                                                                                                                                                                                                                                                                                                                    |
| [**關鍵字**](keywords-summary.md)                                           | 安裝程式、MSI、資料庫                                                         | 能夠搜尋關鍵字的檔案瀏覽器可以搜尋這些字。                                                                                                                                                                                                                                                                                                                      |
| [**作者**](author-summary.md)                                               | Microsoft Corporation                                                            | 產品製造商的名稱。                                                                                                                                                                                                                                                                                                                                                                  |
| [**註解**](comments-summary.md)                                           | 此安裝程式資料庫包含安裝 [記事本] 所需的邏輯和資料。 | 通知使用者此資料庫的用途。                                                                                                                                                                                                                                                                                                                                                    |
| [**正在建立應用程式**](creating-application-summary.md)                   | 逆 戟 鯨                                                                             | 用來建立安裝資料庫的應用程式。 此範例會將 Orca 資料庫編輯器指定為範例。                                                                                                                                                                                                                                                                                   |
| [**安全性**](security-summary.md)                                           | 0                                                                                | 範例資料庫是不受限制的讀寫。                                                                                                                                                                                                                                                                                                                                                      |



 

[繼續](validating-an-installation-upgrade.md)

 

 




