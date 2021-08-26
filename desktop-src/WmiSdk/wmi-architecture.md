---
description: WMI 提供統一的介面，可用於從電腦系統、網路或企業取得管理資料的任何本機或遠端應用程式或腳本。
ms.assetid: 41ba2a64-3322-48b8-a6ea-e468bfac06e2
ms.tgt_platform: multiple
title: WMI 架構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e261459785fa4e0ccdce7337df788de007c6f335799bbe4778e80f551f5e519e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995519"
---
# <a name="wmi-architecture"></a>WMI 架構

WMI 提供統一的介面，可用於從電腦系統、網路或企業取得管理資料的任何本機或遠端應用程式或腳本。 統一介面的設計，是為了讓 WMI 用戶端應用程式和腳本不需要呼叫各種不同的操作系統應用程式設計介面， (Api) 。 許多 api 都無法由腳本或 Visual Basic 應用程式等 automation 用戶端呼叫。 其他 Api 不會對遠端電腦進行呼叫。

若要從 WMI 取得資料，請撰寫可存取 [Wmi 類別](wmi-classes.md) 的用戶端腳本或應用程式，或撰寫 [*wmi 提供者*](gloss-p.md)以將資料提供給 WMI。 如需詳細資訊，請參閱 [使用 WMI](using-wmi.md)。

## <a name="objects-consumers-and-infrastructure-of-wmi"></a>WMI 的物件、取用者和基礎結構

下圖顯示 WMI 基礎結構與 WMI 提供者以及受管理物件之間的關聯性，同時也顯示 WMI 基礎結構與 WMI 取用者之間的關聯性。

![wmi 基礎結構、wmi 提供者和 managed 物件之間的關聯性](images/wmi-architecture.png)

## <a name="wmi-components"></a>WMI 元件

下列清單描述主要的 WMI 元件：

-   Managed 物件和 WMI 提供者

    WMI 提供者是一種 COM 物件，可監視一或多個 WMI 的 [*managed 物件*](gloss-m.md) 。 受管理物件是邏輯或實體的企業元件，例如硬碟、網路介面卡、資料庫系統、作業系統、進程或服務。

    與驅動程式類似，提供者會提供 WMI 和 managed 物件的資料，以及處理從 WMI 到 managed 物件的訊息。 WMI 提供者是由 DLL 檔和 [*受控物件格式 (MOF)*](gloss-m.md) 檔所組成，此檔案會定義提供者傳回資料並執行作業的類別。 提供者（例如 WMI c + + 應用程式）會使用 [適用于 wmi 的 COM API](com-api-for-wmi.md)。 如需詳細資訊，請參閱 [將資料提供給 WMI](providing-data-to-wmi.md)。

    提供者的範例是預先安裝的登錄 [提供者](/previous-versions/windows/desktop/regprov/system-registry-provider)，它會存取系統登錄中的資料。 登錄提供者有一個 [*WMI 類別*](gloss-w.md) [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)，具有許多方法，但沒有屬性。 其他預先安裝的提供者（例如 [win32 提供者](/windows/desktop/CIMWin32Prov/win32-provider)）通常具有具有許多屬性的類別，但有少數方法（例如 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 或 [**win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)）。 登錄提供者 DLL 檔案（Stdprov.dll）包含的程式碼會在用戶端腳本或應用程式要求時動態傳回資料。

    WMI MOF 和 DLL 檔案位於% WINDIR% \\ System32 \\ Wbem，以及 [wmi Command-Line 工具](wmi-command-line-tools.md)，例如 [**Winmgmt.exe**](winmgmt.md) 和 [**Mofcomp.exe**](mofcomp.md)。 提供者類別（例如 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)）是在 MOF 檔案中定義，然後在系統啟動時編譯成 WMI 存放庫。

-   [WMI 基礎結構](wmi-infrastructure.md)

    wmi 基礎結構是 Microsoft Windows 作業系統元件，也就是 (winmgmt) 的 wmi 服務。 WMI 基礎結構有兩個元件： WMI 核心和 Wmi 存放 [*庫*](gloss-w.md)。

    WMI 存放庫是由 WMI [*命名空間*](gloss-n.md)所組成。 WMI 服務會在系統啟動時建立一些命名空間，例如根 \\ 預設、根 \\ cimv2 和根 \\ 訂用帳戶，並預先安裝一組預設的類別定義，包括 [Win32 類別](/windows/desktop/CIMWin32Prov/win32-provider)、 [WMI 系統類別](wmi-system-classes.md)和其他命名空間。 在系統上找到的其餘命名空間是由作業系統或產品其他部分的提供者所建立。 如需詳細資訊和大部分作業系統版本中找到的 WMI 提供者清單，請參閱 [Wmi 提供者](wmi-providers.md)。

    WMI 服務可作為提供者、管理應用程式和 WMI 儲存機制之間的媒介。 只有有關物件的靜態資料會儲存在存放庫中，例如提供者所定義的類別。 當用戶端要求時，WMI 會從提供者動態取得大部分的資料。 您也可以設定訂閱，以從提供者接收事件通知。 如需詳細資訊，請參閱 [監視事件](monitoring-events.md)。

-   WMI 取用者

    WMI 取用者是與 WMI 基礎結構互動的管理應用程式或腳本。 管理應用程式可以透過呼叫 [適用于 wmi 的 COM API](com-api-for-wmi.md) 或 [適用于 WMI 的腳本 API](scripting-api-for-wmi.md)，來查詢、列舉資料、執行提供者方法或訂閱事件。 受管理物件（例如磁片磁碟機或服務）唯一可用的資料或動作，就是提供者所提供的資料或動作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WMI](using-wmi.md)
</dt> <dt>

[WMI 提供者](wmi-providers.md)
</dt> <dt>

[建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)
</dt> <dt>

[腳本和應用程式的 WMI 工作](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[將資料提供給 WMI](providing-data-to-wmi.md)
</dt> <dt>

[WMI 類別](wmi-classes.md)
</dt> <dt>

[監視事件](monitoring-events.md)
</dt> <dt>

[呼叫方法](calling-a-method.md)
</dt> </dl>

 

 
