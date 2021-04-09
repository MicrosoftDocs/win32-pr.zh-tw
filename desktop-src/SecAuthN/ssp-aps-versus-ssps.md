---
description: 說明 SSP/Ap 與 Ssp 之間的差異。
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/Ap 與 Ssp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d089a27da6b0ab5d4228af924f738f27a1d728
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944881"
---
# <a name="sspaps-vs-ssps"></a>SSP/Ap 與 Ssp

[*安全性套件*](../secgloss/s-gly.md) 會以下列其中一種動態連結程式庫類型部署 (dll) ：

-   [SSP/Ap](#sspaps-vs-ssps)
-   [Ssp](#sspaps-vs-ssps)

安全性套件是否位於安全性支援提供者/[*驗證套件*](../secgloss/a-gly.md) (SSP/AP) 或 [*安全性支援提供者*](../secgloss/s-gly.md) (ssp) DLL 是由它所提供的安全性服務類型以及它需要與 [*本地安全機構*](../secgloss/l-gly.md) (LSA) 整合的程度決定。 這些差異也會決定在自訂安全性封裝中實作為的 API。

## <a name="sspaps"></a>SSP/Ap

SSP/AP 是包含一或多個 [*安全性套件*](../secgloss/s-gly.md) 的 DLL，可以作為用戶端/伺服器應用程式的 SSP，以及做為登入應用程式的 [驗證套件](authentication-packages.md) 。 為了在這兩個角色中運作，SSP/Ap 會在系統啟動時載入至 LSA 進程空間，也可以載入至用戶端/伺服器應用程式進程。

自訂 SSP/AP 安全性套件必須同時執行 [由使用者模式 SSP/ap 所執行](authentication-functions.md)的函式，以及 [由 SSP/ap 所執行](authentication-functions.md)的函式。 這些函式的使用方式可以利用 LSA 支援函式來提供先進的安全性功能，例如權杖建立、 [*補充*](../secgloss/s-gly.md) 認證支援和傳遞驗證。

如果自訂的 SSP/AP 安全性套件提供完整範圍的訊息 [*完整性*](../secgloss/i-gly.md) 和隱私權功能，也會執行 [由使用者模式 SSP/ap 所執行](authentication-functions.md)的函式。

## <a name="ssps"></a>Ssp

SSP 是一個包含一或多個安全性套件的 DLL，可為用戶端/伺服器應用程式提供已驗證的連線、訊息完整性和訊息加密服務。 Ssp (SSPI) 函式來實行 [安全性支援提供者介面](sspi.md) 。 應用程式可以直接呼叫 SSPI 函式，以存取 SSP 中的安全性套件。 Ssp 會載入至用戶端和伺服器進程;它們不會與 LSA 整合。

 

 
