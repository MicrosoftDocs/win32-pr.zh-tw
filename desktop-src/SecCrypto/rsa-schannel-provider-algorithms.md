---
description: Microsoft RSA/Schannel 密碼編譯提供者可能會支援演算法。
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: RSA/Schannel 提供者演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dd7f22e6353544690c14091d29af50fec94dc3b65d6733aefc2a9fa8387bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900508"
---
# <a name="rsaschannel-provider-algorithms"></a>RSA/Schannel 提供者演算法

Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md)密碼編譯提供者可能支援下列演算法。



| 演算法識別碼    | 描述                                                                                                                         | 註解                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| CALG \_ RSA \_ KEYX | RSA 公開金鑰 [*金鑰交換演算法*](../secgloss/k-gly.md) | 金鑰長度：可設定為8位遞增的384位到16384位。 預設金鑰長度：1024位。<br/> |
| CALG \_ MD5       | MD5 雜湊演算法。                                                                                                              | 僅提供給雜湊之用。                                                                                      |
| CALG \_ SHA       | SHA 雜湊演算法。                                                                                                              | 必須用於 DSS 簽章。                                                                                |
| CALG \_ RC2       | RC2 區塊加密演算法。                                                                                                     | 金鑰長度：40至88位                                                                                       |
| CALG \_ RC4       | RC4 資料流程加密演算法。                                                                                                    | 金鑰長度：40至88位                                                                                       |



 

 

 
