---
description: 列舉篩選圖形中的物件
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: 列舉篩選圖形中的物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369cd3400d3b7fc9944662ed6d32fd67234af90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109105"
---
# <a name="enumerating-objects-in-a-filter-graph"></a>列舉篩選圖形中的物件

應用程式可能需要在篩選圖形中找出特定的篩選，甚至在篩選器上找出特定的釘選。 例如，它可能會使用特定篩選器所公開的介面。 或者，它可能會建立特製化的篩選圖形，而且需要在個別的 pin 上呼叫方法來連接篩選。 基於這個目的，DirectShow 提供數種方法來列舉篩選圖形中的物件。

本節中所討論的列舉值會遵循 COM 列舉介面所使用的標準格式。 如需詳細資訊，請參閱 Platform SDK 中的「IEnumXXXX」主題。 如需列舉使用者電腦上已註冊但尚未在篩選圖形中之篩選準則的相關資訊，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。

本文包含下列主題：

-   [列舉篩選](enumerating-filters.md)
-   [列舉釘選](enumerating-pins.md)
-   [列舉媒體類型](enumerating-media-types.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本的 DirectShow 工作](basic-directshow-tasks.md)
</dt> </dl>

 

 



