---
title: 設定 COM 應用程式的安全性
description: 設定 COM 應用程式的安全性
ms.assetid: 5b615007-e04b-41be-872c-20e0ea818ff1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1168fcd8d9119226efe9469eabef617e6400cfbc8d1202a4833ac3e4d0ea20d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104306"
---
# <a name="setting-security-for-com-applications"></a>設定 COM 應用程式的安全性

有數種方式可協助您控制應用程式的安全性。 您可以變更電腦的預設安全性設定，而電腦上的所有應用程式都會使用這些設定來提供自己的安全性值。 您可以使用 Dcomcnfg.exe 或藉由呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)來設定特定進程的安全性。 您也可以透過程式設計的方式控制介面 proxy 層級的安全性設定。

下列主題提供說明如何設定安全性的程式：

-   [修改電腦的安全性預設值](modifying-the-security-defaults-for-a-computer.md)
-   [設定 Process-Wide 安全性](setting-processwide-security.md)
-   [在介面 Proxy 層級設定安全性](setting-security-at-the-interface-proxy-level.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 




