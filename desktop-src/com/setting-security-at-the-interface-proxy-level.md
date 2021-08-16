---
title: 在介面 Proxy 層級設定安全性
description: 有時候，用戶端需要對特定介面的呼叫安全性進行細微的控制。
ms.assetid: 72925ca2-78c9-47d9-8760-63f6379326d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef969039dcfdc12449b7a8d0a3d63729ab5f84061ade1a743d21a1b6b34331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309093"
---
# <a name="setting-security-at-the-interface-proxy-level"></a>在介面 Proxy 層級設定安全性

有時候，用戶端需要對特定介面的呼叫安全性進行細微的控制。 例如，可能會針對進程設定較低層級的安全性，但對特定介面的呼叫可能需要較高的驗證層級，例如加密。 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)介面的方法可讓用戶端藉由控制介面 proxy 層級的安全性設定，來變更與特定介面呼叫相關聯的安全性設定。

用戶端可以查詢現有的物件以進行 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) ，然後呼叫 [**IClientSecurity：： QueryBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-queryblanket) 方法，找出特定介面 proxy 目前的安全性設定。 [**IClientSecurity：： SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)方法可以用來修改物件上個別介面 proxy 的安全性設定，然後再呼叫其中一個介面方法。 新的設定會套用到此特定介面的任何未來呼叫者。 [**IClientSecurity：： CopyProxy**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-copyproxy)方法提供一種方式，讓用戶端複製介面 proxy，以便後續對複本的 **SetBlanket** 呼叫不會影響原始 proxy 的呼叫端。

[**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) 通常用來將特定介面 proxy 的驗證層級提升至更高層級的安全性保護。 不過，在某些情況下，降低特定介面 proxy 的驗證層級也會很有説明。 例如，假設進程的預設驗證層級是 RPC \_ C 驗證層級以外的某個 \_ 值 \_ \_ ，而且用戶端和伺服器位於不信任彼此的不同網域中。 在此情況下，除非用戶端呼叫 **SetBlanket** 將驗證層級降低至 RPC \_ C \_ 驗證 \_ 層級 NONE，否則對伺服器的呼叫將會失敗 \_ 。

使用 proxy 管理員所提供之 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) 預設實作為的用戶端，可以呼叫 [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket)、 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)和 [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) helper 函式，而不是直接呼叫 **IClientSecurity** 方法。 Helper 函式可簡化程式碼，但比直接呼叫對應的 **IClientSecurity** 方法稍微低一點。

Proxy 管理員會為用戶端在本機執行 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) 介面。 某些自訂封送處理的物件可能不支援 **IClientSecurity**。

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) 適用于所有支援的驗證服務 (目前的 NTLMSSP、Schannel 和 Kerberos v5 通訊協定) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 COM 應用程式的安全性](setting-security-for-com-applications.md)
</dt> </dl>

 

 