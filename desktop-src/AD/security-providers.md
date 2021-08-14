---
title: 安全性提供者
description: 安全性支援提供者介面 (SSPI) 支援相互驗證，並且會直接透過 sspi 上的 SSPI Api 和服務（包括 RPC）來公開。
ms.assetid: 3aa64aa1-c707-489f-a0a3-08bf6ac151ec
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3685ad95b5e339853be947170bb0a8681a376d8d2f34368534d02b3b0cbdf4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183653"
---
# <a name="security-providers"></a>安全性提供者

安全性支援提供者介面 (SSPI) 支援相互驗證，並且會直接透過 sspi 上的 SSPI Api 和服務（包括 RPC）來公開。

並非所有可供 SSPI 使用的安全性封裝都支援相互驗證。 若要取得相互驗證，應用程式必須要求相互驗證，以及支援的安全性封裝。 例如，在[具有 SCP 的 Windows 通訊端服務中進行相互驗證](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md)的程式碼範例，會在 Secur32.dll （隨附于 Windows 2000）中使用 "negotiate" 套件。

 

 




