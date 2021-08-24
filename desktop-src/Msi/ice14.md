---
description: ICE14 會驗證 Windows Installer 資料庫的功能資料表。
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a0789b7844fcbee52654d29b700b167a073fa51778ef3882b1fcbe2864fbb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638168"
---
# <a name="ice14"></a>ICE14

ICE14 會驗證功能的下列各項：

-   在 [功能資料表](feature-table.md)的 [屬性] 資料行中，該根父功能沒有設定 msidbFeatureAttributesFollowParent 位。 根功能沒有父系。
-   在功能資料表的功能和功能父資料行中，沒有任何功能具有相同的專案 \_ 。 [](feature-table.md) 沒有任何功能可以是本身的父系。

## <a name="result"></a>結果

ICE14 會在功能資料表的功能和功能的父資料行中找到具有 msidbFeatureAttributesFollowParent 位集或功能相同專案的根功能時張貼錯誤訊息 \_ 。

## <a name="example"></a>範例

在下列範例中，ICE14 會傳回下列錯誤：

-   功能運動在檔案資料表的功能和功能父資料行中具有相同的值 \_ 。
-   根功能運動已設定 msidbFeatureAttributesFollowParent 位。

在此範例的功能樹狀結構中，運動是根功能以及游泳和足球功能的父系。 自由樣式是游泳的子功能。 TouchFootball 是足球的子功能。

[功能表](feature-table.md) (部分) 



| 功能       | 屬性 | 功能 \_ 父系 |
|---------------|------------|-----------------|
| 運動項目         | 4          | 運動項目           |
| 游泳      | 1          | 運動項目           |
| 足球      | 4          | 運動項目           |
| 自由泳     | 1          | 游泳        |
| TouchFootball | 4          | 足球        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



