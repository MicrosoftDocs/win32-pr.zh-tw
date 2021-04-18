---
description: Microsoft 基底 DSS 和 Diffie-Hellman 密碼編譯提供者所支援的演算法。
ms.assetid: 8db1c7cb-41e0-470b-b927-989da4c09324
title: PROV_DSS_DH 提供者演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098625153d4d447d7290827dcad44a6c78f55561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978194"
---
# <a name="prov_dss_dh-provider-algorithms"></a>>PROV \_ DSS \_ DH 提供者演算法

下表列出 Microsoft 基底 DSS 和 Diffie-Hellman 密碼編譯提供者所支援的演算法。



| 演算法識別碼      | 描述                                 | 註解                                                                                                        |
|-------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| CALG \_ MD5         | MD5 雜湊演算法。                      | 僅提供給雜湊之用。                                                                                      |
| CALG \_ SHA         | SHA 雜湊演算法。                      | 必須用於 DSS 簽章。                                                                                |
| CALG \_ SHA1        | 與 CALG \_ SHA 相同。                          | 不加評論。                                                                                                     |
| CALG \_ DSS \_ SIGN   | DSS 公開/私密金鑰簽章演算法。 | 金鑰長度：可設定為64位遞增的512位到1024位。 預設金鑰長度：1024位。<br/> |
| CALG \_ DH \_ SF      | 儲存和轉寄 D-H 金鑰交換。         | 金鑰長度：可設定為8位遞增的384位到512位。 預設金鑰長度：512位。<br/>      |
| CALG \_ DH \_ EPHEM   | 暫時的 D-H 金鑰交換。                 | 金鑰長度：可設定為8位遞增的384位到512位。 預設金鑰長度：512位。<br/>      |
| CALG \_ CYLINK \_ MEK | DES 金鑰的40位變異。              | 金鑰長度：40位。                                                                                            |



 

 

 




