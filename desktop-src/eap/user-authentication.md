---
title: 使用者驗證
description: 驗證通訊協定本身可以透過受保護的 EAP (PEAP) 來驗證使用者。
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10de1d08a0daffe7fb415c3eab4ba939afa9387
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "103679247"
---
# <a name="user-authentication"></a>使用者驗證

驗證通訊協定本身可以透過受保護的 EAP (PEAP) 來驗證使用者。 作業系統中內建的驗證提供者有兩種： Windows 網域驗證 (透過目錄服務存取，) 和遠端存取撥入使用者服務 (RADIUS) 。

在 RADIUS 為驗證提供者的情況下，EAP 外掛程式會安裝在 RADIUS 伺服器上，而不是安裝在 (AP) server （例如 RAS 伺服器）的無線存取點上。 AP 伺服器會直接從用戶端將 EAP 封包傳遞給 RADIUS 伺服器上的驗證服務。 AP 伺服器不會處理 EAP 封包中的任何資訊，但它必須接受伺服器端、完整強度 (256 位) PEAP 產生的加密金鑰，才能建立安全的連接。

 

 




