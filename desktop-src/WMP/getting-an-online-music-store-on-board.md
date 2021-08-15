---
title: 取得面板上的線上音樂商店
description: 取得面板上的線上音樂商店
ms.assetid: f7eff687-9832-41bc-8f3d-a2ab11917eb0
keywords:
- Windows Media Player線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08e618f1eddca3389801d2b6c2d5de1e7a6ee67f7aef593478f4999f69bbd148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390878"
---
# <a name="getting-an-online-music-store-on-board"></a>取得面板上的線上音樂商店

本主題說明將線上數位媒體存放區帶入 Windows Media Player 的流程。 從開始到完成的上執行緒序所需的時間大約是45-60 個工作天。 下表說明「內建」程式的兩個階段。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>階段</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pending</td>
<td><ul>
<li>您會將必要的連絡人資訊、啟動資訊和驗證帳戶傳送給 Microsoft。</li>
<li>Microsoft 會將測試金鑰和生產金鑰傳送給您。</li>
<li>您可以使用 Windows Media Player 來測試您的線上商店。</li>
<li>您將簽署的合約和合約提交給 Microsoft。</li>
</ul></td>
</tr>
<tr class="even">
<td>驗證</td>
<td>Microsoft 會驗證您的線上商店。</td>
</tr>
</tbody>
</table>



 

完成暫止和驗證階段之後，Microsoft 會發佈您的線上商店。

## <a name="pending-stage"></a>暫止階段

擱置階段讓您有機會在 Windows Media Player 中測試您的線上商店。 這也是確保所有必要合約和合約都已簽署的好時機。 若要開始使用，請將下列資訊傳送給 Microsoft，如本主題稍後所定義：

-   連絡人資訊
-   啟動資訊
-   驗證帳戶

收到您的連絡人和啟動資訊後，Microsoft 會將測試金鑰和生產金鑰傳送給您。 將您的測試金鑰新增至登錄並重新啟動播放程式之後，您的線上商店將會出現在播放程式中，而且您可以進行測試。 如需有關如何將測試金鑰放在登錄中的詳細資訊，請參閱 [類型1線上商店的登錄機碼和專案](registry-keys-and-entries-for-a-type-1-online-store.md) ，或 [類型2線上商店的登錄機碼和專案](registry-keys-and-entries-for-a-type-2-online-store.md)。

您應測試線上商店的所有層面，包括其使用者介面和其外掛程式。 在測試過程中，您必須執行 [類型2線上音樂商店驗證測試](validation-tests-for-type-2-online-music-stores.md)中所述的測試。

> [!Note]  
> 類型1存放區必須通過類型2存放區的所有驗證測試，再加上類型1體驗特有的一些其他測試。 如需類型1驗證測試的相關資訊，請聯絡 Windows Media Player 服務虛擬團隊 mpsvctm@microsoft.com 。

 

## <a name="contact-information"></a>連絡資訊

下表顯示 Microsoft 針對您的線上商店所需的連絡人資訊。 填寫 [[連絡人資訊] 表單](contact-information-form-for-an-online-music-store.md)，並將它傳送給 Windows Media Player Services 虛擬團隊 mpsvctm@microsoft.com 。



| Item                     | 描述                                                                               |
|--------------------------|-------------------------------------------------------------------------------------------|
| 商店名稱               | 您存放區的品牌名稱                                                            |
| Provider Name            | 提供者/白卷標公司的名稱 (如果不同)                                |
| 商店地區設定             | Windows 的使用者地區設定 (s) 您的商店必須顯示在                                |
| 商店類別           | 音樂、廣播、電影、電視、體育、新聞、音訊娛樂及/或其他 (請說明)  |
| 購買模型           | 購買、出租、訂用帳戶及/或其他 (請說明)                             |
| 商店語言           |                                                                                           |
| 商店連絡人名稱 (s)     |                                                                                           |
| 將連絡人電子郵件儲存 (s)   |                                                                                           |
|  (s 的 MSFT Passport 帳戶)  | 這是在 Beta 和合作夥伴開發計畫中未來可能的提名。         |
| 交貨位址         | 沒有任何郵政 方塊                                                                             |
| City                     |                                                                                           |
| 狀態                    |                                                                                           |
| 郵遞區號              |                                                                                           |
| 國家/地區           |                                                                                           |
| Telephone                |                                                                                           |
| 傳真                      |                                                                                           |
| 問卷連絡人           | 如果我們在未來與您聯繫此計畫的經驗，是否有問題？        |



 

