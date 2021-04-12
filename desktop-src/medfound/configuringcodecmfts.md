---
description: 設定編解碼器 MFTs
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: 設定編解碼器 MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0065f05d10eae367b13ef6f7caf3fe2ab322163a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468636"
---
# <a name="configuring-codec-mfts"></a>設定編解碼器 MFTs

本主題說明設定編解碼器 MFTs 的流程。 每個編解碼器都有特定的程式，但此處所述的全部資訊都有提供。

## <a name="configuring-mft-inputs-and-outputs"></a>設定 MFT 輸入和輸出

每個 MFT 都支援特定的輸入和輸出類型。 您可以藉由重複呼叫 [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)來取得支援的輸入類型，並以每個呼叫遞增類型索引。 當您找到適當的類型時，請呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)來設定輸入類型。 然後，您可以使用呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 和 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)，針對輸出類型重複此程式。 您必須在設定輸入類型之後，才查詢或設定可用的輸出類型。

## <a name="configuring-the-codec-mfts-for-encoding"></a>設定編碼的編解碼器 MFTs

所有的 Windows Media 音訊和影片編解碼器都支援各種不同的編碼功能。 這些功能通常是藉由使用 **IPropertyStore** 介面的方法，在 MFT 上設定屬性來設定。 有些屬性是使用特製化的編解碼器介面進行設定。 在 [編解碼器物件](codecobjects.md)的區段中，會列出每個編解碼器的這些介面。

設定編碼 MFT 的一般作業順序如下所示：

1.  使用 **IPropertyStore** 的方法來設定所需的編解碼器功能。
2.  如有需要，請使用編解碼器 MFT 介面來設定其他功能。
3.  設定輸入和輸出類型。 設定類型的順序會因個別編解碼器而異。 如需詳細資訊，請參閱使用 [音訊](workingwithaudio.md) 和使用 [影片](workingwithvideo.md)。

## <a name="configuring-the-codec-mfts-for-decoding"></a>設定編解碼器 MFTs 進行解碼

解碼比編碼更簡單，因為支援的解碼器功能較少。

設定解碼 MFT 的一般作業順序如下所示：

1.  使用 **IPropertyStore** 的方法來設定所需的解碼器功能。
2.  將輸入類型設定為用於編碼器輸出的類型。
3.  設定輸出類型。 針對不同的輸入，支援的輸出類型是不同的。

> [!Note]  
> 請務必將相同的媒體類型用於編碼器輸入，如同用於編碼器輸出一樣。 這是因為 Windows Media 音訊和影片編解碼器使用媒體格式搭配額外的資料。 如果沒有延伸格式資料，您就無法將壓縮的內容解碼。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用編解碼器 MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



