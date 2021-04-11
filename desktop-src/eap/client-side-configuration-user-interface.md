---
title: Client-Side 設定消費者介面
description: 實行驗證通訊協定的廠商也可以為通訊協定提供設定使用者介面 (UI) 。
ms.assetid: 956a7ad6-1fd5-4938-aa2f-4de646dfd6c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7296f6afd8fd84f287b6c2c7085e5ed92685f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314887"
---
# <a name="client-side-configuration-user-interface"></a>Client-Side 設定消費者介面

實行驗證通訊協定的廠商也可以為通訊協定提供設定使用者介面 (UI) 。 設定 UI 可在與驗證通訊協定相同的 DLL 中，或在個別的 DLL 中執行。 此外，執行設定 UI 的 DLL 可能會支援一個以上的驗證通訊協定。 設定 UI 的 DLL 路徑會儲存在「RAS \_ EAP VALUENAME CONFIGUI 登錄」 \_ 值的「 \_ 驗證通訊協定」機碼下。 如需有關建立此登錄值的詳細資訊，請參閱 [EAP 安裝](eap-installation.md)。

設定使用者介面的 DLL 應匯出下列函式的進入點：

[**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui)

[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

當使用者建立特定連線的設定專案時，無論是針對 RAS 或無線用戶端，使用者都可以選取服務應該與該專案搭配使用的驗證通訊協定。 如果驗證通訊協定是可設定的，則服務會呼叫 [**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui) 來叫用設定 UI。 設定 UI 會將 **RasEapInvokeConfigUI** 傳回的設定資訊儲存在設定專案中。

設定資訊對用戶端電腦上的所有使用者都是通用的。 特定使用者或使用者的特定資訊不應儲存在專案中。 驗證通訊協定應該使用身分 [識別](obtaining-identity-information.md) 函 [式或互動式使用者介面](interactive-user-interface.md)來取得使用者特定的資訊。 驗證通訊協定可以將這項資訊儲存在登錄中，方法是將它傳遞至 [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))的 *pEapOutput* 參數中的驗證服務。

設定資訊也應該不是目前電腦的特定資訊;它應該可從機器移植到電腦。

當驗證服務針對驗證通訊協定呼叫 [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) 函式時，它會將包含指標的 [**PPP \_ EAP \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) 結構傳遞至設定資訊。 呼叫 **RasEapBegin** 完成之後，驗證服務會呼叫 [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) 來釋放設定資訊所佔用的記憶體。 因此，在呼叫 **RasEapBegin** 期間，驗證通訊協定應該會將設定資訊複製到私用記憶體緩衝區。

廠商可以在指定通訊協定預設設定資訊的驗證通訊協定的登錄機碼下新增值。 廠商也可以新增值，指定使用者建立電話簿專案時是否需要輸入設定資訊。 如需詳細資訊，請參閱 [驗證通訊協定登錄值](authentication-protocol-registry-values.md)。

 

 