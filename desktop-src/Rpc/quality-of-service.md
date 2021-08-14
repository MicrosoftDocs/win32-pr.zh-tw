---
title: '服務品質 (RPC) '
description: 用戶端程式可以使用 RpcBindingSetAuthInfoEx 函式，而不是 RpcBindingSetAuthInfo 函式來建立已驗證的系結。
ms.assetid: bc3d47ba-3c1b-4aba-8fe3-b4501a621931
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d7c68386a5d7db4f59b620bc998d628faa2969671ef99b5c5fc2c65aadeb96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927146"
---
# <a name="quality-of-service-rpc"></a>服務品質 (RPC) 

用戶端程式可以使用 [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) 函式，而不是 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) 函式來建立已驗證的系結。 如果有，則會將指向 [**RPC \_ 安全性 \_ QOS**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) 結構的指標傳遞為 **RpcBindingSetAuthInfoEx** 的最後一個參數。 此結構包含服務品質的相關資訊。 用戶端程式也可以指定身分識別追蹤，然後選取模擬類型。

使用 [**RPC \_ 安全性 \_ QOS**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos)結構的 **功能** 成員，來設定用戶端/伺服器應用程式的哪些部分經過驗證。 如果 \_ \_ 選取 [rpc C QOS 功能] \_ \_ 預設值，則 RPC 執行時間程式庫會根據 SSP 的預設值來驗證用戶端或伺服器。 Kerberos 通訊協定 SSP 預設會驗證用戶端和伺服器。 Microsoft 提供的所有其他 Ssp 預設為向伺服器驗證用戶端，但不會向用戶端驗證服務器。

如果用戶端和伺服器應該一律彼此驗證，請將 [**rpc \_ 安全性 \_ Qos**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos)結構的 **功能** 成員設定為 rpc \_ C \_ qos \_ 功能的 \_ 相互 \_ 驗證。 某些安全性提供者可能不支援相互驗證。 如果對 \_ \_ \_ \_ 這類安全性提供者指定了 RPC C QOS 功能的相互 \_ 驗證，則會在進行遠端程序呼叫時傳回錯誤。 使用安全通道 SSP 時，也可以將 **功能** 成員設定為 RPC \_ C \_ QOS \_ 功能的 \_ 任何授權單位 \_ 。 這個常數會指定即使發出用戶端驗證憑證的憑證授權單位單位不在 SSP 的根憑證存放區中，SSP 仍應驗證遠端程序呼叫。 如果 SSP 無法辨識憑證授權單位單位，則預設值為拒絕憑證。 憑證授權單位單位是一種獨立的公司或組織，例如 VeriSign，會發出驗證憑證。

應用程式也可以設定 RPC 執行時間程式庫所使用的身分識別追蹤。 程式通常會使用 [*靜態身分識別追蹤*](s-glos.md)。 使用靜態追蹤時，會在呼叫 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) 函式時設定用戶端的認證。 然後，RPC 執行時間程式庫會針對系結上的所有 RPC 呼叫使用這些認證，不論呼叫端執行緒的身分識別變更或呼叫進程為何。 應用程式也可以選取 [*動態身分識別追蹤*](d-glos.md)。 動態身分識別追蹤會指示 RPC 執行時間程式庫在每次呼叫時使用呼叫執行緒的認證，而不是在系結控制碼中使用。 預設的身分識別追蹤是靜態的。

如果用戶端的身分識別不會變更，靜態身分識別追蹤可能會有較佳的效能特性，而且可以在每次呼叫執行緒上的身分識別是否與提供給安全性系統的身分識別相同時，儲存 RPC 執行時間檢查。 如果呼叫執行緒的身分識別在呼叫之間可能會變更，而且伺服器需要辨識這些變更，最好是指定動態身分識別追蹤，也就是讓 RPC 執行時間以安靜且有效率的方式追蹤身分識別，而如果身分識別變更的話，就代表您管理該變更。

> [!Note]  
> 針對 **ncalrpc** 呼叫，靜態和動態身分識別追蹤具有不同的效能特性，而且視情況而定，可能會更快。

 

作為 QOS 規格的一部分，用戶端程式也可以設定伺服器程式可代表其執行的模擬類型。 如需詳細資訊，請參閱 [用戶端](client-impersonation.md)模擬。

[**Rpc \_ 安全性 \_ qos**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos)結構的 [版本號碼] 欄位應一律設定為 [rpc \_ C \_ 安全性 \_ qos \_ 版本]。

 

 




