---
description: Windows Driver Model (WDM) 提供者會授與符合 WDM 模型的硬體驅動程式之類別、實例、方法和事件的存取權。
ms.assetid: 8686a613-0e53-4e6e-b193-7839abfb70de
ms.tgt_platform: multiple
title: 從設備磁碟機存取資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bec478f83ddbc6d58419710fb868ddd233f820a06004210c1dac495de86b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131911"
---
# <a name="accessing-data-from-device-drivers"></a>從設備磁碟機存取資料

Windows Driver Model (WDM) 提供者會授與符合 WDM 模型的硬體驅動程式之類別、實例、方法和事件的存取權。 硬體驅動程式的類別位於 \\ \\ 根 \\ wmi 命名空間中。

對於撰寫設備磁碟機和對設備磁碟機資料有興趣的系統管理員而言，WDM 提供者很感興趣。

本主題將討論下列各節：

-   [設備磁碟機寫入器的資訊](#information-for-device-driver-writers)
-   [驅動程式資料的系統管理員和使用者資訊](#information-for-administrators-and-users-of-driver-data)
-   [相關主題](#related-topics)

## <a name="information-for-device-driver-writers"></a>設備磁碟機寫入器的資訊

當 WDM 提供者從設備磁碟機可執行檔中解壓縮二進位 MOF 時，會建立與特定設備磁碟機相關的 WMI 類別。 每次啟動 WMI、安裝新的設備磁碟機，或刪除特定驅動程式的 [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) 實例時，就會發生這種情況。 藉由檢查 Wmiprov，您可以判斷在解壓縮二進位 MOF 檔案時，是否發生錯誤。 [Mofcomp.exe](mofcomp.md)錯誤的詳細資料會在 mofcomp.exe 中報告。 如需詳細資訊，請參閱 [WMI 記錄](wmi-log-files.md)檔。 基於效能的考慮，由於 WDM 提供者啟動或停止，因此，WDM 提供者不會在建立或刪除類別時產生事件。

WDM 提供者會將所有 WNODE 的資料轉換成類別資訊。 如果將資料從 WNODE 轉換成類別資料時遇到錯誤，則會在 Wmiprov 中報告此標頭，並以與記憶體傾印相同的格式轉譯位元組。

在將 WDM 提供者卸載並重載之前，對驅動程式安全性設定所做的變更不會生效。 如需詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。

WMI 也可以讓硬體驅動程式使用高效能計數器。 如需有關建立高效能類別以及在 Perfmon 系統監視器中顯示資料的詳細資訊，請參閱 [改善執行個體提供者的效率](improving-the-efficiency-of-an-instance-provider.md)。 如需有關撰寫啟用 WMI 之設備磁碟機的詳細資訊，請參閱 [https://www.microsoft.com/ddk](https://msdn.microsoft.com/library/aa972908.aspx) 。 如需 MOF 檔案中的 WDM 特定限定詞的詳細資訊，請參閱 [**Wdm 提供者專屬的限定詞**](qualifiers-specific-to-the-wdm-provider.md)。

## <a name="information-for-administrators-and-users-of-driver-data"></a>驅動程式資料的系統管理員和使用者資訊

列出 [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) 類別的實例會提供系統中的驅動程式清單，以及有關 WDM 提供者是否成功編譯每個驅動程式之 mof 的資訊。 您可以藉由刪除代表該驅動程式的 WMIBinaryMofResource 實例，來強制提供者重新編譯和重新產生驅動程式的類別。 [Mofcomp.exe](mofcomp.md)錯誤的詳細資料會在 mofcomp.exe 中報告。

如果 WMI 命名空間已損毀，則可以將它刪除並重新開啟，以強制執行 WDM 重建驅動程式類別。 如需有關開啟命名空間的詳細資訊，請參閱 [在 WMI 中建立](creating-hierarchies-within-wmi.md)階層。

驅動程式類別有時可能會在驅動程式載入中斷或其他異常操作時發生「擱置」。 當安裝新的驅動程式或 **軟體 \\ Microsoft \\ WBEM \\ WDMProvider** 登錄機碼值 **PROCESSSTRANDEDCLASSES** 設定為 **TRUE** 時，WDM 提供者只會搜尋和清除「擱置」類別。 將此值設定為 **TRUE** 會使 WMI 啟動效能變慢，因為清除作業。 預設值為 **FALSE**。 當 \\ 第一次開啟「根 Wmi」命名空間時，WDM 提供者只會檢查這個登錄值。

如果對 WDM 設備磁碟機進行安全性變更，在將 WDM 提供者卸載並重載之前，變更將不會生效。 Windows 管理服務必須停止並重新啟動，才能完成此動作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WMI](using-wmi.md)
</dt> </dl>

 

 
