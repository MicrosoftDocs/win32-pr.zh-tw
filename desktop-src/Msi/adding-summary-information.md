---
description: 下列摘要資訊屬性必須在每個安裝封裝中定義，使用軟體工具來存取摘要資訊資料流程的 Istream 介面。
ms.assetid: 9775959f-5ab2-43cd-8cc8-9d81945b4ec6
title: 新增摘要資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dc43ba8df737fb4d7c30998ec6c9581376df6ef6274140e68ec767e3a416f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328578"
---
# <a name="adding-summary-information"></a>新增摘要資訊

下列摘要資訊屬性必須在每個安裝封裝中定義，使用軟體工具來存取 [摘要資訊資料流程](summary-information-stream.md)的 **Istream** 介面。 例如，您可以使用 Windows Installer SDK 提供的工具 Msiinfo.exe 來設定這些屬性。 如果未設定這些屬性，封裝將不會傳遞 [套件驗證](package-validation.md)。



| 摘要資訊屬性                                                   | 資料                                   | 備註                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**範本**](template-summary.md) (平臺和語言) <br/>         | ; 1033                                  | 資料庫使用的平臺和語言。 如果 [**範本**](template-summary.md) 摘要屬性值中缺少平臺規格，則安裝程式會假設採用 Intel 架構。 資料庫中的 [**ProductLanguage**](productlanguage.md) 屬性通常用於這個摘要屬性。 範例的語言識別項表示封裝使用的是美國英文。 |
|  (套件程式碼) 的 [**修訂編號**](revision-number-summary.md)<br/>    | {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3} | 這是可唯一識別範例套件的封裝程式碼 [GUID](guid.md) 。 如果您重現此範例，請使用 GUIDGEN 之類的公用程式，為您的套件產生不同的 GUID。 GUIDGEN 的結果包含小寫字元，請注意，您必須將有效封裝程式碼的所有小寫字元變更為大寫。 請參閱 [套件代碼](package-codes.md)。             |
| [**頁面計數**](page-count-summary.md) (最小安裝程式版本) <br/> | 200                                    | 針對最小 Windows Installer 2.0，這個屬性應該設定為整數200。                                                                                                                                                                                                                                                                                                                 |
| 來源) 的 [**字數統計**](word-count-summary.md) (類型<br/>            | 0                                      | 封裝的全域來源類型是完整的檔案名和未壓縮的名稱。 如需詳細資訊，請參閱 [壓縮和未壓縮的來源](compressed-and-uncompressed-sources.md) ，以及檔案 [資料表](file-table.md) 之屬性資料行的描述。                                                                                                                                |



 

其餘的摘要資訊資料流程屬性不是必要的，但應該針對 MNP2000.msi 範例設定。



| 摘要資訊屬性                                 | 資料                                                                             | 備註                                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**標題**](title-summary.md)                               | 安裝資料庫                                                            | 通知使用者此資料庫適用于安裝，而不是轉換或修補程式。                        |
| [**主體**](subject-summary.md)                           | MNP2000                                                                          | 檔案瀏覽器可以將此資料庫顯示為與此資料庫一起安裝的產品。                                  |
| [**關鍵字**](keywords-summary.md)                         | 安裝程式、MSI、資料庫                                                         | 能夠搜尋關鍵字的檔案瀏覽器可以搜尋這些字。                                    |
| [**作者**](author-summary.md)                             | Microsoft Corporation                                                            | 產品製造商的名稱。                                                                                |
| [**註解**](comments-summary.md)                         | 此安裝程式資料庫包含安裝記事本所需的邏輯和資料。 | 通知使用者此資料庫的用途。                                                                  |
| [**正在建立應用程式**](creating-application-summary.md) | 逆 戟 鯨                                                                             | 用來建立安裝資料庫的應用程式。 此範例會將 Orca 資料庫編輯器指定為範例。 |
| [**安全性**](security-summary.md)                         | 0                                                                                | 範例資料庫是不受限制的讀寫。                                                                    |



 

您不需要將 [**最後一次儲存**](last-saved-by-summary.md)的時間、 [**上次儲存的時間/日期**](last-saved-time-date-summary.md)、 [**建立時間/日期**](create-time-date-summary.md)、 [**最後列印**](last-printed-summary.md)、 [**字元計數**](character-count-summary.md)和 [**字碼頁**](codepage-summary.md) 摘要屬性設定為完成此範例資料庫。 此範例依賴資料庫編輯工具來設定和更新這些選用的屬性。

例如，若要使用 MsiInfo 將摘要資訊新增至範例，請變更至包含資料庫的目錄，然後使用下列命令列。 請勿重複使用範例套件識別碼，如下所示。

**Msiinfo.exe MNP2000.msi-T "安裝資料庫"-J 主旨-A "Microsoft Corporation"-K "安裝程式，MSI，資料庫"-O "此安裝程式資料庫包含安裝記事本所需的邏輯和資料。"-P; 1033-V {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3}-G 200-W 0-N Orca-U 0**

如需摘要資訊的詳細資訊，請參閱 [關於摘要](about-the-summary-information-stream.md)資訊資料流程、 [使用摘要資訊資料流程](using-the-summary-information-stream.md)，以及 [摘要資訊資料流程參考](summary-information-stream-reference.md)。

請參閱 [摘要資訊資料流程屬性集](summary-information-stream-property-set.md) ，以取得所有摘要資訊屬性的完整清單，以及其描述的 [摘要屬性描述](summary-property-descriptions.md) 。

[繼續](importing-the-user-interface.md)

 

 




