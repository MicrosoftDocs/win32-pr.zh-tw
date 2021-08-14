---
description: 插入式終端機實施的一般需求如下所示。
ms.assetid: 7cee19b1-ceea-494a-b576-4deede759905
title: 執行可插入的終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a75dd7b085377c8474c9a89d74a297c3ca66c6740c01c7428e7b6f250e16c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762900"
---
# <a name="implementing-pluggable-terminals"></a>執行可插入的終端機

插入式終端機實施的一般需求為：

-   可插入的終端機基礎串流程式碼應符合所需 Msp 的功能。
-   終端機必須使用 DirectShow 濾波器來處理大部分的 msp (這是在) 上假設。
-   音訊終端機必須支援 8 kHz 16 位 mono 線性 PCM，才能進行大部分的 Msp。
-   終端機應該藉由執行 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)來啟用自由執行緒封送處理。 終端機可以藉由呼叫 COM API [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) ，並將 **IMarshal** 匯總至傳回的指標來完成這項作業。 終端物件的函式應該呼叫 [**IMarshal >版本**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)。
-   終端機應執行或匯總任何適當的其他終端機特定介面。
-   終端機執行必須是安全線程。
-   終端機執行必須 \# 針對 [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol)定義包含 Termmgr。 這是 Windows 2000 SP1 下的 tapi 3 或 tapi 3 應用程式所需的一般包含和程式庫的補充。

介面和方法的執行附注：

終端機必須執行 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) (雙重介面– Vtable + [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)) 。

[**ITTerminal：： get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)

終端機必須傳回您所挑選 GUID 的 **BSTR** 標記法，以識別您的終端機類型。 透過 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)配置 **BSTR** 。 若要從 GUID 轉換成 **BSTR**，請呼叫 [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)、 **SysAllocString** 和 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)。

[**ITTerminal：： get \_ TerminalType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype)

如果應用程式會執行終端機，終端機通常應該會傳回 TT \_ DYNAMIC。 傳回 TT \_ 靜態也會正常運作，如果終端機對應至硬體裝置，則傳回此值可能很適當; 不過，這麼做可能會對使用者造成混淆，因為 MSP 的靜態終端機列舉中不會有靜態終端機。

[**ITTerminal：： get \_ 狀態**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)

如果終端機執行不會任意限制終端機可同時連接的資料流程數目，則終端機應該一律傳回 TS \_ NOTINUSE。

否則，終端機執行會任意限制終端機可連接的資料流程數目。 在此情況下，終端機應該會保留它所連接的資料流程數目。 終端機應該在成功的 [**ITTerminalControl：： ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) 呼叫上遞增此內部計數，並在成功的 ITTerminalControl 上將它遞減 [**：:D isconnectterminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal) 呼叫。 在 [**ITTerminal：： get \_ 狀態**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)中， \_ 如果此計數等於可以一次選取終端機的資料流程數目上限，則應該傳回 ts INUSE; 否則，它應該會傳回 ts \_ NOTINUSE。 請注意，如果限制為1，則計數可以是布林值或終端 \_ 狀態值。

[**ITTerminal：： get \_ Name**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_name)

終端機會傳回其選擇的 **BSTR** 名稱，並透過 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)配置。 此名稱對使用者應該有意義，而且應該進行當地語系化。

[**ITTerminal：：取得 \_ 媒體媒體**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)

終端機應該會傳回它的媒體類型，也就是 TAPIMEDIATYPE \_ 音訊或 TAPIMEDIATYPE \_ 影片。

[**ITTerminal：： get \_ 方向**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_direction)

終端機會傳回終端 \_ 方向列舉值，指出終端機的方向。 如果終端機為雙向 (例如，橋接器) ，則必須傳回 TD \_ 雙向。

終端機必須只) 執行 [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) (vtable。

[**ITTerminalControl：： get \_ AddressHandle**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-get_addresshandle)

應用程式提供的終端機應該一律傳回 **Null** 作為位址控制碼。 這會向 MSP 指出此終端機未建立在特定的 MSP 位址物件上。

[**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal)

在此呼叫中，終端機會將其篩選 () 新增至指定的圖形，並將它們彼此連接（如果適用）。 然後，終端機會針對指定的資料流程方向，傳回終端機 (s) 所公開的 pin。

不支援並行連接至多個資料流程的終端機，會 \_ 在此方法成功完成時，將內部變數設定為 TS INUSE。

終端機可以使用此呼叫中的 *dwTerminalDirection* 參數，來判斷其所連接的資料流程方向。 雙向終端機需要這項功能。

> [!Note]  
> 通常 (在 MSP 基類和所有已知的 Msp) 中，如果終端機從單一 [**ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) 呼叫傳回一個以上的 pin，則 msp 串流程式碼將會使連接失敗。 這是很好的，因為在連線期間傳回一個以上 pin 的終端機需要 MSP 具有終端機的特殊知識，才能有效使用額外的 pin。

 

[**ITTerminalControl::CompleteConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-completeconnectterminal)

終端機應該只傳回 \_ [確定]。 終端機也可以視需要進行連線初始化。

[**ITTerminalControl：:D isconnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal)

終端機應該進行將終端機與圖形其餘部分中斷連線所需的任何動作。 這通常牽涉到從圖形中移除所有終端機篩選，並將終端機狀態設定為 TS \_ NOTINUSE。

[**ITTerminalControl::RunRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-runrenderfilter)

終端機應該只傳回 E \_ >notimpl。

[**ITTerminalControl::StopRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-stoprenderfilter)

終端機應該只傳回 E \_ >notimpl。

 

 