## <a name="startup-information"></a>啟動資訊

針對您存放區將提供的每個地理區域，為您的測試存放區傳送一組啟動資訊、一組用於生產存放區的啟動資訊，以及一組驗證帳戶。

[線上音樂商店的 [啟動資訊] 表單](startup-information-form-for-an-online-music-store.md)包含兩份 [啟動資訊] 表單和 [驗證帳戶] 表單的一個複本。 填寫表單，然後將其傳送給 Windows Media Player Services 虛擬小組 mpsvctm@microsoft.com 。

下表說明 Microsoft 針對您的線上商店所需要的啟動資訊。



| Item                                                                                                     | 描述                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 服務資訊 XML URL (2048-字元限制)                                                               | Windows Media Player 取得[ServiceInfo XML 檔](serviceinfo-document.md)的 URL。                                                                                                                                         |
| 服務金鑰 (唯一識別碼)                                                                                   | 可唯一識別您的線上商店的字串。 您應該建立一個用於生產環境，另一個用於測試 (例如，"MyStore" 和 "MyStoreTest" ) 。 請注意，服務金鑰與測試金鑰的內容不同。                        |
| 易記名稱 (30 個字元的限制)                                                                        | 顯示在 Windows Media Player 服務選取器中的商店名稱。                                                                                                                                                        |
| 功能表影像 URL (2048-字元限制)                                                                     | Windows Media Player 抓取在服務選取器中顯示的 15 x 15 圖元標誌的 URL。                                                                                                                                 |
| 購買音樂 URL (2048-字元限制) <br/>  (整合式音樂存放區) <br/>                | 播放程式的「購買 CD」和「購物音樂線上」連結所使用的 URL。                                                                                                                                                              |
| 10 ft UI 購買 URL (2048-字元限制) <br/> 僅 (整合式音樂存放區--選擇性) <br/> | 播放程式在 Windows XP Media center Edition 和 Windows Vista 的 Windows Media center 中使用的「購買 CD」和「在線上購物音樂」連結所使用的 URL。                                                                              |
| 商店標誌 (130w x 共30小時) <br/>  (分別附加 PNG 檔案。 ) <br/>                              | 當滑鼠停留在流覽所有影像上時，顯示在工具提示中的商店標誌。 這個標誌必須是 PNG 格式的檔案，且最好是使用 Alpha 混合的檔案，才能調整 Windows Media Player 中的色彩變更。 |
| 流覽-所有影像 (108w x 108h) <br/>  (分別附加 PNG 檔案。 ) <br/>                       | 當滑鼠停留在流覽所有影像上時，出現在工具提示中的簡短描述。                                                                                                                                               |
| 商店描述文字 (110-字元限制)                                                              | 出現在工具提示中的文字會顯示在商店描述文字下方。                                                                                                                                                                        |
|  (45-字元限制) 的超連結文字                                                                  | [流覽所有線上商店] 頁面上顯示的商店標誌。 它必須是 PNG 格式的檔案，且最好是使用 Alpha 混合的檔案，才能調整 Windows Media Player 中的色彩變更。                                           |



 

> [!Note]  
> 108 x 108 圖元流覽-所有影像都是 Windows Media Player 11 和更新版本的需求。

 

> [!Note]  
> 在 Windows Media Player 11 和更新版本中，會忽略 ServiceInfo XML 檔的 ServiceTask2 和 ServiceTask3 元素。 如需 ServiceInfo XML 檔的詳細資訊，請參閱 [ServiceInfo 檔](serviceinfo-document.md)。

 

## <a name="validation-accounts"></a>驗證帳戶

