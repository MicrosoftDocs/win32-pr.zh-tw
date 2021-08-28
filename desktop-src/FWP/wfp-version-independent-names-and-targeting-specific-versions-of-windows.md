---
title: 以 Windows 的特定版本為目標的 WFP Version-Independent 名稱和目標
description: 在許多情況下，Windows 的篩選平臺 (WFP) API 會提供一個以上版本的函式或結構。
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf5fbef08c3284d94eb215e0cce2fc44fc9b827b686e531057db22b60020132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766668"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a>以 Windows 的特定版本為目標的 WFP Version-Independent 名稱和目標

在許多情況下，Windows 的篩選平臺 (WFP) API 會提供一個以上版本的函式或結構。

WFP API 中大部分的資料和函式名稱都是以版本號碼結尾，例如 "0" 或 "1"，即使只有一個版本也是一樣。

## <a name="version-mapping-in-fwpvih"></a>Fwpvi 中的版本對應

從 Windows 7 SDK 和 WDK 開始包含 fwpvi .h 標頭檔。 此標頭檔會將無版本 API 名稱對應至適用于指定作業系統的版本。

例如，以下是 Windows 8 SDK 中包含的 fwpvi 版本的簡短摘要。


```C++
#define FwpmNetEventCreateEnumHandle FwpmNetEventCreateEnumHandle0
#if (NTDDI_VERSION >= NTDDI_WIN8)
#define FwpmNetEventEnum FwpmNetEventEnum2
#elif (NTDDI_VERSION >= NTDDI_WIN7)
#define FwpmNetEventEnum FwpmNetEventEnum1
#else
#define FwpmNetEventEnum FwpmNetEventEnum0
#endif
```



如上所示，只有一個版本的 **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) –因此任何對 **FwpmNetEventCreateEnumHandle** 的呼叫一律會呼叫 **FwpmNetEventCreateEnumHandle0**，不論目標作業系統為何。

不過，有三種版本的 **FwpmNetEventEnum**： [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0)、 [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)和 [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)。 Fwpvi .h 標頭檔可確保對 **FwpmNetEventEnum** 的呼叫將會呼叫最適合目標作業系統的版本：

-   Windows 8 (或更新版本的 [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)) 
-   以 Windows 7 為目標的 [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)
-   [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0)舊版作業系統 (例如 Windows Vista 或 Windows vista Service Pack 1 (SP1) ) 

## <a name="calling-version-independent-functions-and-structures"></a>呼叫 Version-Independent 函式和結構

建議以特定作業系統或 WDK 版本為目標的 WFP 開發人員一律針對與版本無關的宏進行程式設計。 這會自動選取您的目標作業系統所支援的最新版本。 建議使用最新的標頭檔，即使是以較早的作業系統為目標。 以一致的方式進行，可確保使用最新的支援版本，也可以讓您更輕鬆地維護和更新程式碼。

[WFP api 參考檔](fwp-reference.md)說明編號 API 的每個版本。 如果有一個以上的版本，則會注明目標作業系統。 不過，開發人員通常會想要呼叫與版本無關的 (numberless) api，並指出目標作業系統 (例如 Windows Vista 的 **NTDDI \_ WIN6** 或 Windows 8) 的 **NTDDI \_ WIN8** 。

為了確保正確處理在不同版本中採用不同參數的函式，您可以包含條件式區塊（例如） `#if (NTDDI_VERSION >= NTDDI_WIN7)` 。

 

 




