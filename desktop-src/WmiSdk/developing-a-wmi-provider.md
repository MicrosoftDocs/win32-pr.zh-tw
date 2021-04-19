---
description: 提供者是元件物件模型 (COM) 物件，可作為 WMI 和 managed 物件之間的媒介。
ms.assetid: a4f537ba-9081-43b4-acff-4d206de3d9d7
ms.tgt_platform: multiple
title: 開發 WMI 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9249c251f75f08f9e5142e70a507b0dced8f91df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000270"
---
# <a name="developing-a-wmi-provider"></a>開發 WMI 提供者

提供者是元件物件模型 (COM) 物件，可作為 WMI 和 managed 物件之間的媒介。 例如，當應用程式或腳本使用 WMI [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別來要求磁片資料時，會透過預先安裝的 [Win32 提供者](/windows/desktop/CIMWin32Prov/win32-provider)動態取得資料。

如果您想要透過 WMI 提供資料給其他應用程式，您可以藉由撰寫 COM 伺服器或透過 Visual Studio 中的 **WMI ATL 嚮導** 來建立非受控程式碼提供者。 您可以使用 .NET Framework 中的 WMI 來撰寫 managed 程式碼提供者。 本節中的主題描述撰寫非受控 COM 提供者的程式。

> [!Note]  
> 若要確保在 WMI 發生失敗並重新啟動時，受管理物件的所有 WMI 類別定義都會還原至 [*wmi 儲存*](gloss-w.md)機制，請使用受控物件格式 (MOF) 檔中的 [**\# pragma 自動**](pragma-autorecover.md)復原預處理器指令。

 

提供者是由 [*受控物件格式 (MOF)*](gloss-m.md) 架構中定義的類別，以及執行提供者功能的 DLL 檔案所組成。 例如，定義 Win32 提供者類別的 MOF 為 CIMWin32，而 DLL 是 CIMWin32.dll，這兩者都位於% windir% \\ System32 \\ Wbem 中。

提供者的 MOF 架構可能包含數種提供者類型。 例如， [事件記錄提供者](/previous-versions/windows/desktop/eventlogprov/event-log-provider) 在名為 Ntevt 的一個 mof 檔案中有實例、方法和事件提供者類型。 建議將相關提供者的所有類別和註冊架構組合在一個檔案中，而不是為每個類別建立一個檔案。

除了使用預先安裝的提供者之外，您還可以建立自己的提供者，以提供硬體裝置或軟體作業的相關資訊。

下表列出建立提供者的基本工作。



| Task                                                                                                                                                            | Description                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)                                                              | 針對您想要透過 WMI 管理的實體開發模型，並建立受控物件格式 (MOF) 檔來描述架構。<br/> |
| [藉由撰寫提供者，將資料提供給 WMI](supplying-data-to-wmi-by-writing-a-provider.md)                                                                  | 建立與 WMI 結合的最基本提供者。<br/>                                                                                |
| [將提供者併入應用程式中](incorporating-a-provider-in-an-application.md)                                                                    | 將提供者包含在應用程式中的元件（如果沒有全部時間執行）。<br/>                                         |
| [註冊提供者](registering-a-provider.md)                                                                                                            | 向 COM 和 WMI 註冊提供者。<br/>                                                                                               |
| [初始化提供者](initializing-a-provider.md)                                                                                                          | 執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 和 [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) 介面。<br/>   |
| [對 WMI 進行呼叫](making-calls-to-wmi.md)                                                                                                                  | 從提供者呼叫 WMI 介面。<br/>                                                                                                  |
| [模擬用戶端](impersonating-a-client.md)                                                                                                            | 設定安全性以存取用戶端應用程式。<br/>                                                                                          |
| [更新提供者](updating-a-provider.md)                                                                                                                  | 視需要改善提供者。<br/>                                                                                                       |
| [卸載提供者](unloading-a-provider.md)                                                                                                                | 在關機期間或提供者閒置時，從記憶體中移除提供者。<br/>                                                         |
| 偵測[提供者](debugging-providers.md)和[提供者設定和疑難排解類別](provider-configuration-and-troubleshooting-classes.md) | 使用 WMI 提供的功能來對提供者進行 Debug 錯。<br/>                                                                                 |
| [在64位電腦上取得和提供資料](getting-and-providing-data-on-a-64-bit-computer.md)                                                          | 評估您是否需要32位的應用程式相容性提供者，或如果64位提供者可提供資料給這兩個用戶端。<br/>      |



 

下列主題討論撰寫不同類型的提供者所需的步驟：

-   [撰寫執行個體提供者](writing-an-instance-provider.md)
-   [撰寫方法提供者](writing-a-method-provider.md)
-   [撰寫事件提供者](writing-an-event-provider.md)
-   [撰寫事件取用者提供者](writing-an-event-consumer-provider.md)
-   [撰寫類別提供者](writing-a-class-provider.md)
-   [撰寫屬性提供者](writing-a-property-provider.md)
-   [讓執行個體提供者成為 High-Performance 提供者](making-an-instance-provider-into-a-high-performance-provider.md)

 

