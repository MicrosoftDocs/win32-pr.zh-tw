---
title: 軟體限制原則
description: Windows XP 版推出的軟體限制原則 (SRP) 設定，可協助保護系統免于不明且可能有危險的程式碼。
ms.assetid: 44b4e448-f5b4-4483-b53b-506938b36857
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23176b23be5fcf4dc45f040f53e5d8f9dfbcdf05a8aee87feabd125d05c5372d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129800"
---
# <a name="software-restriction-policy"></a>軟體限制原則

Windows XP 版推出的軟體限制原則 (SRP) 設定，可協助保護系統免于不明且可能有危險的程式碼。 SRP 提供一種機制，其中只有受信任的程式碼會獲得不受限制的使用者許可權存取權。 未知的程式碼可能會包含與目前安裝的程式衝突的病毒或程式碼，只允許在受限制的環境中執行 (通常稱為 *沙箱*) 不允許存取任何安全性敏感的使用者權限。 正確地使用 SRP 可讓您的業務更敏捷，因為它提供主動式架構來防止問題，而不是依賴在發生問題之後還原系統的昂貴替代方案的被動架構。

SRP 相依于將信任層級指派給可在系統上執行的程式碼。 目前有兩個信任層級：不受限制且不允許。 具有不受限制之信任層級的程式碼會被授與不受限制地存取使用者的許可權，因此此信任層級應只套用至完全信任的程式碼。 具有不允許信任層級的程式碼不允許存取任何安全性敏感使用者許可權，而且只能在沙箱中執行，因此不受限制的程式碼無法將不允許的程式碼載入其位址空間中。

個別 COM 應用程式的 SRP 設定是透過登錄中應用程式[AppID](appid-key.md)機碼中的[SRPTrustLevel](srptrustlevel.md)值來完成。 如果未指定 COM 應用程式的 SRP 信任層級，則會使用不允許的預設值。 具有不受限制之信任層級的 COM 應用程式可不受限制地存取使用者的許可權，但只能載入具有不受限制之信任層級的元件，而不允許的 COM 應用程式則可以載入具有任何信任層級的元件，但無法存取任何安全性敏感的使用者許可權。

除了個別 COM 應用程式的 SRP 信任層級，另外還有兩個 SRP 屬性會決定如何將 SRP 用於所有 COM 應用程式。 如果已啟用 [SRPRunningObjectChecks](srprunningobjectchecks.md) ，將會檢查是否有適當的 SRP 信任層級，以嘗試連接到正在執行的物件。 執行中的物件不能有比用戶端物件更嚴格的 SRP 信任層級。 例如，如果用戶端物件具有不受限制的信任層級，則執行中的物件不能有不允許的信任層級。

第二個屬性會決定 SRP 如何處理 activate as activator 連接。 如果啟用 [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md) ，則會將為伺服器物件設定的 srp 信任層級與用戶端物件的 srp 信任層級進行比較，並使用更嚴格的信任層級來執行伺服器物件。 如果未啟用 **SRPActivateAsActivatorChecks** ，伺服器物件會以用戶端物件的 srp 信任層級執行，而不論其設定所在的 srp 信任層級為何。 預設會啟用 **SRPRunningObjectChecks** 和 **SRPActivateAsActivatorChecks** 。

 

 




