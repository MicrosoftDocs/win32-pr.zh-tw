---
description: Diffie-Hellman 演算法的目的是要讓兩部或多部主機建立和共用相同的秘密加密金鑰，只要透過不安全的網路共用資訊就可以了。
ms.assetid: f89a1268-e364-41ec-a6a8-1f6331dbb787
title: Diffie-hellman/Schannel 提供者演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4fb88e3a50e15a6690340ab3fbcee91da1193a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321032"
---
# <a name="diffie-hellmanschannel-provider-algorithms"></a>Diffie-hellman/Schannel 提供者演算法

Diffie-Hellman 演算法的目的是要讓兩部或多部主機建立和共用相同的秘密加密金鑰，只要透過不安全的網路共用資訊就可以了。 透過網路共用的資訊是以一些常數值和 D-H 公開金鑰的形式呈現。

Microsoft [*diffie-hellman*](../secgloss/d-gly.md) / [*Schannel*](../secgloss/s-gly.md)密碼編譯提供者支援下列演算法。



| 演算法識別碼                  | 描述                                                                                                                                           | 註解                                                                                                   |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| CALG \_ DH \_ SF                  | Diffie-Hellman 儲存和轉寄 [*金鑰交換演算法*](../secgloss/k-gly.md) | 金鑰長度：可設定為8位遞增的384位到512位。 預設金鑰長度：512位。<br/> |
| CALG \_ MD5                     | MD5 雜湊演算法。                                                                                                                                | 僅提供給雜湊之用。                                                                                 |
| CALG \_ DH \_ EPHEM               | 暫時的 D-H 金鑰交換。                                                                                                                           | 金鑰長度：可設定為8位遞增的384位到512位。 預設金鑰長度：512位。<br/> |
| CALG \_ SHA                     | SHA 雜湊演算法。                                                                                                                                | 必須用於 DSS 簽章。                                                                           |
| CALG \_ RC2                     | RC2 區塊加密演算法                                                                                                                        | 金鑰長度：40至88位。                                                                                 |
| CALG \_ RC4                     | RC4 串流加密演算法                                                                                                                       | 金鑰長度：40至88位。                                                                                 |
| CALG \_ CYLINK \_ MEK<br/> | DES 變異加密演算法                                                                                                                      | 金鑰長度：40位。                                                                                       |



 

 

 
