---
title: PrintCapabilities 設定相依性
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e7f376d8bd0dab823adb3a2e0665db27508b1d7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103853524"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a>PrintCapabilities 架構中的設定相依性

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

PrintCapabilities 架構會根據所使用的專案，以及由父元素和子項目表示的一般結構，而緊密地平行使用 Print Schema Framework。 專屬於 PrintCapabilities 的設定相依性會在此列為一般架構的延伸模組。 設定相依性是指某些專案（包括其內容）可以改變或甚至從一個 PrintCapabilities 檔刪除到下一個，因為設定相依性的結果。 即使父項目必須與設定無關，其子項目還是可能具有相依性。 這類相依性是使用 \* \* GPD 檔中的 Switch/Case 結構來表示。

作為設定相依性的範例，請考慮與 PrintCapabilities 檔中每個屬性相關聯的值。 每個 PrintCapabilities 檔在定義的屬性實例和指派給這些屬性實例的值實例中可能不同。



| 項目類型                                                                                                                                                                             | 設定相依性                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 功能 <br/> 選項<br/> ParameterInit<br/> ParameterRef<br/> PrintCapabilities<br/> PrintTicket<br/> 屬性<br/> ScoredProperty<br/> | 這些元素不能有設定相依性。<br/>                                                                                                                                                           |
| ParameterDef <br/>                                                                                                                                                                 | ParameterDef 元素和其中包含的元素，都不能有任何設定相依性。<br/>                                                                                        |
| 屬性 <br/>                                                                                                                                                                     | 屬性元素可能具有設定相依性，除非它們出現在 ParameterDef 元素中。<br/>                                                                                                       |
| 值 <br/>                                                                                                                                                                        | 出現在 ScoredProperty 元素內的值元素不能有任何設定相依性。 出現在 Property 元素內的值元素可能會對設定有任意的相依性。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




