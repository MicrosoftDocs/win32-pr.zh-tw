---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: 使用 PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dda5b21d1472ec8d4162c8d7229ff47264fb55
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103945749"
---
# <a name="uses-of-the-printcapabilities"></a>使用 PrintCapabilities

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

PrintCapabilities 的目的是要將可設定的裝置屬性工作表示為功能/選項結構或參數結構。 這項資訊會定義裝置的設定空間，並且可供使用者介面 (UI) 用戶端用來建立 UI。 Print Schema 關鍵字會定義一組標準功能實例、標準功能實例的選項實例，以及 ParameterDef 實例。

PrintCapabilities 中的功能/選項或參數結構旨在保存描述裝置的屬性或 ScoredProperty 實例，以及多工緩衝處理器子系統所支援的實例。 這些屬性和 ScoredProperty 實例是裝置用戶端的一般興趣，並包含 Win32 DevCaps 函式所提供的資訊。 Print Schema 關鍵字會定義一組標準屬性和 ScoredProperty 實例。

請注意，PrintCapabilities 檔的目的是只代表單一值資料：不相依于裝置特定設定的資料。 PrintCapabilities 檔只提供設定相依資料的快照集。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



