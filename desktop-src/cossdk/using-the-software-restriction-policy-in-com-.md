---
description: 使用軟體限制原則可讓您的企業更具 agile，因為它提供主動式架構來防止問題，而不是依賴在發生問題之後還原系統的昂貴替代方案的被動架構。 軟體限制原則是隨著 Microsoft Windows XP 的發行所引進，可協助保護系統免于不明且可能有危險的程式碼。 限制原則會提供一種機制，其中只有受信任的程式碼會獲得不受限制的使用者許可權存取權。 未知的程式碼可能會包含與目前安裝的程式衝突的病毒或程式碼，只允許在受限制的環境中執行 (通常稱為沙箱) 不允許存取任何安全性敏感的使用者權限。
ms.assetid: 233483a0-ff16-4e21-a312-cc57a92124c3
title: 在 COM + 中使用軟體限制原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e823d794cccf590ddf9ffd8fcb6f7982eb1543368e400ab3632601ec3a2b96e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304934"
---
# <a name="using-the-software-restriction-policy-in-com"></a>在 COM + 中使用軟體限制原則

使用軟體限制原則可讓您的企業更具 agile，因為它提供主動式架構來防止問題，而不是依賴在發生問題之後還原系統的昂貴替代方案的被動架構。 軟體限制原則是隨著 Microsoft Windows XP 的發行所引進，可協助保護系統免于不明且可能有危險的程式碼。 限制原則會提供一種機制，其中只有受信任的程式碼會獲得不受限制的使用者許可權存取權。 未知的程式碼可能會包含與目前安裝的程式衝突的病毒或程式碼，只允許在受限制的環境中執行 (通常稱為 *沙箱*) 不允許存取任何安全性敏感的使用者權限。

軟體限制原則取決於將信任層級指派給可在系統上執行的程式碼。 目前有兩個信任層級：不受限制且不允許。 具有不受限制之信任層級的程式碼會被授與不受限制地存取使用者的許可權，因此此信任層級應只套用至完全信任的程式碼。 具有不允許信任層級的程式碼不允許存取任何安全性敏感使用者許可權，而且只能在沙箱中執行，以協助防止不受限制的程式碼將不允許的程式碼載入其位址空間中。

設定系統的軟體限制原則是透過 [本機安全性原則] 系統管理工具來完成，而個別 COM + 應用程式的限制原則設定則是以程式設計方式或透過 [元件服務] 系統管理工具來完成。 如果未指定 COM + 應用程式的限制原則信任層級，則會使用全系統設定來判斷應用程式的信任層級。 由於具有不受限制的信任層級的 COM + 應用程式只能載入具有不受限制之信任層級的元件，因此 COM + 限制原則設定必須謹慎地與全系統設定協調：不允許的 COM + 應用程式可以載入具有任何信任層級的元件，但無法存取所有使用者的許可權。

除了個別 COM + 應用程式的軟體限制原則信任層級以外，其他兩個屬性會決定如何將限制原則用於所有的 COM + 應用程式。 如果已啟用 [SRPRunningObjectChecks](/windows/desktop/com/srprunningobjectchecks) ，將會檢查是否有適當的信任層級，來嘗試連接到執行中的物件。 執行中的物件不能有比用戶端物件更嚴格的信任層級。 例如，如果用戶端物件具有不受限制的信任層級，則執行中的物件不能有不允許的信任層級。

第二個屬性會決定軟體限制原則如何處理啟動為啟動的連接。 如果啟用 [SRPActivateAsActivatorChecks](/windows/desktop/com/srpactivateasactivatorchecks) ，則會將為伺服器物件設定的信任層級與用戶端物件的信任層級進行比較，並使用更嚴格的信任層級來執行伺服器物件。 如果未啟用 SRPActivateAsActivatorChecks，不論設定的信任層級為何，伺服器物件都會以用戶端物件的信任層級執行。 預設會啟用 SRPRunningObjectChecks 和 SRPActivateAsActivatorChecks。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端驗證](client-authentication.md)
</dt> <dt>

[用戶端模擬和委派](client-impersonation-and-delegation.md)
</dt> <dt>

[設定軟體限制原則](configuring-the-software-restriction-policy.md)
</dt> <dt>

[程式庫應用程式安全性](library-application-security.md)
</dt> <dt>

[多層式應用程式安全性](multi-tier-application-security.md)
</dt> <dt>

[程式設計元件安全性](programmatic-component-security.md)
</dt> <dt>

[以角色為基礎的安全性管理](role-based-security-administration.md)
</dt> </dl>

 

 
