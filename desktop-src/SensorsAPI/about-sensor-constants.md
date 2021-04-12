---
description: 關於感應器常數
ms.assetid: ba85ccd8-5251-4e47-84da-80899fe84c39
title: 關於感應器常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea862d38af74058d11d3a6fa1eb11a702b3b277
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513909"
---
# <a name="about-sensor-constants"></a>關於感應器常數

Windows 感應器和位置平台使用常數的方式有很多種。 平臺會定義您可以在感應器驅動程式程式碼中使用的不同常數。 感應器製造商可以定義自訂常數。 您可以在「感應器 .h」檔案中找到平臺定義常數的定義。 如需平臺定義感應器常數的詳細資訊，請參閱 [常數](constants.md)。

### <a name="sensor-and-data-organization"></a>感應器和資料組織

平臺會以下列方式組織感應器和資料。

-   類別代表各種類別的感應器裝置。 類別可讓您將可能提供類似資訊的感應器群組在一起，或以某種方式與其他相關聯。 每個類別都以 **GUID** 常數表示。 例如，報表緯度和經度座標的感應器屬於定位感應器類別。 這是由感應器 \_ 類別 \_ 位置常數所 representented。
-   感應器類型代表特定類型的感應器。 每個感應器類型都符合特定的類別。 不同類型的兩個感應器可以屬於相同類別或不同類別。 每個感應器類型都是以 **GUID** 常數來表示。 例如，全球定位系統感應器會由感應器 \_ 類型 \_ 位置 \_ GPS 常數來識別。 不過，使用 IP 位址提供目前位置的感應器會由感應器 \_ 類型 \_ 位置 \_ 查閱常數來識別。 不過，這兩個感應器都屬於「定位感應器」類別。
-   資料類型代表感應器可以提供的特定資訊類型。 感應器資料類型可以包含實際的測量值，例如海拔高度;用來表示資料的單位相關資訊，例如計量;資料的參考點，例如海平面。 每個資料類型都是以 **PROPERTYKEY** 常數來表示。 例如，在量表中代表海拔高度的資料類型，會由感應器 \_ 資料 \_ 類型 \_ 高度 \_ SEALEVEL \_ 計量常數來識別。
-   當報告資料時，值會被視為包含在資料欄位中，而相關資料欄位的集合則構成資料包表。 資料包表會使用 [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) 介面封裝在一起。 每個資料包表都必須包含至少一個有效的資料欄位，以及可識別資料包表建立時間的時間戳記。 時間戳記是以感應器 \_ 資料 \_ 類型 \_ TIMESTAMP 常數來表示。

### <a name="other-constants"></a>其他常數

您的程式也必須使用其他常數。 這些常數包括下列各項：

-   感應器屬性，例如感應器 \_ 屬性 \_ 描述。 這些常數通常是用來描述感應器。 某些感應器屬性必須由感應器提供，某些屬性可由用戶端應用程式設定，而有些則必須一律從感應器傳回相同的值。 [ [**感應器屬性**](sensor-properties.md) 參考] 區段提供每個屬性的此資訊。
-   事件常數，例如感應器 \_ 事件 \_ 狀態 \_ 已變更。 事件常數包含表示事件種類的 **GUID** s，以及代表事件參數類型的 **PROPERTYKEY** s。 您將使用這些常數進行方法呼叫，例如 [**ISensor：： SetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventinterest) 和 [**ISensor：： GetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-geteventinterest)。

### <a name="custom-constants"></a>自訂常數

感應器製造商可以定義自訂常數。 例如，感應器可以屬於平臺未定義的類別。 在您可以使用定義自訂常數的感應器之前，感應器製造商必須發佈這些值，例如藉由發佈標頭檔。 如需詳細資訊，請參閱感應器提供的檔。

 

 
