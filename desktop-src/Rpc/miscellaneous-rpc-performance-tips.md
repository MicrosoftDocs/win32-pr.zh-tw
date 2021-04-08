---
title: 其他 RPC 效能秘訣
description: 本節討論開發高效能 RPC 伺服器的其他效能秘訣。 本節提供許多參考 RPC 用戶端的秘訣。 正確開發 RPC 用戶端可讓 RPC 伺服器執行較少的工作。
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b0b43f996cc0a165076f1d7aab1b69e6fb9b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021081"
---
# <a name="miscellaneous-rpc-performance-tips"></a>其他 RPC 效能秘訣

本節討論開發高效能 RPC 伺服器的其他效能秘訣。 本節提供許多參考 RPC 用戶端的秘訣。 正確開發 RPC 用戶端可讓 RPC 伺服器執行較少的工作。

## <a name="use-kerberos"></a>使用 Kerberos

如果使用安全性，請使用 Kerberos。 在伺服器端，Kerberos 不需要存取 KDC。 這會將工作負載從伺服器移至用戶端，以提供更佳的執行伺服器。

## <a name="use-static-identity-tracking"></a>使用靜態身分識別追蹤

如果使用安全性，請嘗試使用靜態身分識別追蹤。 靜態身分識別追蹤在資源使用方面比動態身分識別追蹤更便宜。 如果用戶端身分識別變更，而且伺服器不應留意變更，請使用動態追蹤，而不是為每個身分識別建立不同的系結控制碼。 但是，如果身分識別是一樣的，請確定 RPC 知道這一點，以避免 RPC 每次都會檢查變更的身分識別。

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a>使用 RpcGetAuthorizationCoNtextForClient 函式

如果您需要在 Windows XP 中檢查存取權，請使用 [**RpcGetAuthorizationCoNtextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) 函數。 產生的 Authz 內容可提供非常快速的存取檢查，可透過 RPC 執行時間有效率地快取。

## <a name="do-not-modify-the-token-unless-necessary"></a>除非必要，否則請勿修改權杖

如果使用動態身分識別追蹤，除非絕對必要，否則請勿修改執行緒/進程 token。 即使已修改為先前擁有的設定，權杖通常與安全性系統有足夠的差異，以觸發新的安全性內容建立。

## <a name="consider-mixed-mode-serialization-for-context-handles"></a>針對內容控制碼考慮混合模式序列化

內容控制碼的預設序列化模式會序列化 (獨佔) 。 請考慮進行所有不修改共用序列化模式中內容控制碼狀態的呼叫。 如需詳細資訊，請參閱 [**RpcSsCoNtextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) 。

 

 




