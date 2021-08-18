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
ms.openlocfilehash: 13589d7ba6dea0693acaacb5e0d1f551b4a4f178c4ccb50a1bd8ebb513dda3de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996508"
---
# <a name="installing-from-a-cd-while-online"></a>在線上從 CD 安裝

使用者可以在連線到網際網路時，從 CD 安裝 Windows Media Player。 發生這種情況時，Windows Media Player 安裝程式會尋找 *ServiceInfo* 命令列參數所指定的 ServiceInfo 檔。 如果索引 **鍵** 屬性符合 *DefaultService* 命令列參數，安裝程式會檢查 Install 元素以自訂安裝程式。 使用屬性值時，安裝程式會顯示您的使用者授權合約 (EULA) 和您的隱私權聲明，並同時抓取 .cab 檔案並安裝到使用者的電腦上。 例如，您可以使用這項功能來安裝您的線上商店所需的最新 COM 物件版本。

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

 

 




