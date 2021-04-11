---
description: 使用 Microsoft Digest 的 HTTP 驗證需要三個輸入緩衝區才能產生挑戰回應。 下表摘要說明這些緩衝區。
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: 摘要挑戰回應的輸入緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112189"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a>摘要挑戰回應的輸入緩衝區

使用 Microsoft Digest 的 HTTP 驗證需要三個輸入緩衝區才能產生挑戰回應。 下表摘要說明這些緩衝區。



| 緩衝區編號 | 包含                                                                                                                                             | 緩衝區類型                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| 0             | 從伺服器收到的挑戰                                                                                                                   | 之 SECBUFFER \_ TOKEN                                            |
| 1             | HTTP 方法                                                                                                                                          | 之 SECBUFFER \_ 參數                                           |
| 2             | H (實體)                                                                                                                                             | 之 SECBUFFER \_ 參數                                           |
| 3             | 目標伺服器 (SPN) 的 [*服務主體名稱*](../secgloss/s-gly.md) 。 | **之 secbuffer \_目標 \_ 主機** \| **之 SECBUFFER \_ READONLY**      |
| 4             | 通道系結 token 值                                                                                                                        | **之 secbuffer \_通道 \_** 系結 \| **之 SECBUFFER \_ READONLY** |



 

緩衝區零包含從伺服器收到的摘要挑戰，以回應存取保護之資源的初始要求。

緩衝區1包含方法的字串標記法，例如 "GET" 或 "POST"。 方法會在 A2 的計算中使用，如 [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)中所述。

緩衝區2是訊息的實體主體的 [*MD5*](../secgloss/m-gly.md) 雜湊，如 RFC 2617 中所述。

當搭配通道系結使用 Digest 時，緩衝區3會在 UTF-8 格式中包含目標伺服器的 SPN。

當搭配通道系結使用 Digest 時，緩衝區4包含通道系結 token 值。

## <a name="input-buffers-for-sasl"></a>SASL 的輸入緩衝區

僅提供緩衝區零。 為了與其他 Ssp 相容，您可以呼叫 [**InitializeSecurityCoNtext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) ，而不會有有效的伺服器挑戰。 在此情況下， *pInput* 參數應該設定為 **Null**。

 

 
