---
title: 在線上從 CD 安裝
description: 在線上從 CD 安裝
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Windows Media Player 線上商店，在線上從 CD 安裝
- 線上商店，在線上從 CD 安裝
- 輸入1個線上商店，在線上時從 CD 安裝
- 輸入2個線上商店，在線上時從 CD 安裝
- Windows Media Player 線上商店，從 CD 安裝線上
- 線上商店，從 CD 安裝線上
- 輸入1個線上商店，從 CD 安裝線上
- 輸入2個線上商店，從 CD 安裝線上
- Windows Media Player 線上商店，在線上安裝 CD
- 線上商店，在線上安裝 CD
- 輸入1個線上商店，在線上安裝 CD
- 輸入2個線上商店，在線上安裝 CD
- 在線上從 CD 安裝線上商店
- 線上安裝線上商店的 CD
- 線上商店的線上安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd57015e64dece444b1a91afebe3144bee117caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968431"
---
# <a name="installing-from-a-cd-while-online"></a>在線上從 CD 安裝

使用者可以在連線到網際網路時，從 CD 安裝 Windows Media Player。 發生這種情況時，Windows Media Player 安裝程式會尋找 *ServiceInfo* 命令列參數所指定的 ServiceInfo 檔。 如果索引 **鍵** 屬性符合 *DefaultService* 命令列參數，安裝程式會檢查 Install 元素以自訂安裝程式。 安裝程式會使用屬性值， (EULA) 和您的隱私權聲明中顯示您的使用者授權合約，也會將您的 .cab 檔案取出並安裝到使用者的電腦上。 例如，您可以使用這項功能來安裝您的線上商店所需的最新 COM 物件版本。

安裝之後，Windows Media Player 會使用您為 *DefaultService* 命令列參數指定的金鑰名稱來設定初始線上存放區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Install 元素**](install-element.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> <dt>

[**設定初始線上商店**](setting-the-initial-online-store.md)
</dt> <dt>

[**安裝線上商店的命令列參數**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




