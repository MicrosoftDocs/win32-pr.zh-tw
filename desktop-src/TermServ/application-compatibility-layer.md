---
title: 應用程式相容性層
description: 若要在遠端桌面服務環境中執行繼承應用程式，您可以使用遠端桌面服務應用程式相容性層。
ms.assetid: 6e61ed45-4fcb-4aee-b8cc-638a9b87ce00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3630346578801e4d2578db6f528048914412dc9ad1a8544e2c2d303188814b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099608"
---
# <a name="application-compatibility-layer"></a>應用程式相容性層

若要在遠端桌面服務環境中執行繼承應用程式，您可以使用遠端桌面服務應用程式相容性層。 當遠端桌面工作階段主機 (RD 工作階段主機) 伺服器載入未遠端桌面服務感知的應用程式時，它也會載入包含相容性程式碼的 DLL。 若要使用遠端桌面服務應用程式相容性層級，您可以在編譯應用程式時設定 NOT TSAWARE 旗標。

如果您的應用程式遠端桌面服務感知，您可以避免載入此額外 DLL 並執行相容性程式碼的額外負荷。

若要指出您的應用程式遠端桌面服務感知，請在選用標頭中設定 **IMAGE \_ DLLCHARACTERISTICS \_ TERMINAL \_ SERVER \_ 感知** 旗標。 如果您使用 Microsoft Visual C++ 隨附的連結器，您可以使用 **TSAWARE** 連結器選項來設定這個旗標。 Microsoft Visual C++ 隨附的 **DUMPBIN** 工具提供 */HEADERS* 選項來判斷 **TSAWARE** 旗標的狀態。 如需使用 **DUMPBIN** 工具的詳細資訊，請參閱 [DUMPBIN 參考](/cpp/build/reference/dumpbin-reference?view=vs-2019)。

當您使用 **TSAWARE** 旗標時請小心，因為它可讓您的應用程式略過任何遠端桌面服務相容性優化。 只有當您確定應用程式是針對遠端桌面服務環境而設計時，才應該使用 **TSAWARE** 旗標。 如果您的應用程式符合下列準則，您可以安全地使用「 **映射 \_ DLLCHARACTERISTICS \_ 終端機 \_ 伺服器 \_ 感知** 」旗標。

-   應用程式不會使用 .ini 的檔案。
-   在安裝期間，應用程式不會寫入 **HKEY \_ 目前的 \_ 使用者** 。 如需詳細資訊，請參閱 [儲存 User-Specific 資訊](storing-user-specific-information.md)。
-   應用程式不會以系統服務的形式執行， (也就是 LUID = System) 。
-   應用程式不會預期 Windows 或其他系統目錄的獨佔存取權。 這表示應用程式不會將每個使用者的暫存或設定資料儲存在 Windows 或其他系統目錄中。
-   應用程式不會將使用者特定資料或設定寫入 **HKEY 本機電腦** 登錄 hive。
-   應用程式會遵循本檔中所述的其他遠端桌面服務相容性指導方針。

 

 