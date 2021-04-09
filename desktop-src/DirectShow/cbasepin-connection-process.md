---
description: CBasePin 連接進程
ms.assetid: 4b3a9023-0267-4caa-9d89-88237009df05
title: CBasePin 連接進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1441b0daba58857e00da0139d3312fb277287fc2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935799"
---
# <a name="cbasepin-connection-process"></a>CBasePin 連接進程

本節說明 [**CBasePin**](cbasepin.md) 類別如何執行 pin 連接程式。

篩選圖形管理員會起始所有的釘選連接。 它會呼叫輸出釘選的 [**IPin：： Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) 方法，並指定輸入的 pin。 輸出 pin 會藉由呼叫輸入釘選的 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 方法來完成連接。 輸入 pin 可以接受或拒絕連接。

篩選圖形管理員也可以指定連接的媒體類型。 如果是，則會嘗試使用該類型連接。 如果沒有，則 pin 必須協商型別。 篩選圖形管理員也可以指定 *部分* 媒體類型，此類型的 \_ 主要類型、子類型或格式類型的值為 GUID Null。 在這種情況下，pin 會嘗試比對媒體類型的任何部分（若已指定）;值 GUID \_ Null 可作為萬用字元。

[**CBasePin：： Connect**](cbasepin-connect.md)方法一開始先確認 pin 可以接受連接。 例如，它會檢查 pin 是否尚未連接。 它會將連接進程的其餘部分委派給 [**CBasePin：： AgreeMediaType**](cbasepin-agreemediatype.md) 方法。 接下來的所有專案都是由 **AgreeMediaType** 執行。

如果媒體類型是完全指定的，則 pin 會呼叫 [**CBasePin：： AttemptConnection**](cbasepin-attemptconnection.md) 方法來嘗試連接。 否則，它會依下列順序嘗試媒體類型：

1.  輸入釘選的慣用類型。
2.  輸出釘選的慣用類型。

您可以將 [**CBasePin：： m \_ bTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md) 旗標設為 **TRUE**，以反轉此順序。

在每個案例中，pin 都會呼叫 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 來列舉媒體類型。 這個方法會取出傳遞給 [**CBasePin：： TryMediaTypes**](cbasepin-trymediatypes.md) 方法的枚舉器物件。 **TryMediaTypes** 方法會在每個媒體類型之間執行迴圈，並針對每個類型呼叫 [**AttemptConnection**](cbasepin-attemptconnection.md) 。

在 [**AttemptConnection**](cbasepin-attemptconnection.md) 方法中，輸出圖釘會呼叫下列方法：

-   它會自行呼叫 [**CBasePin：： CheckConnect**](cbasepin-checkconnect.md) ，以檢查輸入的 pin 是否適合。
-   它本身會呼叫 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) ，以驗證媒體類型。
-   它會在輸入 pin 上呼叫 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 。 輸入 pin 會使用這個方法來判斷是否應接受連接。
-   它會自行呼叫 [**CBasePin：： CompleteConnect**](cbasepin-completeconnect.md) 來完成連接。

請注意：

-   [**CheckConnect**](cbasepin-checkconnect.md) 是虛擬方法。 在基類中，此方法會檢查釘選方向是否相容。 輸出 pin 必須連接到輸入圖釘，反之亦然。 衍生的 pin 類別通常會覆寫這個方法，以執行其他檢查。 例如，它可能會查詢連接所需介面的其他 pin。 如果衍生類別覆寫 **CheckConnect**，則也應該呼叫 [**CBasePin**](cbasepin.md) 方法。
-   [**CheckMediaType**](cbasepin-checkmediatype.md) 是一種單純的虛擬方法，衍生類別必須執行此方法。
-   [**CompleteConnect**](cbasepin-completeconnect.md) 是不會在基類中執行任何動作的虛擬方法。 衍生類別可以覆寫這個方法，以執行完成連接所需的任何其他工作，例如決定記憶體配置器。

如果這些步驟中有任何一項失敗，輸出圖釘會呼叫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法，以復原 [**CheckConnect**](cbasepin-checkconnect.md)所採取的任何步驟。

輸入釘選的 [**ReceiveConnection**](cbasepin-receiveconnection.md) 方法會呼叫輸入釘選的 [**CheckConnect**](cbasepin-checkconnect.md)、 [**CheckMediaType**](cbasepin-checkmediatype.md)和 [**CompleteConnect**](cbasepin-completeconnect.md) 方法。 如果其中任何一項失敗，連接嘗試也會失敗。

下圖顯示 [**CBasePin**](cbasepin.md)中的連接程式：

![cbasepin 連接進程](images/cbasepin-connect.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



