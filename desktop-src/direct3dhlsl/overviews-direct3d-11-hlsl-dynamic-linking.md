---
title: 動態連結
description: 圖形開發人員有時候會建立大型的一般用途著色器，以供各種不同的場景專案使用。
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5cd10bab8e2b4a28458cad1050847e0184ce43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673440"
---
# <a name="dynamic-linking"></a>動態連結

圖形開發人員有時候會建立大型的一般用途著色器，以供各種不同的場景專案使用。 在執行時間，著色器會有條件地執行適用于特定情況的程式碼。 可惜的是，這些大型的一般用途著色器會使用一般用途的暫存器 (GPRs) 效率不高，而且可能比較小、更具針對性的著色器慢許多。

著色器模型5藉由引進動態著色器連結來解決這個效能問題。 動態連結會使用介面和虛擬函式來分隔著色器程式碼片段，並允許應用程式選取要在繪製時使用的片段。 這會藉由只系結所需的著色器程式碼，而不是整個大型的一般用途著色器，來改善效能。

## <a name="in-this-section"></a>本節內容



| 項目                                                                                                                                                                                                                                                                                                                         | 描述                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[儲存要共用之著色器的變數和類型](storing-variables-and-types-for-shaders-to-share.md)<br/> | 描述類別連結化物件，用來儲存多個著色器可以共用的變數和類型。<br/> |
| <span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[介面和類別](overviews-direct3d-11-hlsl-dynamic-linking-class.md)<br/>                                                                                                         | 描述如何使用 HLSL 介面和類別來執行動態連結。<br/>                           |
| <span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[介面使用限制](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)<br/>                                                                            | 描述在著色器程式碼中使用介面的限制。<br/>                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





