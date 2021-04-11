---
description: 訊息驗證碼 (MAC) 用來偵測訊息篡改和偽造。
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Schannel 中的訊息驗證碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93939c0c4b4550ad0c24f8e6ef0e0b8bf9f1b07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194068"
---
# <a name="message-authentication-codes-in-schannel"></a>Schannel 中的訊息驗證碼

[*訊息驗證碼*](../secgloss/m-gly.md) (MAC) 用來偵測訊息篡改和偽造。 訊息的傳送者會使用傳送者和收件者所共用的 [*工作階段金鑰*](../secgloss/s-gly.md)，加密訊息內文的單向 [*雜湊*](../secgloss/h-gly.md)來建立 MAC。 MAC 會附加至傳送給收件者的訊息。 訊息收件者會使用共用工作階段金鑰和訊息內文再次產生 MAC，並將產生的 MAC 與接收自傳送者的 MAC 進行比較。 如果兩者相同，則寄件者必須有共用工作階段金鑰，而且訊息在傳輸時尚未改變。

在安全通道通訊協定中，用來產生 MAC 的演算法是由傳送者和收件者所使用的 [加密套件](cipher-suites-in-schannel.md) 所決定。

 

 
