---
title: 安裝線上商店的命令列參數
description: 安裝線上商店的命令列參數
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Windows Media Player 線上商店，設定命令列參數
- 線上商店，安裝命令列參數
- 輸入1個線上商店，安裝命令列參數
- 輸入2個線上商店，安裝命令列參數
- 設定命令列參數
- Windows Media Player 線上商店，命令列參數
- 線上商店、命令列參數
- 輸入1個線上商店、命令列參數
- 類型2線上商店，命令列參數
- 命令列參數
- Windows Media Player 線上商店、參數
- 線上商店、參數
- 輸入1個線上商店、參數
- 類型2線上商店、參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0605814d3f8ce5e3015cf67d38f213a6b6f07500
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021381"
---
# <a name="setup-command-line-parameters-for-online-stores"></a>安裝線上商店的命令列參數

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

在 Windows XP 上安裝 Windows Media Player 10 或 Windows Media Player 11 時，您可以附加命令列參數，以指定使用者所看到的第一個線上商店。

語法


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



參數

DefaultService (必要) 

線上商店的索引鍵名稱。 這個值必須符合 ServiceInfo 檔中 **ServiceInfo** 元素之索引 **鍵** 屬性的索引鍵名稱。

ServiceInfo (必要) 

安裝在使用者電腦上之 ServiceInfo 檔的完整路徑。

ServiceExtra (選用) 

Windows Media Player 10 的查詢字串會在線上抓取檔時附加至 ServiceInfo 檔的 URL。

## <a name="remarks"></a>備註

如需使用您的應用程式轉散發 Windows Media Player 軟體的詳細資訊，請參閱轉散發 [Windows Media Player 軟體](redistributing-windows-media-player-software.md)。

當使用者的電腦未連線到網際網路時，會使用本機 ServiceInfo 檔中包含的資訊來設定初始使用中服務的 Windows Media Player。

命令列參數會區分大小寫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**共同品牌的線上商店**](co-branding-online-stores.md)
</dt> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Install 元素**](install-element.md)
</dt> <dt>

[**設定初始線上商店**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




