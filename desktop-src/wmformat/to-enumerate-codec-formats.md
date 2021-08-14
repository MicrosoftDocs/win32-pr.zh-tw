---
title: 列舉編解碼器格式
description: 列舉編解碼器格式
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- 串流，列舉編解碼器格式
- 編解碼器，列舉
- 資料流程、編解碼器格式
- 編解碼器，格式
- 編解碼器，IWMCodecInfo 介面
- IWMCodecInfo，編解碼器格式
- 編解碼器，IWMCodecInfo3 介面
- IWMCodecInfo3，編解碼器格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5221b675c5aa3b5602bcfda96b22233f77d4ba92199f29f36885a4053700dfd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196514"
---
# <a name="to-enumerate-codec-formats"></a>列舉編解碼器格式

編解碼器格式是以編解碼器資料填入的串流設定物件。 每個編解碼器格式都包含編解碼器所支援的媒體設定。 大部分音訊編解碼器都支援有限數量的格式，每個都是由編解碼器列舉，而且可以使用 [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)的方法來存取。 另一方面，視頻編解碼器只提供單一格式。 這是因為影片串流具有比音訊串流設定更具彈性的變數，例如框架大小。 使用影片串流時，您必須填入部分串流設定值;音訊串流設定只能進行編輯，以指派名稱、連線名稱和串流號碼。 如需詳細資訊，請參閱 [所有資料流程的通用](configuration-common-to-all-streams.md)設定。

列舉的編解碼器格式取決於目前使用 [**IWMCodecInfo3：： SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting)設定的編解碼器列舉設定。 目前只支援兩種編解碼器屬性： g \_ wszNumPasses，它會指定編解碼器將執行的編碼傳遞數目，而 g \_ wszVBREnabled 則指定編解碼器是否會使用可變的位元速率編碼。 任何編解碼器支援的最大編碼傳遞數目是兩個，因此有四個不同的設定可供您抓取編解碼器，如下表所示。



|    &nbsp;    | 固定位元速率 (CBR) 資料流程 | 2-通過 CBR 串流 | 以品質為基礎的變數位元速率 (VBR) 資料流程 | 以位速率為基礎的 VBR 串流 (受限或不受限制的)  |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| g \_ wszVBREnabled | FALSE                          | FALSE             | TRUE                                         | true                                                     |
| g \_ wszNumPasses  | 1                              | 2                 | 1                                            | 2                                                        |



 

若要列舉編解碼器支援的格式，請使用 [**IWMCodecInfo：： GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) 來尋找支援的編解碼器數目。 然後針對每個格式呼叫 [**IWMCodecInfo：： GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) 。 格式索引的範圍是從零到1，小於支援的格式總數。 您可以藉由呼叫 [**IWMCodecInfo2：： GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc)來取出格式的描述。 使用 **GetCodecFormatDesc** 時，您不需要使用 **GetCodecFormat**，因為這兩種方法都會抓取資料流程設定物件。 影片編解碼器格式不包含描述。 每個影片編解碼器都只有一種格式，可用於該類型的所有資料流程。

當您取得編解碼器格式時，您會取得包含格式設定之資料流程設定物件的 [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) 介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**從編解碼器取得串流設定資訊**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




