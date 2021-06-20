---
description: Print Schema Framework 會定義命名空間，其中包含在 Print Schema 關鍵字中定義的元素和 XML 屬性。
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: 在 Print Schema 關鍵字中定義的物件和名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aabdac90de6743388ca1f4d44e1ad52c020dbd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408551"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a>在 Print Schema 關鍵字中定義的物件和名稱

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

Print Schema Framework 會定義命名空間，其中包含在 Print Schema 關鍵字中定義的元素和 XML 屬性。 這包括功能、選項和 ScoredProperty 之類的元素。屬性名稱，例如名稱和傳播;和 XML 屬性的值，例如受限的。 換句話說，在 Print Schema 關鍵字中定義的每個名稱都應使用這個命名空間來明確限定，或應該透過使用預設的 xmlns 屬性，以隱含方式與這個命名空間相關聯。 Print Schema 關鍵字檔會定義可能出現在任何給定內容或位置的公用元素實例。 元素實例必須只出現在 Print Schema Framework 所指定的內容或位置中。 例如，在列印架構關鍵字中定義的 <.psf： Option name = "psk： Letter" > 實例必須出現在 <.psf： Feature name = "psk： PageMediaSize" > 實例 (也定義在列印架構關鍵字) 中。 您無法在其指定的內容之外自由使用指定的選項實例。

私用定義的元素實例可能會出現在任何位置，只要專案類型出現在 Print Schema Framework 所允許的內容中即可。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



