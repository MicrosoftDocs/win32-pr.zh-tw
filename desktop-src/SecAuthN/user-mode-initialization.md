---
description: 分散式 (用戶端/伺服器) 應用程式會使用安全性套件來取得已驗證的連線，以及交換訊息。
ms.assetid: 8f28177f-335a-4fa2-bf66-2ec1698bebec
title: 使用者模式初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09be7c4c00937473e2ecc3d6b01bb7c59a2842085a133f381b5a8a10bd9b215f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915580"
---
# <a name="user-mode-initialization"></a>使用者模式初始化

分散式 (用戶端/伺服器) 應用程式會使用 [*安全性套件*](../secgloss/s-gly.md) 來取得已驗證的連線，以及交換訊息。 應用程式會呼叫安全性支援提供者介面 (SSPI) 函式，這些函式會對應至 [SSP/ap 所執行](authentication-functions.md)的函式，以及 [使用者模式 SSP/ap 所執行](authentication-functions.md)的函式。 這項對應是由安全性提供者 DLL (Secur32.dll 或 Security.dll) （可以動態載入至用戶端和伺服器進程）執行。 DLL 也可以使用 Secur32 以靜態方式連結。 DLL 和 LIB 都隨附于 Microsoft Windows 軟體開發套件 (SDK) 。

如果包含安全性封裝的 SSP/AP DLL 已正確註冊，則系統會處理將安全性封裝載入用戶端或伺服器的進程。

伺服器會從監視埠（等候用戶端傳送訊息）開始取得與用戶端安全連線的程式。 用戶端會藉由呼叫 SSPI 函式 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)，開始取得伺服器安全連線的程式。 此函式會對應到自訂安全性封裝的 [**SpInitLsaModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) 函式。 **SpInitLsaModeCoNtext** 會將權杖傳回給用戶端，並將其轉送至伺服器。

從用戶端收到權杖時，伺服器會呼叫 SSPI 函式 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)，此函式會分派到安全性套件的 [**SpAcceptLsaModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) 函式。 如果 **SpAcceptLsaModeCoNtext** 函式成功，而且不再需要處理來建立安全性內容，則函式應該會將狀態 \_ 成功傳回給呼叫者。 如果需要額外的處理，此函式應該會傳回 \_ 我繼續需要的秒數 \_ \_ ，然後將權杖傳回給伺服器。 伺服器會將權杖轉送至用戶端，而該用戶端會再次呼叫 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 。

在已驗證的連接建立或失敗之前，此呼叫迴圈可能會經常重複。 在這個過程中，如果 [**SpAcceptLsaModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) 或 [**SpInitLsaModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) 函式成功，而且不需要再處理來建立 [*安全性內容*](../secgloss/s-gly.md)，則函式應該會將狀態 \_ 成功傳回給呼叫者。 如果需要額外的處理，則函式應該會傳回 \_ 我繼續需要的秒數 \_ \_ ，然後將權杖傳回給呼叫者，負責轉送它。

由安全性封裝所執行的通訊協定會決定重複此迴圈的次數。 例如，在支援三階段相互驗證的安全性封裝中，呼叫順序如下所示：

1.  用戶端會藉由呼叫 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)來取得權杖，並將它傳送至伺服器。 伺服器第一次呼叫 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) ，並取得傳送給用戶端的回復權杖。
2.  用戶端會使用從伺服器收到的權杖，在第二次呼叫 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)，然後取得最終的權杖。 用戶端會將此權杖傳送至伺服器。
3.  伺服器會接收第2階段所產生的權杖，以在 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)的最終呼叫中使用。

當 [**SpAcceptLsaModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) 和 [**SpInitLsaModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) 函式成功，而且不再需要處理來建立安全性內容時，這些函式應該會將狀態 \_ 成功傳回給呼叫者。 此外，如果自訂安全性封裝支援 [使用者模式 SSP/ap 所執行](authentication-functions.md)的函式，則 **SpAcceptLsaModeCoNtext** 和 **SpInitLsaModeCoNtext** 必須透過 *MappedCoNtext* 參數傳回 **TRUE** 。 *MappedCoNtext* 值不會傳回給應用程式;它是由 LSA 攔截的。

當 *MappedCoNtext* 為 **TRUE** 時，LSA 會呼叫 SSP/AP DLL 的 [**SpUsermodeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spusermodeinitializefn) 函式。 此函式會提供每個安全性封裝所執行的使用者模式函數指標的表格。 每個封裝的 [**SpInstanceInit**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinstanceinitfn) 函式都會使用 **SpUsermodeInitialize** 所傳回的函數資料表來呼叫。 **SpInstanceInit** 會接收 [使用者模式 SSP/ap 所呼叫之 LSA](authentication-functions.md)函式的指標表格。

 

 
