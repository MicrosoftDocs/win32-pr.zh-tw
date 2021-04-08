---
title: RAS 安全性主機支援
description: Windows NT 4.0 提供了一種方法，可讓協力廠商 RAS 安全性 DLL 增強內建的 RAS 安全性功能。 Windows 95 未提供此支援。
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- 主機支援，RAS
- 安全性主機支援，RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674027"
---
# <a name="ras-security-host-support"></a>RAS 安全性主機支援

Windows NT 4.0 提供了一種方法，可讓協力廠商 RAS 安全性 DLL 增強內建的 RAS 安全性功能。 Windows 95 未提供此支援。

Windows NT/Windows 2000 RAS 伺服器提供驗證遠端使用者網路存取的安全性機制。 當 RAS 伺服器接收到呼叫時，會針對本機或網域帳戶資料庫驗證使用者的認證。 RAS 也支援回呼安全性，在這種情況下，RAS 伺服器會掛斷，然後再回呼遠端使用者來建立連線。 對於此安全性層級不足的網路，您可以安裝協力廠商 RAS 安全性 DLL。 然後，安全性 DLL 可以從標準使用者帳戶資料庫以外的資料庫讀取安全性資訊，以驗證遠端使用者。

當 RAS 伺服器接收到呼叫時，它會叫用安全性 DLL 來驗證遠端使用者。 RAS 安全性主機支援提供一種機制，讓安全性 DLL 透過遠端電腦上的終端機視窗與遠端使用者進行通訊。 在一般案例中，安全性 DLL 會要求遠端使用者的登入名稱。 然後，DLL 會使用其私用安全性資料庫來制定傳送至遠端終端機機的挑戰。 例如，這項挑戰可能是使用者必須提供做為 cardkey 讀者輸入的程式碼。 Cardkey 讀取器接著會顯示遠端使用者在終端機視窗中輸入的回應。 然後，安全性 DLL 會根據使用者在私用安全性資料庫中的資訊來驗證回應。

如果安全性 DLL 驗證遠端使用者，RAS 伺服器會執行自己的驗證。 如此可確保 RAS 安全性一律會驗證遠端使用者，即使已安裝可授與存取權給所有使用者的安全性 DLL 也是如此。

> [!Note]  
> Windows NT/Windows 2000 目前僅針對非同步數據機連線提供 RAS 安全性主機支援;不支援其他類型的連線（例如乙太網路 (）不是數據機連線) 、VPN (也不是數據機連線) ，或 (為同步) 的 ISDN。

 

 

 




