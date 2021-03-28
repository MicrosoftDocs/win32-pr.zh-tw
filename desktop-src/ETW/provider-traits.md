---
description: 提供者特性是將更多資料附加至個別提供者註冊的方法。
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: 提供者特性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c67b25857070edb6419be9a2898d2667f3a179d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973569"
---
# <a name="provider-traits"></a>提供者特性

提供者特性是將更多資料附加至個別提供者註冊的方法。 它們可用於以資訊清單為基礎或 TraceLogging 的提供者。 目前支援將提供者名稱和/或提供者群組新增至個別提供者註冊。 未來可能會加入更多特性類型。 這項資訊會以集合格式的二進位 blob 形式儲存在核心中。

您只能針對註冊設定一次特性。 任何進一步嘗試在該註冊上設定特性的嘗試都會失敗。

若要在以資訊清單為基礎的提供者上設定提供者特性，請使用 EventProviderSetTraits 資訊類別呼叫 [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) 函數。 EventInformation 緩衝區應包含下列格式的二進位 blob：

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

個別的特性應該採用下列格式：

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

從個別的特性，ETW \_ 提供者特性 \_ \_ 類型定義如下：

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

呼叫 [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) 函數時，TraceLogging 提供者會自動設定提供者特徵。 TraceLogging 提供者的名稱一律會包含在其特性中。 您可以在提供者定義中使用 [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) 宏，在 TraceLogging 提供者上設定群組。

## <a name="custom-traits"></a>自訂特性

雖然可能尚未定義大部分的255可能特性類型，但特性類型1-127 是由 Microsoft 所保留供定義。 其餘較高的索引類型值可供外部開發人員使用，如其所見。 考慮將自己的自訂特性新增至提供者的任何人，都應該嘗試將其特徵大小總計保持在256個位元組以下，原因如下：

-   這些特性會包含在針對提供者所撰寫的每個事件中。 大型特性可能會導致大量記錄檔。
-   在提供者的存留期內，特性會儲存在非分頁核心集區中。

## <a name="provider-groups"></a>提供者群組

提供者群組是 GUID 定義的可控制實體，與提供者本身很類似。 主要差異在於，雖然提供者 GUID 只會用來控制其提供者的註冊，但群組將會控制其所有成員註冊。 例如，啟用具有指定關鍵字和層級的提供者群組，將會啟用所有群組成員註冊與該關鍵字和層級。

群組成員資格可能會受到許可權限制。 如果 [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) 的呼叫端沒有加入指定群組的許可權，則會拒絕成員資格。

在某些情況下，追蹤會話控制器可能會想要從其啟用群組中排除幾個提供者。 這可以藉由設定不允許的清單來完成。 不允許的清單是提供者 Guid 清單，將不會根據單一記錄會話的群組設定來啟用。 您可以使用 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 和 TraceSetDisallowList 資訊類別，動態變更不允許的清單。

雖然可以針對個別提供者以類似的方式針對提供者群組進行大部分的啟用動作，但還是有一些例外狀況。 例外狀況包括：

-   私用追蹤會話無法控制提供者群組。
-   當提供者群組採用個別提供者的特定資訊時，事件名稱、事件識別碼和裝載篩選器並不適用。

 

 
