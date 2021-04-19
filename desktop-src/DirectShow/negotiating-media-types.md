---
description: 協商媒體類型
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: 協商媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdcb78cfef6b8396d866ea148267c5a899cd353
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986023"
---
# <a name="negotiating-media-types"></a>協商媒體類型

當篩選圖形管理員呼叫 [**IPin：： Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) 方法時，會有數個選項可用於指定媒體類型：

-   **完成類型：** 如果媒體類型是完全指定的，則會嘗試使用該類型連接。 如果無法連線，連接嘗試就會失敗。
-   **部分媒體類型：** 如果主要類型、子類型或格式類型為 GUID Null，則媒體類型為 [ *部分* ] \_ 。 值 GUID \_ Null 可做為 "萬用字元"，表示可接受任何值。 Pin 會協商與部分類型一致的型別。
-   **沒有媒體類型：** 如果篩選圖形管理員傳遞 **Null** 指標，則 pin 可以接受兩個 pin 都可接受的任何媒體類型。

如果釘選連線，連接一定會有完整的媒體類型。 篩選圖形管理員所提供之媒體類型的目的是要限制可能的連線類型。

在進行協調程式期間，輸出 pin 會藉由呼叫輸入 pin 的 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 方法來提議媒體類型。 輸入 pin 可以接受或拒絕建議的類型。 此程式會重複，直到輸入的 pin 接受型別，或是輸出的釘選出型別且連接失敗。

輸出圖釘如何選取要建議的媒體類型取決於執行。 在 DirectShow 基類中，輸出圖釘會在輸入 pin 上呼叫 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 。 這個方法會傳回列舉輸入釘選媒體類型的列舉值。 如果失敗，輸出釘會列舉自己慣用的類型。

**使用媒體類型**

在接收 **AM \_ 媒體 \_ 類型** 參數的任何函式中，一律先驗證 **cbFormat** 和 **formattype** 的值，再取值 **pbFormat** 成員。 下列程式碼不正確：


```C++
if (pmt->formattype == FORMAT_VideoInfo)
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Wrong!
}
```



下列程式碼是正確的：


```C++
if ((pmt->formattype == FORMAT_VideoInfo) && 
    (pmt->cbFormat > sizeof(VIDEOINFOHEADER) &&
    (pbFormat != NULL))
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Now you can dereference pVIH.
}
```



 

 



