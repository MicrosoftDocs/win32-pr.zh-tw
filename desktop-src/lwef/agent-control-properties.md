---
title: Agent 控制項屬性
description: Agent 控制項屬性
ms.assetid: e6a5b2db-9abf-4988-be41-fc7f4530507f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5e80b10469e7e256b1b2bf3bcf55fb5a8a08b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021007"
---
# <a name="agent-control-properties"></a>Agent 控制項屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

下列屬性可直接從 Agent 控制項存取：

-   [**連線**](connected-property.md)
-   [**Name**](name-property-a.md)
-   [**RaiseRequestErrors**](raiserequesterrors-property.md)

此外，某些程式設計環境可能會指派其他設計階段或執行時間屬性。 例如，Visual Basic 會新增 Left、Index、Tag 和 Top 屬性，在表單上定義控制項的位置，即使控制項不會出現在執行時間的表單頁面上也一樣。

暫止的屬性仍支援回溯相容性，但一律會傳回 **False** ，因為伺服器已不再支援暫停狀態。

 

 




