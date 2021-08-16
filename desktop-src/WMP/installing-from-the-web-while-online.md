---
title: 在線上時從 Web 安裝
description: 在線上時從 Web 安裝
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Windows Media Player 線上商店，在線上從 Web 安裝
- 線上商店，在線上從 Web 安裝
- 輸入1個線上商店，線上時從 Web 安裝
- 輸入2個線上商店，線上時從 Web 安裝
- Windows Media Player 線上商店，從 Web 安裝線上
- 線上商店，從 Web 安裝線上
- 輸入1個線上商店，從 Web 安裝線上
- 輸入2個線上商店，從 Web 安裝線上
- 在線上從 Web 安裝線上商店
- 線上商店的線上安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801dd9fbee8bff2660a39f6b40e8a5a9e703df00f82be54a7b93c0d200d2ccea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135551"
---
# <a name="installing-from-the-web-while-online"></a>在線上時從 Web 安裝

使用者可以在連線到網際網路時，將 Windows Media Player 安裝為 Web 下載。 在此情況下，Microsoft 可以設定您指定的初始線上商店。

若要以這種方式轉散發 Windows Media Player，請使用下列 URL：

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*版本*&UserLocale =*localID*&Service =*key*

在上述 URL 中，將 *金鑰* 設定為線上商店的金鑰名稱，並將 *localeID* 設定為存放區提供服務的地區設定識別碼。 將 Windows XP 或1上 Windows Media Player 11 的 *版本* 設定為2，Windows Media Player 10。 此 URL 會安裝 Windows Media Player，並將初始使用中的存放區設定為索引 *鍵* 所指定的存放區。

下列範例會顯示安裝 Windows Media Player 11 的 URL，並將 Proseware 設定為初始使用中存放區。 適用于 *localeID* 的409值表示 Proseware 提供美國的服務。

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

如果線上商店的 ServiceInfo 檔包含 Install 元素，Windows Media Player 安裝程式將會自訂安裝程式。 使用屬性值時，安裝程式會顯示您的使用者授權合約 (EULA) 和您的隱私權聲明，並同時抓取 .cab 檔案並安裝到使用者的電腦上。 例如，您可以使用這項功能來安裝您的線上商店所需的最新 COM 物件版本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Install 元素**](install-element.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> <dt>

[**設定初始線上商店**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




