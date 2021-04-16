---
description: Windows 挑戰/回應 (NTLM) 是在網路上使用的驗證通訊協定，該通訊協定包含執行 Windows 作業系統和獨立系統的系統。
ms.assetid: 35a38858-d36f-45c9-95f4-2541a182f5ac
title: Microsoft NTLM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9723f24d5913adefe70d4e238de0591790a34bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511236"
---
# <a name="microsoft-ntlm"></a>Microsoft NTLM

Windows 挑戰/回應 (NTLM) 是在網路上使用的驗證通訊協定，該通訊協定包含執行 Windows 作業系統和獨立系統的系統。

Microsoft [*Kerberos*](../secgloss/k-gly.md) [*安全性套件*](../secgloss/s-gly.md) 可為網路上的系統增加更高的安全性。 雖然 Microsoft *Kerberos* 是所選擇的通訊協定，但仍支援 NTLM。 NTLM 還必須用於獨立系統的登入驗證。 如需有關 Kerberos 的詳細資訊，請參閱 [Microsoft kerberos](microsoft-kerberos.md)。

NTLM 認證是以互動式登入程式期間取得的資料為基礎，並且包含功能變數名稱、使用者名稱和使用者密碼的單向 [*雜湊*](../secgloss/h-gly.md) 。 NTLM 使用加密的挑戰/回應通訊協定來驗證使用者，而不需要透過網路傳送使用者的密碼。 相反地，要求驗證的系統必須執行計算，以證明它可以存取安全的 NTLM 認證。

透過網路的互動式 NTLM 驗證通常牽涉到兩個系統：用戶端系統（使用者要求驗證的用戶端系統），以及網域控制站，其中會保留與使用者密碼相關的資訊。 非互動式驗證（可能需要允許已登入的使用者存取資源，例如伺服器應用程式），通常需要三個系統：用戶端、伺服器，以及代表伺服器進行驗證計算的網域控制站。

下列步驟顯示 NTLM 非互動式驗證的大綱。 第一個步驟會提供使用者的 NTLM 認證，而且只會在互動式驗證 (登入) 處理過程中發生。

1.  只有在使用者存取用戶端電腦並提供功能變數名稱、使用者名稱和密碼時，) 才 (互動式驗證。 用戶端會計算密碼的密碼編譯 [*雜湊*](../secgloss/h-gly.md) ，並捨棄實際的密碼。
2.  用戶端會將使用者名稱以 [*純文字*](../secgloss/p-gly.md)) 傳送至伺服器 (。
3.  伺服器會產生16位元組的亂數字（稱為 *挑戰* 或 [*nonce*](../secgloss/n-gly.md)），並將它傳送至用戶端。
4.  用戶端會使用使用者密碼的雜湊來加密這項挑戰，並將結果傳回伺服器。 這稱為 *回應*。
5.  伺服器會將下列三個專案傳送至網域控制站：

    -   使用者名稱
    -   傳送至用戶端的挑戰
    -   從用戶端收到的回應

6.  網域控制站會使用使用者名稱，從安全性帳戶管理員資料庫取出使用者密碼的雜湊。 它會使用此密碼雜湊來加密挑戰。
7.  網域控制站會比較在步驟6中所計算 (的加密挑戰，) 到步驟 4) 中用戶端 (所計算的回應。 如果兩者相同，驗證就會成功。

您的應用程式不應直接存取 NTLM [*安全性封裝*](../secgloss/s-gly.md) ;相反地，它應該使用 [*Negotiate*](../secgloss/n-gly.md) 安全性封裝。 Negotiate 可讓您的應用程式利用更高階的 [*安全性通訊協定*](../secgloss/s-gly.md) （如果驗證所含的系統支援的話）。 目前，協商安全性封裝會在 [*Kerberos*](../secgloss/k-gly.md) 和 NTLM 之間進行選取。 除非其中一個與驗證相關的系統無法使用，否則 Negotiate 會選取 Kerberos。

 

 
