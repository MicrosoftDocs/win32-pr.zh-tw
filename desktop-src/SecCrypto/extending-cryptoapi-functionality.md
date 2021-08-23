---
description: 密碼編譯和安全通訊的未來無法輕易地預測。
ms.assetid: 41c1758d-1213-47a6-81d5-7755b41c3007
title: 擴充 CryptoAPI 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1c2d45ec9e0262843bb8e0ff7d7d727785a63c2d37467b321e7cc5664388cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007025"
---
# <a name="extending-cryptoapi-functionality"></a>擴充 CryptoAPI 功能

[*密碼*](../secgloss/c-gly.md)編譯和安全通訊的未來無法輕易地預測。 可能會出現新的憑證類型，不同的憑證延伸可能會發現常見的使用方式，而且可能會引進新的訊息類型。 基於這個原因，擴充性是關鍵 [*CryptoAPI*](../secgloss/c-gly.md) 函數設計的一部分。

下列各節顯示使用 Oid 擴充 CryptoAPI 函式的總覽。



| 主題                                                                              | 目錄                                                                                                                            |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [OID 總覽](oid-overview.md)                                                   | OID 基本概念。                                                                                                           |
| [建立新功能](creating-the-new-functionality.md)               | 建立 Oid 和函式，以擴充現有 Api 的使用。                                                                     |
| [註冊新功能](registering-the-new-functionality.md)         | 設定新的 OID 相關函數。                                                                                               |
| [安裝新功能](installing-the-new-functionality.md)           | 將 OID 函數安裝至記憶體，以改善效能。                                                                          |
| [擴充 CertOpenStore 功能](extending-certopenstore-functionality.md) | 使用可安裝或已註冊的憑證存放區提供者功能來擴充 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) 功能。 |



 

 

 
