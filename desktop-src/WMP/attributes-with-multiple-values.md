---
title: '具有多個值的屬性 (Windows Media Player SDK) '
description: 瞭解 Windows Media Player SDK 中具有多個值的屬性。 某些媒體專案屬性可以有多個值。
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Windows Media Player，媒體專案的屬性
- Windows Media Player 物件模型，媒體專案的屬性
- 物件模型、媒體專案的屬性
- Windows Media Player 行動裝置，媒體專案的屬性
- Windows Media Player ActiveX 控制項、媒體專案的屬性
- Windows Media Player 的行動 ActiveX 控制項、媒體專案的屬性
- ActiveX 控制項、媒體專案的屬性
- Windows Media Player 文件庫、媒體專案的屬性
- 文件庫、媒體專案的屬性
- 屬性，多個值
- 多個屬性值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16baf4bab47dc972ec7b043980dccb0f2aadd57
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262600"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a>具有多個值的屬性 (Windows Media Player SDK) 

某些媒體專案屬性可以有多個值。 例如， **Author**、 **WM/書寫器** 和 **WM/** 內容屬性都可以有一個以上的值。 這類屬性的資料類型是 **多重值字串**。

在 Windows Media Player 中，程式庫會在單一欄位中顯示多個值，並以分號分隔這些值。 不過，每個值實際上都是 Windows Media 專案中的個別屬性。

您可以撰寫程式碼來判斷指定的屬性是否有多個值，然後取得這些值。 您必須使用 *媒體*。**getItemInfoByType**。 如果您使用 *媒體*。**getItemInfo** 方法若要取得多重值屬性，您只會取出第一個值。

[閱讀屬性值](reading-attribute-values.md)主題中的最後一個範例示範如何使用 *媒體*。**getAttributeCountByType** 和 *媒體*。**getItemInfoByType** 方法，以取得指定屬性的多個值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**媒體專案屬性**](media-item-attributes.md)
</dt> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**從 CD 或 DVD 讀取屬性值**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




