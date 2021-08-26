---
description: 設定編解碼器 DMOs
ms.assetid: 431b33f1-ceb0-4f1b-a9f2-72e88b63f973
title: 設定編解碼器 DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4040c0a16c0311d14b0553336e1d9b70a7a6c1fd28a0f01277c955eea55ec7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958328"
---
# <a name="configuring-codec-dmos"></a>設定編解碼器 DMOs

本主題說明設定編解碼器 DMOs 的流程。 每個編解碼器都有特定的程式，但此處所述的全部資訊都有提供。

## <a name="configuring-dmo-inputs-and-outputs"></a>設定 DMO 輸入和輸出

每個 DMO 都支援特定的輸入和輸出類型。 您可以針對輸出呼叫 [**IMediaObject：： GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) 來取得輸入和輸出支援的類型，並針對輸出呼叫 [**IMediaObject：： GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) 。 您可以對任一個方法進行重複呼叫來列舉支援的格式，並在每次呼叫時遞增型別索引。 當索引超出最後支援的類型時，呼叫會傳回 DMO \_ E \_ NO \_ 其他 \_ 專案。

針對視頻編解碼器，針對指定的媒體子類型，只會列舉一個輸出類型或輸入類型。 針對音訊編解碼器，會列舉每個個別支援的類型。 如需個別編解碼器支援類型的詳細資訊，請參閱使用 [音訊](workingwithaudio.md) 和使用 [影片](workingwithvideo.md)。

設定輸入和輸出資料流程的媒體類型之後，請分別呼叫 [**IMediaObject：： SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) 和 [**IMediaObject：： SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) 來設定它們。 這兩種方法都會傳回指定類型無效時 **\_ \_ \_ 不 \_ 接受的 DMO E 類型**。

## <a name="configuring-the-codec-dmos-for-encoding"></a>設定編碼的編解碼器 DMOs

所有的 Windows Media 音訊和影片編解碼器都支援各種不同的編碼功能。 這些功能通常是藉由使用 **IPropertyBag** 介面的方法，在 DMO 上設定屬性來設定。 有些屬性是使用特製化的編解碼器介面進行設定。 在 [編解碼器物件](codecobjects.md)的區段中，會列出每個編解碼器的這些介面。

設定編碼 DMO 的一般作業順序如下所示：

1.  使用 **IPropertyBag** 的方法來設定所需的編解碼器功能。
2.  如有需要，請使用編解碼器 DMO 介面來設定其他功能。
3.  設定輸入和輸出類型。 設定類型的順序會因個別編解碼器而異。 如需詳細資訊，請參閱使用 [音訊](workingwithaudio.md) 和使用 [影片](workingwithvideo.md)。

## <a name="configuring-the-codec-dmos-for-decoding"></a>設定編解碼器 DMOs 進行解碼

解碼比編碼更簡單，因為支援的解碼器功能較少。

設定解碼 DMO 的一般作業順序如下所示：

1.  使用 **IPropertyBag** 的方法來設定所需的解碼器功能。
2.  將輸入類型設定為用於編碼器輸出的類型。
3.  設定輸出類型。 針對不同的輸入，支援的輸出類型是不同的。

> [!Note]  
> 請務必將相同的媒體類型用於編碼器輸入，如同用於編碼器輸出一樣。 這是因為 Windows Media 音訊和影片編解碼器使用媒體格式搭配額外的資料。 這項資料會附加至 [**DMO \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)結構的 **pbFormat** 成員所指向的結構， (通常是 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)或 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))) 。 針對某些類型，額外的資料是列舉編碼器輸出類型的一部分。 其他類型則需要您手動附加此資料。 如果沒有延伸格式資料，您就無法將壓縮的內容解碼。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用編解碼器 DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
