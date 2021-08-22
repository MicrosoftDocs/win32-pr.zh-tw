---
title: 使用 DCOMCNFG 啟用 COM 安全性
description: Dcomcnfg.exe 提供使用者介面，可供修改登錄中的某些設定。
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6161cf7418e7eab705203df51710e789ad2ef7d6843051dd35399fb8388f27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678688"
---
# <a name="enabling-com-security-using-dcomcnfg"></a>使用 DCOMCNFG 啟用 COM 安全性

Dcomcnfg.exe 提供使用者介面，可供修改登錄中的某些設定。 藉由使用 Dcomcnfg.exe，您可以在整個電腦或整個進程的基礎上啟用安全性。 您可以啟用特定電腦的安全性，如此一來，當處理常式未提供本身的安全性設定時，您可以透過程式設計方式或透過登錄值，將會使用 Dcomcnfg.exe 設定的值。 或者，您可以使用 Dcomcnfg.exe 來啟用特定應用程式的安全性。

啟用安全性時，有兩個主要工作要完成：

-   設定不是 None 的驗證層級。
-   設定許可權，包括啟動和存取權限。

完成這些工作所採取的步驟取決於您是要為整個電腦還是只針對特定應用程式啟用安全性。 此外，您可能會想要設定電腦或應用程式的其他值。

> [!Note]  
> 您必須是系統管理員，才能執行 Dcomcnfg.exe。

 

下列主題提供有關如何使用 Dcomcnfg.exe 設定安全性的逐步程式：

-   [使用 DCOMCNFG 設定 System-Wide 安全性](setting-machine-wide-security-using-dcomcnfg.md)
-   [使用 DCOMCNFG 設定 Processwide 安全性](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的安全性](security-in-com.md)
</dt> <dt>

[關閉安全性](turning-off-security.md)
</dt> </dl>

 

 




