---
description: 重新連接釘選
ms.assetid: 34b3e4de-e4eb-48c5-aaef-fc99b63e8691
title: 重新連接釘選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc71b4d5a62ee066edaa5f97b4cc3332b2231d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509991"
---
# <a name="reconnecting-pins"></a>重新連接釘選

在 pin 連線期間，篩選器可以中斷連接並重新連接其中一個其他 pin，如下所示：

1.  篩選準則會在其他篩選器的 pin 上呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) ，並指定新的媒體類型。
2.  如果 **QueryAccept** 傳回 S \_ OK，則篩選準則會呼叫 [**IFilterGraph2：： ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) 來重新連接釘選。

以下是篩選可能需要重新連接 pin 的一些範例：

-   **T 篩選準則。** *T 篩選準則* 會將輸入資料流程分割成多個輸出，而不會變更資料流程中的資料。 指標篩選器可以接受一系列的媒體類型，但類型必須符合所有的釘選連接。 因此，當輸入 pin 連線時，篩選可能需要重新協商輸出針腳上的任何現有連接，反之亦然。 如需範例，請參閱 [InfTee 篩選範例](inftee-filter-sample.md)。
-   **就地記錄篩選。** *就地* 篩選會修改原始緩衝區中的輸入資料，而不是將資料複製到個別的輸出緩衝區。 就地篩選必須針對上游和下游連接使用相同的配置器。 第一個連接 (輸入或輸出的 pin) 會以一般方式協調配置器。 不過，當其他 pin 連線時，可能無法接受第一個配置器。 在這種情況下，第二個 pin 會選擇不同的配置器，而第一個 pin 會使用新的配置器重新連接。 如需範例執行，請參閱 [**CTransInPlaceFilter**](ctransinplacefilter.md) 類別。

在 **ReconnectEx** 方法中，篩選圖形管理員會以非同步方式中斷連接並重新連接釘選。 除非 **QueryAccept** 傳回 S OK，否則篩選準則不得嘗試重新連接 \_ 。 否則，pin 將會保持中斷連線，而導致圖形錯誤。 此外，篩選器也應該在相同的執行緒上，從 [**IPin：： Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) 方法內要求重新連接。 如果 **連接** 方法在某個執行緒上傳回，而另一個執行緒進行重新連接要求，則篩選圖形管理員可能會在進行重新連接之前執行圖形，進而導致圖形錯誤。

 

 



