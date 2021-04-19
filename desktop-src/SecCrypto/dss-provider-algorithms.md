---
description: 下表列出 Microsoft DSS 密碼編譯提供者所支援的演算法。
ms.assetid: 2a7aecf8-e242-4087-83ee-aaa637a9ec71
title: DSS 提供者演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0bd9346da7a9ab1490e2646d9d2559c07359b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987530"
---
# <a name="dss-provider-algorithms"></a>DSS 提供者演算法

下表列出 Microsoft DSS 密碼編譯提供者所支援的演算法。



| 演算法識別碼    | 描述                                 | 註解                                                                                                        |
|-----------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| CALG \_ MD5       | MD5 雜湊演算法。                      | 僅提供給雜湊之用。                                                                                      |
| CALG \_ SHA       | SHA 雜湊演算法。                      | 必須用於 DSS 簽章。                                                                                |
| CALG \_ SHA1      | 與 CALG \_ SHA 相同。                          | 不加評論。                                                                                                     |
| CALG \_ DSS \_ SIGN | DSS 公開/私密金鑰簽章演算法。 | 金鑰長度：可設定為64位遞增的512位到1024位。 預設金鑰長度：1024位。<br/> |



 

 

 




