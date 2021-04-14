---
title: 關閉啟用安全性
description: 關閉啟用安全性
ms.assetid: 3474f8ad-f041-4886-ad39-ff0603c5c69e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da3ebd7cc03d79fc38fbafe3bc652efc3499437
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382950"
---
# <a name="turning-off-activation-security"></a>關閉啟用安全性

一般來說，啟用會使用預設安全性設定。 不過，您可以藉由指定 [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) 結構來控制啟用安全性，這是傳遞給啟用函式的 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) 結構成員。 如果用戶端 \_ \_ 在 COAUTHINFO 結構中指定 RPC C 驗證 \_ 層級無驗證等級 \_ ，則不會嘗試驗證。  否則，將會嘗試安全啟用，如果驗證失敗，則啟用會失敗。

如果用戶端未指定明確的 [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) 結構，而改為將指標設定為 **Null**，COM 將會嘗試驗證用戶端。 如果無法驗證用戶端，COM 會檢查啟動許可權安全描述項，以查看是否有 **Null** DACL 或允許存取所有人的 ACL。 如果此檢查成功，則會啟動伺服器。 因此，即使用戶端未指定 **COAUTHINFO** 結構，在伺服器允許不安全的啟用時也可能會發生。

> [!Note]  
> 若要允許未驗證的網路使用者執行 COM 應用程式，應用程式角色必須包含匿名使用者。 從 Windows Server 2003 開始，根據預設，匿名使用者不會包含在 Everyone 群組中。

 

為什麼用戶端會想要明確關閉啟用安全性，即使伺服器允許不安全的啟用也會發生？ 因為當用戶端不想要或不需要安全性檢查時，明確關閉啟用安全性可提高效能。

您必須執行下列動作，以明確關閉啟用安全性：

-   用戶端必須 \_ 在 COAUTHINFO 結構中指定 RPC C 驗證層級 NONE 的驗證層級，該 \_ \_ \_ 結構是提供給啟用函式之 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)結構的成員。 [](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo)
-   用戶端必須在 COAUTHINFO 結構中指定模擬的 RPC C IMP 層級模擬層級，該 \_ \_ \_ \_ 結構是提供給啟用函式之 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)結構的成員。 [](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) 如果未傳遞此值，您將無法取得 RPC \_ S \_ 伺服器 \_ 。
-   伺服器必須指定 **預設啟動許可權** 的 **所有人**。 執行這項工作的建議方式是使用 Dcomcnfg.exe，如下所示：
    1.  執行 Dcomcnfg.exe。
    2.  在 [ **應用程式** ] 頁面上，選取代表伺服器的應用程式。 按一下 [ **屬性** ] 按鈕 (或按兩下選取的應用程式) 。
    3.  在 [ **安全性** ] 屬性頁上，按一下 [ **使用自訂啟動許可權** ] 按鈕。
    4.  按一下 [**啟動許可權**] 區域中的 [**編輯**] 按鈕。
    5.  在 [登錄 **值許可權** ] 對話方塊中，按一下 [ **新增** ] 按鈕。
    6.  在清單方塊中選取 [ **所有人** ] 的專案。
    7.  在 [ **存取類型** ] 清單方塊中，選擇 [ **允許啟動**]。
    8.  按一下 [確定] 按鈕。

> [!Note]  
> 在 Windows Server 2003 中，COM + 系統應用程式的驗證功能包含 EOAC \_ DISABLE AAA 的值 \_ 。 此值會在啟動系統應用程式時，在 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 呼叫中使用停用的 (AAA) 啟用。 將驗證功能設定為 EOAC \_ DISABLE \_ AAA，可讓在特殊許可權帳戶下執行的應用程式 (例如 LocalSystem) ，以協助防止其身分識別用來啟動未受信任的元件。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關閉通話安全性](turning-off-call-security.md)
</dt> </dl>

 

 