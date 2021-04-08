---
title: 驗證期間的存取點和驗證通訊協定互動
description: RasEapMakeMessage 函式會控制驗證通訊協定和存取點之間的大部分互動 (AP) 。
ms.assetid: edc128e0-3104-4df9-80f4-b2aebcfe1087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e486e3a10e323f28bc2f6fef4c131acfc095b48
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023316"
---
# <a name="access-point-and-authentication-protocol-interaction-during-authentication"></a>驗證期間的存取點和驗證通訊協定互動

[**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))函式會控制驗證通訊協定和存取點之間的大部分互動 (AP) 。 **RasEapMakeMessage** 會處理傳入的 eap 封包，並建立用於傳輸至遠端對等的 eap 封包。 它也會處理事件，例如超時和驗證完成。

如果從遠端對等接收訊息，則 AP 驗證服務會呼叫 [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))，並將指標傳遞至 *pReceivePacket* 參數中所接收的訊息。

如果服務呼叫 [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) ，並將 *PReceivePacket* 設定為 **Null**，則 AP 會使用驗證通訊協定來起始對話方塊，或要求該通訊協定重新傳送最後一個封包。 驗證通訊協定應該根據服務的狀態和訊息內容，判斷服務所採取的動作。

從 [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))返回時， [**PPP \_ EAP \_ 輸出**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output)結構的 **動作** 成員值會指出驗證服務所採取的動作（如果有的話）。 **動作** 成員接受來自 [**PPP \_ EAP \_ 動作**](/windows/desktop/api/Raseapif/ne-raseapif-ppp_eap_action)列舉型別的值。

如果 **Action** 為 **EAPACTION \_ Send**、 **EAPACTION \_ SendAndDone**、 **EAPACTION \_ SendWithTimeout** 或 **EAPACTION \_ SendWithTimeoutInteractive**，服務會將 *pSendPacket* 參數所指向的封包傳送給遠端對等。

**EAPACTION \_ SendWithTimeout** 值允許時間超時，經過這段時間之後，驗證服務會假設連結已遺失，並中斷會話的連線。

**EAPACTION \_ SendWithTimeoutInteractive** 值允許無限的時間量發生。 當用戶端需要使用者輸入時，驗證器應該使用此值。 此超時時間可讓使用者未指定的時間量完成所需的輸入。

如果 **Action** 是 **EAPACTION \_ SendWithTimeout** 或 **EAPACTION \_ SendWithTimeoutInteractive**，則驗證通訊協定應該將 [**PPP \_ EAP \_ 輸出**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output)結構的 **dwIdExpected** 成員設定為從遠端對等的下一個封包的識別碼。 無論下一個從對等接收的封包是否符合此值，驗證服務都會在後續呼叫 [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))時，將封包傳遞給驗證通訊協定。 驗證通訊協定可能會以無訊息方式捨棄封包，方法是直接傳回 **錯誤 \_ PPP \_ 無效 \_** 的封包。 如果在設定的超時期間內未收到具有預期識別碼的封包，驗證服務仍會呼叫 **RasEapMakeMessage**。 在此情況下，會使用將 *pReceivePacket* 參數設定為 **Null** 來進行呼叫，以表示必須再次傳送先前的封包。

如果 **動作** 成員是 **EAPACTION \_ Done** 或 **EAPACTION \_ SendAndDone**，驗證服務會檢查 [**PPP \_ EAP \_ 輸出**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output)的 **dwAuthResultCode** 成員。 如果 **DWAUTHRESULTCODE** 沒有 \_ 錯誤，驗證就會成功。 如果 **dwAuthResultCode** 是沒有錯誤的值 \_ ，則驗證失敗。 針對失敗案例傳回的錯誤碼應該來自 Raserror .h、Mprerror .h 或 Winerror.h。 可能的傳回碼包括（但不限於）下列各項：

-   錯誤 \_ 無 \_ 撥入 \_ 許可權
-   錯誤 \_ 密碼已 \_ 過期
-   錯誤 \_ 帳戶 \_ 已停用
-   錯誤 \_ 限制 \_ 登入時 \_ 數
-   錯誤 \_ 驗證 \_ 內部

如果 **Action** 是 **EAPACTION \_ Done** 或 **EAPACTION \_ SendAndDone**， **pUserAttributes** 成員應指向屬性，以覆寫在 [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))的呼叫中傳遞給伺服器的相同類型的屬性。

伺服器上的驗證通訊協定可以要求驗證服務叫用目前的驗證提供者，方法是在 [**PPP \_ EAP \_ 輸出**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output)的 **動作** 成員中傳回 **EAPACTION \_ 驗證**。 在此情況下， **PPP \_ EAP \_ 輸出** 中的 **pUserAttributes** 指標只會指向伺服器上的驗證通訊協定所產生的屬性。 它不包含任何在 [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))的呼叫中傳遞給伺服器的屬性。 驗證提供者不需要這些初始屬性，因為驗證認證是在 EAP 訊息本身內，而不是個別的 RADIUS 屬性。 當驗證服務回應 **EAPACTION \_ 驗證** 動作時， **pUserAttributes** 在 [**PPP \_ EAP \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)中會指向驗證期間產生的所有屬性。 這些屬性會傳回至用戶端上的驗證通訊協定。

如果驗證通訊協定使用 **EAPACTION \_ 驗證**，則驗證提供者會執行 PAP 或 MD5-CHAP。 此驗證方法只能搭配 Windows 用戶端使用。

如果驗證通訊協定不依賴驗證提供者來驗證使用者，就不需要通訊協定設定 **EAPACTION \_ 驗證** 的 **動作**。 這種情況的範例是 EAP-Transport 層安全性 (TLS) 。

EAP 成功封包是未認可的封包。 因此，伺服器可能會遺失且不會重新傳送。 如果用戶端上的驗證服務收到 (NCP) 封包的網路控制通訊協定，伺服器端驗證服務會繼續執行，就像驗證成功一樣。 這是因為伺服器已移至 PPP 的 NCP 階段。 因此，驗證服務會呼叫 [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) ，並將 [**PPP \_ EAP \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)結構的 **fSuccessPacketReceived** 成員設為 **TRUE**。

在驗證會話的過程中，驗證通訊協定可能需要直接與用戶端上的使用者互動。 驗證通訊協定廠商可以針對此目的提供互動式使用者介面。 驗證通訊協定可透過在 [**PPP \_ EAP \_ 輸出**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output)結構中設定 **fInvokeInteractiveUI**、 **pUICoNtextData** 和 **dwSizeOfUICoNtextData** 成員，要求服務顯示互動式 UI。 如需使用互動式 UI 的詳細資訊，請參閱 [互動式消費者介面](interactive-user-interface.md)。

驗證通訊協定應該只透過 [互動式消費者介面](interactive-user-interface.md)下所述的機制來顯示使用者介面。 如果驗證通訊協定本身顯示使用者介面，PPP 執行緒會封鎖，直到關閉使用者介面為止。

如果在驗證程式期間， [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) 會傳回任何不是 **\_ 錯誤** 或 **錯誤 \_ PPP 無效封 \_ \_ 包** 的值、會話已中斷連線，並在伺服器上記錄錯誤 () 或顯示給用戶端) 上的使用者 (。

 

 