---
description: 本主題提供一些指導方針，以將解碼器或編碼器作為媒體基礎轉換 (MFT) 。
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: 執行編解碼器 MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4412db23747e9a6b3468e9e428120d099b2445ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194988"
---
# <a name="implementing-a-codec-mft"></a>執行編解碼器 MFT

本主題提供一些指導方針，以將解碼器或編碼器作為媒體基礎轉換 (MFT) 。

-   [編碼器](#encoders)
    -   [編碼器格式的協商](#encoder-format-negotiation)
-   [解碼器](#decoders)
    -   [僅限轉碼的解碼器](#transcode-only-decoders)
    -   [電影屬性](#telecine-attributes)
-   [相關主題](#related-topics)

## <a name="encoders"></a>編碼器

### <a name="encoder-format-negotiation"></a>編碼器格式的協商

下列程式是用來初始化編碼器：

1.  查詢 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面的 MFT。
2.  呼叫 [**ICodecAPI：： SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) 以設定編碼屬性。
3.  呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 來設定編碼格式。
4.  呼叫 [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) ，以取得相容輸入類型的清單。  (可能會略過此步驟。 ) 
5.  呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) ，以設定未壓縮的輸入格式。

在步驟3中設定輸出類型之後， [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) 方法必須傳回與目前輸出類型相容的輸入類型清單。 換句話說， **GetInputAvailableType** 在此點傳回的任何類型都必須是有效的 [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)。

對於解碼器，會反轉型別設定順序：先設定輸入型別，後面接著輸出型別。 設定輸入類型之後， [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 方法必須傳回可傳遞至 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 方法的類型清單。

編碼器和解碼器應支援 NV12 為常見的未壓縮格式。 這可確保管線元件可與基本的 colorspace 轉換交互操作。 當然，也可以支援其他格式。

## <a name="decoders"></a>解碼器

### <a name="transcode-only-decoders"></a>Transcode-Only 的解碼器

某些解碼器會針對轉碼 (解碼，然後重新編碼串流) ，因此不適合在播放期間使用。

如果解碼器 MFT 僅供轉碼使用，則在您註冊 MFT 時，請設定 [ **\_ \_ \_ \_ 僅限轉碼旗標的 MFT 列舉旗** 標] 旗標。  (參閱 [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)。 ) 

依預設， [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函式不會傳回轉碼的解碼器。 若要列舉轉碼的解碼器，請呼叫 **MFTEnumEx** ，然後在 *旗標* 參數中將 **MFT \_ 列舉 \_ 旗標轉碼為 \_ \_ ONLY** 旗標。 在 **MFTEnumEx** 函式中使用時，此旗標會列舉轉碼的解碼器和其他的解碼器。



| **\_ \_ \_ \_ 僅限 MFTRegister MFT 列舉旗標轉碼** | **\_ \_ \_ \_ 僅限 MFTEnumEx MFT 列舉旗標轉碼** | 是否列舉了 MFT？ |
|--------------------------------------------------|------------------------------------------------|--------------------|
| 1                                                | 1                                              | 是                |
| 1                                                | 0                                              | 否                 |
| 0                                                | 1                                              | 是                |
| 0                                                | 0                                              | 是                |



 

### <a name="telecine-attributes"></a>電影屬性

媒體來源可能會將下列電影屬性附加至它所提供的媒體範例。



| 屬性                                                                                   | 描述                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [**MFSampleExtension \_ RepeatFirstField**](mfsampleextension-repeatfirstfield-attribute.md) | 相當於 "repeat first field" (RFF) 旗標。 |
| [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) | "Top field first" (TFF) 旗標的反向。       |



 

這些旗標會在執行去交錯時，提供提示給增強型影片轉譯器 (EVR) 。 解碼器應該將這些旗標複製到輸出範例，使其到達 EVR，以將這些旗標傳播至輸出範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫自訂的 MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 
