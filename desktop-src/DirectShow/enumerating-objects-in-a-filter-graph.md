---
description: 列舉篩選 Graph 中的物件
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: 列舉篩選 Graph 中的物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa6206a583daaa984ef67af297c11c125128e58fec410ec1251afaca3987f582
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965468"
---
# <a name="enumerating-objects-in-a-filter-graph"></a>列舉篩選 Graph 中的物件

應用程式可能需要在篩選圖形中找出特定的篩選，甚至在篩選器上找出特定的釘選。 例如，它可能會使用特定篩選器所公開的介面。 或者，它可能會建立特製化的篩選圖形，而且需要在個別的 pin 上呼叫方法來連接篩選。 基於這個目的，DirectShow 提供數個方法來列舉篩選圖形中的物件。

本節中所討論的列舉值會遵循 COM 列舉介面所使用的標準格式。 如需詳細資訊，請參閱 Platform SDK 中的「IEnumXXXX」主題。 如需列舉使用者電腦上已註冊但尚未在篩選圖形中之篩選準則的相關資訊，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。

本文包含下列主題：

-   [列舉篩選](enumerating-filters.md)
-   [列舉釘選](enumerating-pins.md)
-   [列舉媒體類型](enumerating-media-types.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本 DirectShow 工作](basic-directshow-tasks.md)
</dt> </dl>

 

 



