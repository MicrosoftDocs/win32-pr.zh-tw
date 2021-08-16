---
title: 離線時安裝
description: 離線時安裝
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Windows Media Player 線上商店，離線安裝
- 線上商店，離線安裝
- 輸入1個線上商店，離線安裝
- 輸入2個線上商店，離線安裝
- Windows Media Player 線上商店、離線安裝
- 線上商店、離線安裝
- 輸入1個線上商店、離線安裝
- 輸入2個線上商店、離線安裝
- 離線時安裝線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3051aca9634bc2c53950baa783bcf62fc6861c616facd9dc563d70d011c2459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135501"
---
# <a name="installing-while-offline"></a>離線時安裝

使用者可以在未連線到網際網路的情況下安裝 Windows Media Player。 發生這種情況時，Windows Media Player 安裝程式會尋找 *ServiceInfo* 命令列參數所指定的 ServiceInfo.xml 檔。 如果索引 **鍵** 屬性符合 *DefaultService* 命令列參數，安裝程式會將下列元素的資訊套用至 Windows Media Player：

-   友好. 線上商店的易記名稱會顯示在 Windows Media Player 的使用者介面中。
-   色彩。 指定的色彩會套用至工作列和按鈕。
-   ServiceTask1、ServiceTask2 和 ServiceTask3。 已設定 ButtonText 和 ButtonTip 子項目。 未設定 URL 屬性。 當使用者連線到網際網路，且 Windows Media Player 以正常方式抓取其線上商店清單時，就會設定 URL。
-   影像。 MenuURL 和 ServiceLargeURL 屬性已設定。 這些 Url 必須指向您使用 file://通訊協定安裝在使用者硬碟上的映射。

當使用者嘗試觀看線上商店時，Windows Media Player 會顯示一則訊息，告知使用者需要網際網路連線。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Color 元素**](color-element.md)
</dt> <dt>

[**FriendlyName 元素**](friendlyname-element.md)
</dt> <dt>

[**Image 元素**](image-element.md)
</dt> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**ServiceInfo 元素**](serviceinfo-element.md)
</dt> <dt>

[**ServiceTask1 元素**](servicetask1-element.md)
</dt> <dt>

[**ServiceTask2 元素**](servicetask2-element.md)
</dt> <dt>

[**ServiceTask3 元素**](servicetask3-element.md)
</dt> <dt>

[**設定初始線上商店**](setting-the-initial-online-store.md)
</dt> <dt>

[**安裝線上商店的命令列參數**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




