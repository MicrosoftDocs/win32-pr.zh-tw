---
description: 使用系統登錄提供者的管理應用程式可以定義類別，其屬性代表特定金鑰的登錄資料，然後將類別儲存在 WMI 存放庫中。
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: 定義 System Registry 提供者的類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deecdbc419c5a245e609380732474a39089f28cb8c2fd76c2ac57546f2d00110
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097288"
---
# <a name="defining-classes-for-the-system-registry-provider"></a>定義 System Registry 提供者的類別

使用系統登錄提供者的管理應用程式可以定義類別，其屬性代表特定金鑰的登錄資料，然後將類別儲存在 WMI 存放庫中。 針對系統登錄定義類別的大部分程式，與定義任何其他類別的程式相同。 不過，系統登錄提供者會要求您使用特定的資料類型和限定詞。

下列程式說明如何定義 System Registry 提供者的類別。

**若要定義 System Registry 提供者的類別**

1.  建立類別的方式，就像任何其他類別一樣。

    如需詳細資訊，請參閱 [建立類別](creating-a-class.md)。

2.  將適當的登錄資料類型對應至適當的 WMI 類型。

    System Registry provider 將登錄資料類型對應至特定的 WMI 資料類型。 如需詳細資訊，請參閱將登錄 [資料類型對應至 WMI 資料類型](mapping-a-registry-data-type-to-a-wmi-data-type.md)。

3.  使用必要的限定詞來定義登錄提供者的位置，以及適當登錄機碼的位置。

    系統登錄提供者會使用三個限定詞來定義各種類別、提供者和登錄專案的位置。 如需詳細資訊，請參閱 [使用限定詞定義登錄類別](defining-a-registry-class-with-qualifiers.md)。

 

 



