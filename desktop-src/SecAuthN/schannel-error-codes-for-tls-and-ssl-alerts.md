---
description: 從傳輸層安全性 (TLS) 或安全通訊端層 (SSL) 通訊協定收到對應的警示時，Schannel 會傳回下列錯誤訊息。
ms.assetid: 0a6ac61d-a00c-4fc8-a995-d25d17e405df
title: TLS 和 SSL 警示的 Schannel 錯誤碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9fdba202e63d212fc85f0c02eb5ac9dc20db047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944131"
---
# <a name="schannel-error-codes-for-tls-and-ssl-alerts"></a>TLS 和 SSL 警示的 Schannel 錯誤碼

從 [*傳輸層安全性*](../secgloss/t-gly.md) (TLS) 或 [*安全通訊端層*](../secgloss/s-gly.md) (SSL) 通訊協定收到對應的警示時， [*Schannel*](../secgloss/s-gly.md)會傳回下列錯誤訊息。 錯誤訊息是在 Winerror.h 中定義。



| TLS 或 SSL 警示                                           | Schannel 錯誤碼                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------|
| SSL3 \_ 警示未 \_ 預期的 \_ 訊息<br/> 10<br/>  | SEC \_ E 不 \_ 合法的 \_ 訊息<br/> 0x80090326<br/>             |
| TLS1 \_ 警示不 \_ 正確的 \_ 記錄 \_ MAC<br/> 20<br/>     | 秒 \_ E \_ 修改的訊息 \_<br/> 0x8009030F<br/>             |
| TLS1 \_ 警示 \_ 解密 \_ 失敗<br/> 21<br/>   | 秒 \_ E \_ 解密 \_ 失敗<br/> 0x80090330<br/>             |
| TLS1 \_ 警示 \_ 記錄 \_ 溢位<br/> 22<br/>     | SEC \_ E 不 \_ 合法的 \_ 訊息<br/> 0x80090326<br/>             |
| SSL3 \_ 警示 \_ 解壓縮 \_ 失敗<br/> 30<br/>  | 秒 \_ E \_ 修改的訊息 \_<br/> 0x8009030F<br/>             |
| SSL3 \_ 警示 \_ 交握 \_ 失敗<br/> 40<br/>   | SEC \_ E 不 \_ 合法的 \_ 訊息<br/> 0x80090326<br/>             |
| TLS1 \_ 警示 \_ 錯誤的 \_ 憑證<br/> 42<br/>     | SEC \_ E \_ CERT \_ 未知<br/> 0x80090327<br/>                |
| TLS1 \_ 警示 \_ 不支援的憑證 \_<br/> 43<br/>    | SEC \_ E \_ CERT \_ 未知<br/> 0x80090327<br/>                |
| TLS1 \_ 警示 \_ 憑證已 \_ 撤銷<br/> 44<br/> | CRYPT \_ E 已 \_ 撤銷<br/> 0x80092010<br/>                    |
| TLS1 \_ 警示 \_ 憑證已 \_ 過期<br/> 45<br/> | SEC \_ E 憑證已 \_ \_ 過期<br/> 0x80090328<br/>                |
| TLS1 \_ 警示 \_ 憑證 \_ 不明<br/> 46<br/> | SEC \_ E \_ CERT \_ 未知<br/> 0x80090327<br/>                |
| SSL3 \_ 警示不 \_ 合法的 \_ 參數<br/>                 | SEC \_ E 不 \_ 合法的 \_ 訊息<br/> 0x80090326<br/>             |
| TLS1 \_ 警示 \_ 不明的 \_ CA<br/> 48<br/>          | SEC \_ E 未 \_ 受信任的 \_ 根<br/> 0x80090325<br/>              |
| TLS1 \_ \_ 拒絕存取 \_ 警示<br/> 49<br/>       | 秒 \_ E \_ 登入 \_ 拒絕<br/> 0x8009030C<br/>                |
| TLS1 \_ 警示 \_ 解碼 \_ 錯誤<br/> 50<br/>        | SEC \_ E 不 \_ 合法的 \_ 訊息<br/> 0x80090326<br/>             |
| TLS1 \_ 警示 \_ 解密 \_ 錯誤<br/> 51<br/>       | 秒 \_ E \_ 解密 \_ 失敗<br/> 0x80090330<br/>             |
| TLS1 \_ 警示 \_ 匯出 \_ 限制<br/> 60<br/>  | SEC \_ E 不 \_ 合法的 \_ 訊息<br/> 0x80090326<br/>             |
| TLS1 \_ 警示 \_ 通訊協定 \_ 版本<br/> 70<br/>    | SEC \_ E \_ 不支援的函式 \_<br/> 0x80090302<br/>        |
| TLS1 \_ ALERT \_ INSUFFIENT \_ SECURITY<br/> 71<br/> | SEC \_ E \_ 演算法 \_ 不相符<br/> 0x80090331<br/>          |
| TLS1 \_ 警示 \_ 內部 \_ 錯誤<br/> 80<br/>      | SEC \_ E \_ 內部 \_ 錯誤<br/> 0x80090304<br/>              |
| TLS1 \_ 警示 \_ 使用者 \_ 已取消<br/> 90<br/>       | SEC \_ E 未 \_ 完成的 \_ 內容 \_ 刪除<br/> 0x80090333<br/> |
| TLS1 \_ 警示 \_ 不會重新 \_ 協商<br/> 100<br/>   | SEC \_ E 不 \_ 合法的 \_ 訊息<br/> 0x80090326<br/>             |
| TLS1 \_ 警示 \_ 不支援的 \_ EXT<br/> 110<br/>    | SEC \_ E 不 \_ 合法的 \_ 訊息<br/> 0x80090326<br/>             |
| 預設<br/>                                         | SEC \_ E 不 \_ 合法的 \_ 訊息<br/> 0x80090326<br/>             |



 

 

 
