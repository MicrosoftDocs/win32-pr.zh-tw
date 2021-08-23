---
title: 取得身分識別資訊
description: 實作為驗證通訊協定的廠商也可以提供函數介面，以取得要求驗證之使用者的初始識別資訊。
ms.assetid: 773c9fdb-c810-4cea-afed-df6484a9c9c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46245b22a5538fc347ba735620270b7bbc1071574852305adc6b3881202ae317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605818"
---
# <a name="obtaining-identity-information"></a>取得身分識別資訊

實作為驗證通訊協定的廠商也可以提供函數介面，以取得要求驗證之使用者的初始識別資訊。

廠商應該執行下列功能。

-   [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)
-   [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

這些函式可以在與驗證通訊協定相同的 DLL 或個別的 DLL 中執行。 此外，執行身分識別函式的 DLL 可能會支援一個以上的驗證通訊協定。 這些函式之 DLL 的路徑會儲存在 [ [RAS \_ EAP VALUENAME \_ 身分 \_ 識別](authentication-protocol-registry-values.md) 登錄] 值的 [驗證通訊協定] 的金鑰下。 如需有關建立此登錄值的詳細資訊，請參閱 [EAP 安裝](eap-installation.md)。

[**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)函式通常會顯示使用者介面 (UI) 來取得使用者的身分識別資訊。 但是，如果 *dwFlags* 參數包含 RAS \_ EAP 旗標 \_ \_ 非 \_ 互動式旗標，則 **RasEapGetIdentity** 不應顯示 UI。

如果 [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)確實顯示 ui，則 ui 必須支援 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) (*wParam*) 值等於 IDCANCEL 的 [**WM \_ 命令**](../menurc/wm-command.md)訊息。

如果此 EAP 的登錄中的 [RAS \_ EAP \_ VALUENAME \_ INVOKE \_ NAMEDLG](authentication-protocol-registry-values.md)值設為零，則驗證服務會呼叫 [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) 。 如果 RAS \_ EAP \_ VALUENAME \_ INVOKE 叫用 \_ NAMEDLG 不存在或存在，而且設定為1，則驗證服務會顯示標準系統使用者名稱對話方塊。

除了 RAS \_ EAP \_ valuename \_ INVOKE \_ NAMEDLG，EAP 廠商可能會在登錄中建立相關的值，也就是 [ras \_ eap \_ valuename \_ invoke \_ PWDDLG](authentication-protocol-registry-values.md)。 如果這個值存在且設定為零，服務將不會顯示標準系統密碼對話方塊。 此值在執行生物特徵辨識方法（例如指紋掃描）來驗證使用者時很有用。 如果 RAS \_ eap \_ valuename \_ INVOKE \_ NAMEDLG 和 ras \_ eap \_ valuename \_ invoke \_ PWDDLG 值為零，則可以使用身分識別 UI 來取得身分識別和生物特徵辨識資訊。 但是，如果只有 RAS \_ EAP \_ VALUENAME \_ INVOKE \_ PWDDLG 為零，驗證服務將不會呼叫 [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)。 在此情況下，您可以使用 [互動式使用者介面](interactive-user-interface.md) 來取得生物特徵辨識資訊。

如需這些登錄值的詳細資訊，請參閱 [驗證通訊協定登錄值](authentication-protocol-registry-values.md)。

[**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)所取得的資訊會在呼叫 [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))期間傳遞至驗證通訊協定。 這項資訊是由 [**PPP \_ EAP \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)結構的 **pszIdentity** 和 **pUserData** 成員所指向。 若要將此資訊儲存在用戶端電腦的登錄中，驗證通訊協定應該會傳回 [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))的 *pEapOutput* 參數中的資訊。

呼叫 [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))之後，驗證服務會呼叫 [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) 來釋放此資料所佔用的記憶體。 因此，在呼叫 **RasEapBegin** 期間，驗證通訊協定應該會將資訊複製到私用記憶體緩衝區。

 

 