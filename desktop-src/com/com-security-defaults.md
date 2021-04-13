---
title: COM 安全性預設值
description: 您可以使用應用程式的 COM 安全性預設值，而非指定您自己的安全性設定。
ms.assetid: 6f1f6925-a6ab-4cfa-b0b4-b4b4012979f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cba607044d6e93c9f01243809feae6e5a600851
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300131"
---
# <a name="com-security-defaults"></a>COM 安全性預設值

您可以使用應用程式的 COM 安全性預設值，而非指定您自己的安全性設定。 在這種情況下，COM 會為您初始化及管理安全性。 您不需要設定登錄或呼叫程式中的任何安全性功能。

但是，如果已設定或修改特定的登錄值，COM 使用的安全性預設值將會受到影響。 下列清單說明 COM 安全性的預設值，並說明某些值如何受到登錄設定的影響。

以下是 COM 使用的預設安全性值：

-   預設的安全性服務提供者是由 COM 決定最符合環境的安全性服務提供者。 COM 會選擇 Kerberos v5 通訊協定或 NTLMSSP，其中的 Kerberos 通訊協定是預設選項。 Schannel 提供的通訊協定都未被選擇為預設值。
-   系統會透過使用者名稱和密碼來識別呼叫者，並自動建立安全性系統所使用的識別權杖。
-   如果 [LegacyAuthenticationLevel](legacyauthenticationlevel.md) 名稱值存在，而且已設定其值，則會使用該值。 否則，驗證層級會設定為 connect (RPC \_ C \_ 驗證 \_ level \_ connect) 。 這個層級表示，在用戶端對伺服器進行的第一次呼叫時，COM 會進行驗證檢查。 如果用戶端通過檢查，就不會再進行進一步的驗證。 AuthenticationLevel 值也可以在 [AppID](appid-key.md) 索引鍵下設定。
-   如果 [LegacyImpersonationLevel](legacyimpersonationlevel.md) 名稱值存在，而且已設定其值，則會使用該值。 否則，會將模擬層級設定為識別)  (RPC \_ C \_ IMP \_ 等級 \_ 。 用戶端會將模擬許可權授與伺服器。 識別層級表示伺服器可以取得用戶端的身分識別。 伺服器可以模擬用戶端的存取控制清單 (ACL) 檢查，但是無法存取系統物件做為用戶端。 如需詳細資訊，請參閱模擬 [層級](impersonation-levels.md) 和 [掩蓋](cloaking.md)。
-   如果 **AppID** 下的 [AccessPermission](accesspermission.md)命名值存在且已設定，則會使用該值。 否則，COM 會檢查是否有 [DefaultAccessPermission](defaultaccesspermission.md) 專案。 如果存在，則會使用該值。 如果此值不存在，COM 會將授與許可權給伺服器身分識別和本機系統的 ACL 進行結構。
-   如果 **AppID** 下的 [SRPTrustLevel](srptrustlevel.md)命名值存在且已設定，則會使用該值。 否則，軟體限制原則 (SRP) 信任層級設定為 [不允許]， (更安全的 \_ LEVELID \_) ，這表示應用程式會在受限的環境中執行，而且不允許存取使用者的任何安全性敏感性使用者權限。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 




