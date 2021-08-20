---
description: 可以在文字或整數資料庫欄位中使用可設定資料的整數格式類型。 MsmConfigItemNonNullable 屬性是此資料格式的隱含，不需要設定。 Null 對此類型而言永遠不是有效的值。
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: 整數格式類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf5d4ad0d7ef9ba8adb1ddb919e284dbd2a10b2eafc7c43f72d6d0ee777f743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805626"
---
# <a name="integer-format-types"></a>整數格式類型

可以在文字或整數資料庫欄位中使用可設定資料的整數格式類型。 MsmConfigItemNonNullable 屬性是此資料格式的隱含，不需要設定。 Null 對此類型而言永遠不是有效的值。

下列整數格式類型存在。

[任意整數類型](arbitrary-integer-type.md)

整數格式類型的可設定專案會使用於文字或整數資料行，而且一般可以由任何正整數或負整數來取代。 不過，特定可設定的專案也可能具有特性語義限制。 例如，特定可設定的專案必須是介於0和100之間的整數，以及其他語義限制。 Mergemod.dll 不會強制執行這類限制，因此模組作者應該準備好處理任何符合指定整數格式類型的字串。

 

 