為了完成接下來的驗證階段一節中所述的驗證程式，Microsoft 針對您的線上商店所提供的每一種帳戶類型，都需要五 (5) 驗證帳戶。 例如，如果您提供的帳戶可區別特性和功能，例如 basic 和 premium，則 Microsoft 將需要每個類型5個 (5) 驗證帳戶，總共10個 (10) 帳戶。

將每個驗證帳戶的使用者名稱和密碼傳送至 mpsvctm@microsoft.com 。 此外，也請包含 Microsoft 可聯絡驗證帳戶的人員姓名。 這些帳戶將用於進行中的每月驗證，因此請包含「充電」帳戶的流程。 當線上商店無法提供足夠的購買點數供 Microsoft 驗證所有購買案例時，就會發生最常見的問題之一。 完成上執行緒序之後，帳戶必須維持使用中狀態。

## <a name="validation-stage"></a>驗證階段

在驗證階段，Microsoft 會確認線上商店的主要功能是否正常運作。 針對 (type 1 和 type 2) 的所有商店，Microsoft 會在 [類型2線上音樂商店的驗證測試](validation-tests-for-type-2-online-music-stores.md)中，執行詳細說明的驗證測試。 Microsoft 也會對類型1存放區執行一些額外的驗證測試。 如果您對於類型1存放區的驗證階段有任何問題，請傳送郵件至 mpsvctm@microsoft.com 。

在驗證階段，Microsoft 會進行兩次驗證。 第一個階段適用于您線上商店的候選版 1 (RC1) 。 如果您的存放區通過 RC1 驗證，您應該將其鎖定，且不會進行任何進一步的變更。 即使您的商店通過 RC1 驗證，Microsoft 也會在您的商店上進行第二次驗證。

如果您的存放區未通過 RC1 驗證行程的任何部分，您將會有兩周的時間來建立第二個候選版 (RC2) ，Microsoft 會在 RC2 驗證階段進行驗證。

如果您的存放區未通過 RC2 驗證的任何部分，則必須等到下列啟動。

## <a name="test-and-production-keys"></a>測試和生產金鑰

回想一下，在擱置階段，您傳送了 Microsoft 兩組啟動資訊：一個用於測試存放區，另一個用於您的生產環境存放區。 另外還記得 Microsoft 傳送了兩個金鑰：測試金鑰和生產金鑰。

測試金鑰完全適用于您自己的用途。 當您的測試金鑰位於登錄中時，Windows Media Player 會使用您為測試存放區提交的 ServiceInfo URL。

當您的生產金鑰位於登錄中時，Windows Media Player 會使用您為生產存放區提交的 ServiceInfo URL。 Microsoft 會在驗證階段使用您的生產金鑰。 Microsoft 永遠不會使用您的測試金鑰進行驗證。

當您的商店上線時，Windows Media Player 會使用您為生產存放區提交的 ServiceInfo URL。

一般來說，您的測試存放區應該是您開發服務並進行每日變更的位置。 您的生產環境存放區應該是您保留服務穩定版本的位置。

## <a name="common-on-boarding-problems"></a>常見的上線問題

以下是一些常見的問題，可能會導致您的存放區無法通過驗證測試。

-   無法從測試伺服器轉換到實際執行伺服器。 這會導致許多問題，例如遺失頁面、不正確 IIS 和安全性設定，以及無法再運作的測試帳戶。
-   立即播放區域中的 [購買] 連結 (或 [商店] 連結) 無效。 這可能會導致您的存放區驗證失敗，即使所有其他專案都在運作中也一樣。
-   Microsoft 的驗證小組將會測試數個購買案例，範圍從小型購買到非常大量的購買。 您必須提供充電方式，讓它們作為商店內的取用者。 如果驗證小組沒有足夠的購買點數可驗證所有案例，就無法驗證您的存放區。

如需常見的上線問題以及 Windows Media Player Services 虛擬小組所編譯常見問題的完整清單，請參閱[線上音樂商店的常見內部問題](common-on-boarding-problems-for-online-music-stores.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[線上商店歡迎套件](online-stores-welcome-kit.md)
</dt> </dl>

 

 





