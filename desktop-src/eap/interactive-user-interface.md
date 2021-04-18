---
title: 互動式消費者介面
description: 實作為驗證通訊協定的廠商也可以為通訊協定提供互動式使用者介面 (UI) 。
ms.assetid: 4f8ba0a4-3b52-4e7c-9e67-748f8d81d7a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761799969f4e439a65534ab551f09b3788e95ba7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968897"
---
# <a name="interactive-user-interface"></a>互動式消費者介面

實作為驗證通訊協定的廠商也可以為通訊協定提供互動式使用者介面 (UI) 。 互動式 UI 可讓驗證通訊協定在驗證會話期間，視需要從使用者取得其他資訊。

互動式 UI 可以在與驗證通訊協定相同的 DLL 或個別的 DLL 中執行。 此外，用來執行互動式 UI 的 DLL 可支援一個以上的驗證通訊協定。 互動式 UI 的 DLL 路徑會儲存在「 [RAS \_ EAP \_ VALUENAME \_ INTERACTIVEUI](authentication-protocol-registry-values.md) 登錄」值的「驗證通訊協定」機碼下。 如需有關建立此登錄值的詳細資訊，請參閱 [EAP 安裝](eap-installation.md)。

互動式 UI 的 DLL 應匯出下列函數的進入點：<dl>

[**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui)  
[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)  
</dl>

互動式使用者介面必須支援 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) (*WPARAM*) 等於 IDCANCEL 的 [**WM \_ 命令**](../menurc/wm-command.md)訊息。

若要顯示互動式 UI，驗證通訊協定應該將 [**PPP \_ EAP \_ 輸出**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output)結構的 **fInvokeInteractiveUI** 成員設定為 **TRUE**。 驗證通訊協定也可以選擇性地將 **pUICoNtextData** 和 **dwSizeOfUICoNtextData** 成員設為 **TRUE** 。 驗證服務會使用這些成員的值將內容資料傳遞給互動式 UI。 驗證通訊協定會以 [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))函數中的參數傳回 **PPP \_ EAP \_ 輸出** 結構。

驗證服務會藉由呼叫 [**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui)來叫用互動式 UI。 接著，服務會在後續呼叫 [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))時，將互動式 UI 所傳回的資料指標傳遞給驗證通訊協定。 指標會以 [**PPP \_ EAP \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) 結構的成員形式傳遞。 **RasEapMakeMessage** 傳回之後，服務會呼叫 [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)來釋放資訊所佔用的記憶體。 因此，在呼叫 **RasEapMakeMessage** 期間，驗證通訊協定應該會將資訊複製到私用記憶體緩衝區。

 

 