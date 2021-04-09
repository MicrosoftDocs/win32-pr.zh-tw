---
description: Windows Installer 開發人員可以撰寫可讓終端使用者使用可設定合併模組的工具。
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: 將模組設定功能新增至合併工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692811"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a>將模組設定功能新增至合併工具

若要讓終端使用者使用可設定的合併模組，您可以撰寫合併和設定工具來執行下列作業：

-   合併工具應該呼叫 Mergemod.dll 版本2.0 中的函式，以合併模組。 舊版的 Mergemod.dll 不能用來設定合併模組。
-   用戶端設定應用程式應與合併模組使用者互動，以收集可設定專案的使用者選擇。
-   合併工具應該將撰寫的設定資訊公開給用戶端應用程式，讓用戶端可以使用此資訊來查詢使用者。
-   當合併工具在合併期間遇到可設定的專案時，應該呼叫用戶端設定工具，以取得從使用者取得的自訂資訊。 合併工具應該對合併模組進行指定的變更。
-   設定應用程式應可讓使用者提供可設定專案的選項，但是所有可能的選項都不需要向使用者顯示。 合併工具可以針對使用者未選取的可設定專案使用預設值。
-   如果使用者未提供自訂資訊，合併工具應該使用合併模組中指定的預設設定值。
-   當使用者提供設定工具的特定選項之後，合併工具會呼叫 Mergemod.dll 來執行合併。

 

 



