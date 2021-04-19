---
description: 指定 Schannel 密碼和加密的強度
ms.assetid: b87d3e72-df7b-4a00-854e-c3706565ed7d
title: 指定 Schannel 密碼和加密的強度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04ec37cfea633814881fba5bfd71ad15205a1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984651"
---
# <a name="specifying-schannel-ciphers-and-cipher-strengths"></a>指定 Schannel 密碼和加密的強度

針對用戶端/伺服器資訊交換，Schannel 的預設行為是根據登錄中啟用的密碼來協商可用的最佳加密。 應用程式可能會使用安全通道認證結構的成員，限制連接所允許的加密和加密強度， [**如下所示 \_**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) ：

1.  將 **palgSupportedAlgs** 成員設定為包含允許之密碼的 [**ALG \_ 識別碼**](../seccrypto/alg-id.md) 陣列。 如需詳細資訊，請參閱密碼識別碼。
2.  將 **dwMinimumCipherStrength** 和/或 **dwMaximumCipherStrength** 成員設定為允許的最小和最大強度。 如需詳細資訊，請參閱加密強度值。
3.  透過呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)函式的 *pAuthData* 參數) [**，將安全通道認證結構 (\_**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) 。 此函數會傳回認證控制碼。
4.  在用戶端 InitializeSecurityCoNtext 的呼叫中指定認證控制碼 [**(一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函數或伺服器端 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函式。

## <a name="cipher-ids"></a>加密識別碼

Schannel 的預設行為是根據系統登錄中的 Schannel 專案要求可用的最佳加密。 請勿變更系統登錄;它針對 Schannel 所包含的設定會在全域使用，並會影響其他應用程式。 如需有效的常數清單，請參閱 [**ALG \_ 識別碼**](../seccrypto/alg-id.md)。

## <a name="cipher-strength-values"></a>加密強度值

這種安全通道功能通常是用來限制與國內或出口強度加密的連接。 國內的強項包括56和128位，而匯出強度限制為56位。 如果您將最小值和最大值設定為零，則 Schannel 將會使用所有可用的加密強度。

使用 TLS 或 SSL 3.0，將 **dwMinimumCipherStrength** 成員設定為-1 (負一個) 來啟用 "Null cipher" 加密套件，以提供簽章但不加密。 如果 **dwMaximumCipherStrength** 也設定為-1，則只會啟用 "Null Cipher" 套件。 這項設定僅供開發之用，不應該用於生產系統。

## <a name="querying-cipher-information"></a>查詢加密資訊

若要取得認證的加密強度設定，請呼叫 [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) 函式，並 \_ 將 SECPKG ATTR \_ 加密強度指定 \_ 為 *ulAttribute* 參數。

若要取得認證的支援演算法清單，請使用 SECPKG ATTR 支援的 ALGS 來呼叫 [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) ， \_ \_ \_ 作為 *ulAttribute* 參數。

 

 
