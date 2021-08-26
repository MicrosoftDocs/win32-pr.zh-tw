---
description: 感應器資料包表物件包含感應器資料。
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: 感應器資料包表物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca1a8e5f61b23753437bd8b1cf4c2a176515b7042b21e84c4d2f431debc8fe6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992598"
---
# <a name="the-sensor-data-report-object"></a>感應器資料包表物件

感應器資料包表物件包含感應器資料。

感應器必須提供有意義的資料，才能發揮效用。 資料產生的數量和頻率會因感應器而異。 例如，偵測門是否開啟的感應器會產生少量的 **布林** 資料，而移動感應器可能會持續產生多個資料項目。 為了將您的程式接收資料的方式標準化，感應器 API 會使用感應器資料包表物件。

您可以透過 [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) 介面存取感應器資料包表中的資訊。 此介面可讓您抓取資料包表的時間戳記，以判斷報表中的資訊是否有用。 您可以使用兩種方式來抓取資料本身：作為個別資料欄值或一組值。 若要以個別值形式取出資料，請呼叫 [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) 方法。 若要取出多個值，請呼叫 [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) 方法。

您可以使用 **PROPERTYKEY** 常數，指定要從報表中取出的資料類型或資料欄位。 一般感應器類型之資料欄位的屬性索引鍵是在 [感應器] 中定義。

 

 
