---
title: 存取範圍和全球支援
description: Windows 7 平臺可讓您更輕鬆地建立可供更多使用者存取且符合或超過存取範圍合規性標準的解決方案。
ms.assetid: bcad2f00-7885-461c-a2dc-0a0a176962b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320f6e52dba4f2a6d9c89a7bdea287e948a1bca048b0d3e88a2a8978e8085d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709115"
---
# <a name="accessibility-and-global-support"></a>存取範圍和全球支援

Windows 7 平臺可讓您更輕鬆地建立可供更多使用者存取且符合或超過存取範圍合規性標準的解決方案。  (ATV) 的輔助技術廠商現在可以為各式各樣的用戶端應用程式建立解決方案，而應用程式開發人員會發現建立和驗證可存取的使用者介面更容易。

Windows 7 也可讓您比舊版 Windows 更容易支援多種通用語言。 從使用者選取語言和位置時，Windows 7 會使用客戶預期的文化特性慣例來呈現日期、數位、行事曆、定序和其他資訊。

## <a name="windows-automation"></a>Windows自動化

Windows 7 提供豐富、以標準為基礎的自動化層，可針對原生應用程式進行擴充。 它是以 Microsoft Active Accessibility 和 Microsoft 消費者介面自動化為基礎。 它也是設計來處理業界標準，例如 W3C Web ARIA (可存取的豐富網際網路應用程式) 和 *508 節的規格*。

消費者介面自動化藉由為 Microsoft Win32 控制項和舊版 Microsoft Active Accessibility 引進更快的非受控自動化 proxy， (*MSAA*) 應用程式，以及更快且更快速的消費者介面自動化事件和 proxy 註冊，提供更佳的效能。 新的擴充性功能可擴充控制項模式、屬性和自訂事件。  (參閱[Windows 自動化 API：總覽](../winauto/windows-automation-api-overview.md). ) 

## <a name="accessibility-support-tools"></a>協助工具支援工具

UI 協助工具檢查工具是方便的圖形化使用者介面工具，可讓開發人員和測試人員快速驗證其 UI 是否符合重要的協助工具需求，例如 *MSAA* (可驗證子系的關聯性或周框矩形) 和消費者介面自動化程式設計存取、事件產生、配置和鍵盤流覽。  (查看 [UI 協助工具檢查](https://www.codeplex.com/AccCheck)程式。 ) 

UIA Verify 是一種測試自動化架構，可針對控制項或應用程式的消費者介面自動化提供者的執行進行手動和自動化測試。 這兩項新工具可讓開發人員在使用 *MSAA* 或消費者介面自動化的應用程式中測試協助工具的執行方式和功能。 這兩種工具都可透過 [CodePlex](https://www.codeplex.com/)取得，這是 Microsoft 為了裝載開放原始碼專案所建立的網站，並可為開發人員群體提供更好的服務。  (請參閱 [消費者介面自動化驗證 (UIA 確認) 測試自動化架構](https://uiautomationverify.codeplex.com/)。 ) 

## <a name="improved-multi-language-user-interface-support-and-linguistic-services"></a>改良的多語言消費者介面支援和語言服務

Windows 7 為開發人員提供了一種標準方法，讓開發人員可以在其應用程式中使用改良的多語言使用者介面支援和語言服務，為國際市場準備應用程式。

擴充的語言服務是 Windows 7 中的一項新功能，可讓開發人員使用相同的一組 api 來利用各種先進的語言功能。 藉由使用 Windows 7 中的擴充語言 ServicesAPIs，開發人員可以自動偵測任何部分 Unicode 文字的語言，並使用該資訊來協助為世界各地的客戶提供更聰明的使用者經驗選擇。 擴充語言服務也提供內建的音譯支援，可將文字從一個書寫系統轉換成另一個。 例如，開發人員現在可以在簡體中文和繁體中文之間自動轉換文字，以協助人們跨語言界限互相通訊。 藉由使用擴充的語言 ServicesAPIs，開發人員將能夠使用現有的擴充語言服務，並在日後挑選新的服務，而不需要學習新的程式碼。  (參閱 [擴充語言服務](../intl/extended-linguistic-services.md)。 ) 

 

 