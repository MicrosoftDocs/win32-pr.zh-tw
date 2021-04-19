---
title: 設定 Process-Wide 安全性
description: 有幾種方式可以設定整個進程的安全性。
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969678"
---
# <a name="setting-process-wide-security"></a>設定 Process-Wide 安全性

有幾種方式可以設定整個進程的安全性。 使用 Dcomcnfg.exe 工具的第一種方式是最簡單的，因為它不需要任何程式設計。 第二項技巧提供程式設計人員更多的控制，且需要呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)。 另一種方法是使用 [AppID](appid-key.md) 金鑰，在登錄中設定整個進程的安全性。

如需這些技術的詳細資訊，請參閱下列主題：

-   [使用 DCOMCNFG 設定 Process-Wide 安全性](setting-processwide-security-using-dcomcnfg.md)
-   [使用 CoInitializeSecurity 設定 Process-Wide 安全性](setting-processwide-security-with-coinitializesecurity.md)
-   [透過登錄設定 Process-Wide 安全性](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在介面 Proxy 層級設定安全性](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[設定 COM 應用程式的安全性](setting-security-for-com-applications.md)
</dt> </dl>

 

 




