---
title: 類型1線上商店的測試和生產金鑰
description: 類型1線上商店的測試和生產金鑰
ms.assetid: 1a975c0b-16b8-4da7-8594-316ae34257d0
keywords:
- Windows Media Player 線上商店，測試金鑰
- 線上商店、測試金鑰
- 輸入1個線上商店、測試金鑰
- Windows Media Player 線上商店、生產金鑰
- 線上商店、生產金鑰
- 輸入1個線上商店、生產金鑰
- Windows Media Player 線上商店，ServiceInfo 檔
- 線上商店，ServiceInfo 檔
- 輸入1個線上商店、ServiceInfo 檔
- 測試金鑰
- 生產金鑰
- ServiceInfo 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e8ce8d049df78f186d336079f76eb00eb8bb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372524"
---
# <a name="test-and-production-keys-for-a-type-1-online-store"></a>類型1線上商店的測試和生產金鑰

當您開始開發線上商店時，Microsoft 會為您提供兩個數值金鑰：測試金鑰和生產金鑰。 同時，您必須為 Microsoft 提供兩個 Url：一個指向您的測試 ServiceInfo 檔，另一個指向您的生產 ServiceInfo 檔。

在開發和測試階段中，只有當您的測試金鑰或生產金鑰位於使用者電腦的登錄中時，才會在 Windows Media Player 中看到您的線上商店。 如果您的測試機碼位於登錄中，Windows Media Player 會抓取您的測試 ServiceInfo 檔，指向您的測試存放區的外掛程式、網頁和影像。 如果您的生產金鑰位於登錄中，Windows Media Player 會抓取您的生產 ServiceInfo 檔，其指向外掛程式、網頁和屬於您生產環境存放區的映射。

您可以使用您認為有用的任何方式來使用您的測試和生產存放區。 但一般而言，差別如下：

-   您的測試存放區是您對外掛程式、網頁、影像和服務的其他元件進行每日變更的位置。
-   您的生產環境存放區是您保留服務穩定版本的位置，包括您的外掛程式、網頁、影像和其他元件。

在 Windows Media Player 中發佈您的線上商店之前，Microsoft 必須驗證您的服務是否正確執行。 在驗證階段，Microsoft 會使用您的生產金鑰。 Microsoft 不會在驗證階段使用您的測試金鑰。

當您的生產線上商店成功完成驗證程式時，Microsoft 會發佈您的存放區，這表示您的生產環境存放區會在所有使用者的 Windows Media Player 中顯示，而不只是在登錄中有您實際執行金鑰的使用者。 發佈存放區之後，就不再需要測試和生產金鑰。

> [!Note]  
> 使用者可能會猜測線上商店的測試或生產金鑰，並在開發期間查看您的商店。 在公開發行之前，您應該特別小心公開您想要保留秘密的功能。

 

如需有關如何將生產和測試金鑰放在使用者登錄中的詳細資訊，請參閱 [類型1線上商店的登錄機碼和專案](registry-keys-and-entries-for-a-type-1-online-store.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於類型1線上商店**](about-type-1-online-stores.md)
</dt> </dl>

 

 




