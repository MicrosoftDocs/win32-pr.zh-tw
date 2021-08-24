---
description: 應用程式專屬的效能計數器可協助您在開發和偵測應用程式時微調效能。
ms.assetid: 016386f6-4675-409e-8446-599e4ff96109
title: 新增效能計數器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aaf66d6a0e2f0c98ad0e9fe3cc66069509d4c2391ab74e4ecaa17d6780f4561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033998"
---
# <a name="adding-performance-counters"></a>新增效能計數器

> [!IMPORTANT]
> 由於有顯著的效能和可靠性限制，提供本主題所描述的效能計數器資料的方法，可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用使用 [2.0 版提供計數器資料](providing-counter-data-using-version-2-0.md) 來建立新的效能計數器，以及遷移現有的效能計數器來使用該方法所述的方法。

應用程式專屬的效能計數器可協助您在開發和偵測應用程式時微調效能。 當您的應用程式完成並安裝在目標系統上之後，計數器可協助系統管理員調整您應用程式的可設定設定。

## <a name="adding-a-performance-object-and-its-counters"></a>新增效能物件與其計數器

1. 設計應用程式的物件類型和計數器。 如需詳細資訊，請參閱 [物件和計數器設計](object-and-counter-design.md)。
2. 建立初始化 (.ini) 檔案，其中包含您提供的效能物件和計數器的名稱和描述。 如需詳細資訊，請參閱 [將計數器名稱和描述新增至](adding-counter-names-and-descriptions-to-the-registry.md)登錄。
3. 建立標頭 ( .h) 檔案，其中包含計數器物件和計數器將在登錄中安裝的相對位移。 如需詳細資訊，請參閱 [將計數器名稱和描述新增至](adding-counter-names-and-descriptions-to-the-registry.md)登錄。
4. 在登錄中設定所需的效能監視專案。 這包括下列步驟。
    1. 在應用程式的 **服務** 金鑰中建立登錄機碼。 如果您沒有這類節點，請在下列登錄機碼底下建立它： `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` 。 如需詳細資訊，請參閱 [建立應用程式的效能金鑰](creating-the-applications-performance-key.md)。
    2. 使用 **lodctr** 公用程式搭配 .ini 和 .h 檔案，在登錄中安裝資訊。 只有當應用程式的 **服務** 金鑰中有效能金鑰時，此公用程式才會成功。 如需詳細資訊，請參閱 [將計數器名稱和描述新增至](adding-counter-names-and-descriptions-to-the-registry.md)登錄。
5. 建立包含一組匯出函數的效能 DLL，這些函式會將查詢的計數器資料提供給取用者。 如需詳細資訊，請參閱 [建立效能延伸模組 DLL](creating-a-performance-extension-dll.md)。
6. 修改應用程式的安裝檔案，以自動將資訊新增至登錄 (如步驟 4) 所述，並在安裝時將效能 DLL 複製到應用程式的目錄。

如需其他登錄專案的詳細資訊，請參閱 [建立其他登錄專案](creating-other-registry-entries.md)。
