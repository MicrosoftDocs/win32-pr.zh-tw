---
title: 強制插入 Key-Frame
description: 強制插入 Key-Frame
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- Advanced Systems Format (ASF) ，強制執行主要畫面格插入
- ASF (Advanced Systems Format) ，強制執行主要畫面格插入
- Advanced Systems Format (ASF) 、主要畫面格插入
- ASF (Advanced Systems Format) ，主要畫面格插入
- 主要畫面格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d400c0ee4ba97aa7de559b1394dbe5c9fb2a974c124924aeae0839b1b4dae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196494"
---
# <a name="to-force-key-frame-insertion"></a>強制插入 Key-Frame

Windows Media 視訊9編解碼器支援強制的主要畫面格插入。 當您將範例傳遞給寫入器時，可以指定必須將它編碼為 [*主要畫面*](wmformat-glossary.md)格。

若要強制執行範例的主要畫面格插入，請執行下列步驟。

1.  配置緩衝區來保存範例，並藉由呼叫 [**IWMWriter：： AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample)，取得包含緩衝區之 [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)介面的指標。
2.  藉由呼叫 [**INSSBuffer：： GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength)，取出在步驟1中建立之緩衝區的位置和大小。
3.  將範例資料複製到緩衝區位置，確定傳遞的範例符合配置的緩衝區。 視範例的來源而定，您可以使用各種功能來複製資料。 例如，如果您要從 AVI 檔案複製資料流程，則可以使用 AVI 函數 **AVIStreamRead**。
4.  藉由呼叫 [**INSSBuffer：： SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength)來更新緩衝區中使用的資料量，以反映樣本的實際大小。
5.  藉由呼叫 **INSSBuffer：： QueryInterface** 來取得 [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)介面的指標。
6.  藉由呼叫 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 方法來設定 WM \_ SampleExtensionGUID OutputCleanPoint 屬性，將範例設定為強制主要畫面格 \_ 。 這個屬性是布林值;將它設定為 **TRUE**。
7.  使用 [**IWMWriter：： WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) 方法，將緩衝區介面傳遞至寫入器，以及輸入編號和取樣時間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[**撰寫範例**](to-write-samples.md)
</dt> <dt>

[**變數位速率 (VBR) 編碼**](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 




