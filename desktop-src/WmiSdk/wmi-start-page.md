---
description: Windows Management Instrumentation (WMI) 是在以 Windows 為基礎的作業系統上管理資料和作業的基礎結構。
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Windows Management Instrumentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec2313ca7ee744ebe6f14be42a33e2e5878960b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983427"
---
# <a name="windows-management-instrumentation"></a>Windows Management Instrumentation

## <a name="purpose"></a>目的

Windows Management Instrumentation (WMI) 是在以 Windows 為基礎的作業系統上管理資料和作業的基礎結構。 您可以撰寫 WMI 腳本或應用程式將遠端電腦上的系統管理工作自動化，但是 WMI 也會提供管理資料給作業系統和產品的其他部分，例如 System Center Operations Manager、先前 Microsoft Operations Manager (MOM) 或 Windows 遠端管理 [WinRM](/windows/desktop/WinRM/portal) (。

> [!Note]  
> 下列檔的目標是開發人員和 IT 系統管理員。 如果您是遇到關於 WMI 的錯誤訊息的使用者，您應該移至 [Microsoft 支援服務](https://support.microsoft.com/) 並搜尋錯誤訊息上所看到的錯誤碼。 如需有關疑難排解 WMI 腳本和 WMI 服務問題的詳細資訊，請參閱 [Wmi 無法運作！](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

> [!Note]  
> Microsoft 完全支援 WMI;不過，您可以透過 Windows 管理基礎結構 (MI) 來取得最新版本的系統管理腳本和控制項。 MI 與舊版 WMI 完全相容，並提供一系列的功能和優點，讓設計和開發提供者和用戶端比以往更容易。 如需詳細資訊，請參閱 [Windows 管理基礎結構 (MI) ](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)。

 

## <a name="where-applicable"></a>適用時

WMI 可以用在所有 Windows 應用程式中，最適合用於企業應用程式和系統管理腳本。

系統管理員可以在 TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)找到有關使用 wmi 的資訊，以及有關 wmi 的各種書籍。 如需詳細資訊，請參閱 [進一步的資訊](further-information.md)。

## <a name="developer-audience"></a>開發人員對象

WMI 是設計給使用 C/c + +、Microsoft Visual Basic 應用程式的程式設計人員，或是在 Windows 上具有引擎的指令碼語言，並處理 Microsoft ActiveX 物件。 雖然對 COM 程式設計的熟悉程度很有説明，但是撰寫應用程式的 c + + 開發人員可以找到良好的範例，讓您開始 [使用 c + + 建立 WMI 應用程式](creating-a-wmi-application-using-c-.md)。

若要使用 .NET Framework 來開發 c # 或 Visual Basic .NET 中的 managed 程式碼提供者或應用程式，請參閱 [.NET Framework 中的 WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))。

許多系統管理員和 IT 專業人員透過 PowerShell 存取 WMI。 適用于 PowerShell 的 Get-WMI 指令程式可讓您取得本機或遠端 WMI 儲存機制的資訊。 因此，許多主題和類別（特別是在 [建立 WMI 用戶端](creating-wmi-clients.md) 一節中）包含 PowerShell 範例。 如需使用 PowerShell 的詳細資訊，請參閱使用 Windows PowerShell [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) 和 [腳本](https://technet.microsoft.com/library/bb978526.aspx)。

## <a name="run-time-requirements"></a>執行階段需求求

如需有關使用特定 API 元素或 WMI 類別之作業系統的詳細資訊，請參閱 WMI 檔中每個主題的需求一節。

如果預期的元件似乎遺失，請參閱 [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md)。

您不需要下載或安裝特定軟體發展 (SDK) ，就能建立 WMI 的腳本或應用程式。 不過，有一些 WMI 系統管理工具可讓開發人員覺得有用。 如需詳細資訊，請參閱「下載」一節中的詳細 [資訊](further-information.md)。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[關於 WMI](about-wmi.md)
</dt> <dd>

WMI 的一般資訊。

</dd> <dt>

[使用 WMI](using-wmi.md)
</dt> <dd>

有關如何開發應用程式以使用 WMI 的資訊，其中包括工具的相關資訊。

</dd> <dt>

[WMI 參考](wmi-reference.md)
</dt> <dd>

WMI 類別、WMI c + + 類別、WMI COM API、腳本 API 和其他 WMI 參考資料的相關檔。

</dd> </dl>

 

 
