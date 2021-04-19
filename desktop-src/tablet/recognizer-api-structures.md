---
description: 本節說明辨識器結構。
ms.assetid: 4c17391f-7af4-42ab-b77f-e3c39cadc0b6
title: 辨識器結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addaccf3e69f35b99379710d681fe8ac45559ea1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997575"
---
# <a name="recognizer-structures"></a>辨識器結構

本節說明辨識器結構。

## <a name="in-this-section"></a>本節內容



| 結構                                                    | Description                                                                                                                                                   |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**字元 \_ 範圍**](/windows/win32/api/rectypes/ns-rectypes-character_range)                  | 指定 Unicode 點的範圍 (字元) 。<br/>                                                                                                  |
| [**>LATTICE \_ 計量**](/windows/win32/api/rectypes/ns-rectypes-lattice_metrics)                  | 描述基準和中線高度。<br/>                                                                                                     |
| [**線段 \_**](/windows/win32/api/rectypes/ns-rectypes-line_segment)                        | 描述線條辨識區段的起點和終點，例如基準或中線。<br/>                                                 |
| [**封包 \_ 描述**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)            | 描述特定 tablet 內容的封包內容。<br/>                                                                               |
| [**封包 \_ 屬性**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)                  | 描述 tablet 驅動程式所報告的封包屬性。<br/>                                                                                 |
| [**屬性 \_ 度量**](/windows/desktop/api/tpcshrd/ns-tpcshrd-property_metrics)                | 定義封包屬性的範圍和解析度。<br/>                                                                                             |
| [**辨識 \_ ATTRS**](/windows/win32/api/rectypes/ns-rectypes-reco_attrs)                            | 抓取辨識器的屬性，或指定當您搜尋已安裝的辨識器時要使用的屬性。<br/>                         |
| [**辨識 \_ 指南**](/windows/win32/api/rectypes/ns-rectypes-reco_guide)                            | 將筆墨的界限定義到辨識器。<br/>                                                                                               |
| [**辨識 \_ >LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)                        | 作為 >lattice 的進入點。<br/>                                                                                                          |
| [**辨識 \_ >LATTICE 資料 \_ 行**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)         | 表示 >lattice 中的資料行。<br/>                                                                                                                |
| [**辨識 \_ >LATTICE \_ 元素**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)       | 對應到一個單字或一個東亞字元，通常是：不過，專案也可以對應至筆勢、圖形或其他程式碼。<br/> |
| [**辨識 \_ >LATTICE \_ 屬性**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties) | 包含屬性結構指標的陣列。<br/>                                                                                              |
| [**辨識 \_ >LATTICE \_ 屬性**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)     | 包含 >lattice 中所使用的屬性。<br/>                                                                                                           |
| [**辨識 \_ 範圍**](/windows/win32/api/rectypes/ns-rectypes-reco_range)                            | 識別結果字串中的字元範圍。<br/>                                                                                             |
| [**筆劃 \_ 範圍**](/windows/win32/api/tpcshrd/ns-tpcshrd-stroke_range)                        | 在 [**InkDisp**](inkdisp-class.md) 物件中指定筆劃的範圍。<br/>                                                                       |



 

 

 




