---
description: 傳輸層安全性 (TLS) 記錄通訊協定會使用在交握期間建立的金鑰來保護應用程式資料。
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: TLS 記錄通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a53d41ad73dc9e1338f0cbff1bec5d6cd6a55e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984229"
---
# <a name="tls-record-protocol"></a>TLS 記錄通訊協定

[*傳輸層安全性*](../secgloss/t-gly.md) (TLS) 記錄通訊協定會使用在 [交握](tls-handshake-protocol.md)期間建立的金鑰來保護應用程式資料。 記錄通訊協定負責保護應用程式資料，並驗證其 [*完整性*](../secgloss/i-gly.md) 和來源。 它會管理下列各項：

-   將外寄訊息分割成可管理的區塊，並目的地重組傳入訊息。
-   壓縮外寄區塊和解壓縮連入區塊 (選擇性) 。
-   將 [*訊息驗證碼*](../secgloss/m-gly.md) (MAC) 套用至外寄訊息，以及使用 MAC 來驗證傳入訊息。
-   加密外寄訊息和解密傳入訊息。

當記錄通訊協定完成時，傳出的加密資料會向下傳遞至傳輸控制通訊協定 (TCP) 層以進行傳輸。

 

 
