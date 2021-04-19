---
title: Co-Branding 線上商店
description: Co-Branding 線上商店
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player 線上商店、共同品牌
- 線上商店、共同品牌
- 輸入1個線上商店、共同品牌
- 輸入2個線上商店、共同品牌
- 共同品牌的線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cae110d3ed04e864f1b617cb4fd6fcdee3b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969855"
---
# <a name="co-branding-online-stores"></a>Co-Branding 線上商店

未操作音樂商店的個人電腦 Oem 可以與線上商店提供者共同品牌。 Windows Media Player 安裝程式支援 ServiceExtra 命令列參數，可讓硬體 Oem 設定線上商店可用來識別安裝初始線上商店的自訂屬性。

例如，如果名為 Fabrikam 的電腦製作者想要將初始線上商店設定為 Proseware 音樂存放區，它可能會使用下列命令列來安裝 Windows Media Player 10：


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



以這種方式安裝 Windows Media Player 時，播放程式會在每次開啟 Proseware 服務時附加 ServiceExtra 字串。 下列範例顯示 Windows Media Player 會傳送至 Proseware 服務以取得 ServiceInfo 檔的 URL：


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



Proseware online store 接著可以使用查詢字串來判斷 Windows Media Player 安裝的 OEM，並傳回動態產生的 ServiceInfo 檔，指向線上商店的共同品牌版本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**安裝線上商店的命令列參數**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




