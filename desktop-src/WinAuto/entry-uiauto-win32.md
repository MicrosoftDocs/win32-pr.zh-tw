---
title: UI 自動化
description: Microsoft 消費者介面自動化是一種協助工具架構，可讓 Windows 應用程式提供使用者介面的程式設計相關資訊， (Ui) 。
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8006c79299cc1f736dc43555968443f634d4a51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842540"
---
# <a name="ui-automation"></a>UI 自動化

Microsoft 消費者介面自動化是一種協助工具架構，可讓 Windows 應用程式提供使用者介面的程式設計相關資訊， (Ui) 。 它可讓您以程式設計方式存取桌面上大部分的 UI 元素。 它可讓輔助技術產品（例如螢幕讀取器）提供使用者介面的相關資訊給使用者，以及透過標準輸入以外的方式操作 UI。 消費者介面自動化也可讓自動化測試腳本與 UI 互動。

-   [適用時](#where-applicable)
-   [開發人員物件](#developer-audience)
-   [執行時間需求](#run-time-requirements)
-   [舊版作業系統的支援](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a>適用情況

藉由使用消費者介面自動化和遵循可存取的設計實務，開發人員可以讓具有視覺、聽力或動作障礙的許多人更容易存取在 Windows 上執行的應用程式。 此外，消費者介面自動化是特別設計來提供適用于自動化測試案例的強大功能。

## <a name="developer-audience"></a>開發人員讀者

消費者介面自動化是專為有經驗的 C/c + + 開發人員所設計。 一般來說，開發人員需要對元件物件模型進行中等程度的瞭解， (COM) 物件和介面、Unicode 和 Windows API 程式設計。

如需受控碼消費者介面自動化的詳細資訊，請參閱 MSDN 上 .NET Framework 開發人員指南》一節中的 [協助工具](/dotnet/framework/ui-automation/) 。

## <a name="run-time-requirements"></a>執行階段需求

下列作業系統支援消費者介面自動化： Windows XP、Windows Server 2003、Windows Server 2003 R2、Windows Vista、Windows 7、Windows 10、Windows Server 2008、Windows Server 2008 R2、Windows Server 2012、Windows Server 2012 R2、Windows Server 2016 以及 Windows Server 2019。

> [!Note]  
> Windows XP 和 Windows Server 2003 也需要 Microsoft .NET Framework 3.0。

 

## <a name="support-for-down-level-operating-systems"></a>舊版作業系統的支援

Windows Vista 的平臺更新是一組執行時間程式庫，可讓開發人員將應用程式的目標設為 Windows 7 和下層作業系統。 Windows Server 2008 的平臺更新是一組執行時間程式庫，可讓開發人員將應用程式的目標設定為 Windows Server 2008 R2 和舊版的 Windows Server。 所有 Windows Vista 和 Windows Server 2008 客戶都可以透過 Windows Update，取得 Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新。 需要適用于 Windows Vista 或 Windows Server 2008 平臺更新的協力廠商應用程式，可以 Windows Update 偵測是否已安裝;如果不是，Windows Update 會在背景中下載並安裝它。

適用于 Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新都支援下列作業系統上的整個 Windows Automation API 3.0 功能集。

-   Windows XP (英文)  <dl> Windows XP Home SP3 x86  
    Windows XP Professional SP3 x86  
    </dl>
-   Windows Server 2003 (English) <dl> Windows Server 2003 SP2 (x86 和 x64)   
    </dl>
-   Windows Vista (英文)  <dl> Starter SP2 (x86 和 x64)   
    Home Premium SP2 (x86 和 x64)   
    Business SP2 (x86 和 x64)   
    Enterprise SP2 (x86 和 x64)   
    終極 SP2 (x86 和 x64)   
    </dl>
-   Windows Server 2008 (英文)  <dl> Windows Server 2008 SP2 (x86 和 x64)  
    </dl>

如需這兩項更新的詳細資訊，請參閱 [Windows Vista 的平臺更新](../win7ip/platform-update-for-windows-vista-portal.md)。

## <a name="in-this-section"></a>本節內容

-   [UI 自動化基礎](entry-uiautocore-overview.md)
-   [消費者介面自動化提供者程式設計人員指南](uiauto-providerportal.md)
-   [消費者介面自動化用戶端程式設計人員指南](uiauto-clientportal.md)
-   [參考](entry-uiautocore-ref.md)
-   [範例](samples-entry.md)
-   [附錄](appendix-entry.md)

 

 