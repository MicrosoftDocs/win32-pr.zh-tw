---
title: 設定檔案讀取的緩衝區
description: 設定檔案讀取的緩衝區
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- Windows Media Format SDK，讀取 ASF 檔案
- Advanced Systems Format (ASF) ，讀取檔案
- ASF (Advanced Systems Format) ，讀取檔案
- Windows Media Format SDK，配置緩衝區
- Advanced Systems Format (ASF) ，配置緩衝區
- ASF (Advanced Systems Format) ，配置緩衝區
- Advanced Systems Format (ASF) ，緩衝區配置
- ASF (Advanced 系統格式) ，緩衝區配置
- 緩衝區配置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374366"
---
# <a name="allocating-buffers-for-file-reading"></a>設定檔案讀取的緩衝區

在最基本的檔案讀取案例中，用來傳遞範例的緩衝區是由讀取物件 (讀取器物件或同步讀取器物件) 所配置。 不過，您可以自行配置緩衝區。 如需有關配置自己的緩衝區之優點的詳細資訊，請參閱使用者配置的 [範例支援](user-allocated-sample-support.md)。

若要使用您自己的緩衝區進行檔案讀取，請執行下列步驟。

1.  針對讀取器執行回呼或回呼，以在需要緩衝區時呼叫。 如果您正在讀取輸出範例，請使用 [**IWMReaderAllocatorEx：： AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex)。 如果您正在讀取串流範例，請使用 [**IWMReaderAllocatorEx：： AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)。 包含管理適合您應用程式之緩衝區的任何邏輯。
2.  配置您將用於讀取檔案的緩衝區集區。
    -   藉由呼叫 [**IWMReaderAdvanced：： GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) 或 [**IWMReaderAdvanced：： GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) 來尋找緩衝區所使用的每個輸出和/或資料流程，以找出緩衝區所需的大小。 如果使用同步讀取器，請改用 [**IWMSyncReader：： GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) 或 [**IWMSyncReader：： GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) 。
    -   建立集區的每個緩衝區。
3.  設定讀取器或同步讀取器進行讀取。 如需詳細資訊，請參閱 [使用非同步讀取器讀取](reading-files-with-the-asynchronous-reader.md) 檔案，或 [使用同步讀取器讀取](reading-files-with-the-synchronous-reader.md)檔案。
4.  開始撰寫之前，請針對您要使用 reader 物件配置緩衝區的每個輸出和資料流程，呼叫 [**IWMReaderAdvanced：： SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) 或 [**IWMReaderAdvanced：： SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) 。 若為同步讀取器，請改為呼叫 [**IWMSyncReader2：： SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) 或 [**IWMSyncReader2：： SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) 。
5.  開始讀取檔案。

讀取物件將會呼叫適當的配置器回呼，並從您的應用程式取得範例。 您的緩衝區管理邏輯必須包含一個方法，告知緩衝區可自由使用。 一般來說，當轉譯其內容時，會將緩衝區放回集區。 視您的應用程式而定，您可能只需要在集區中有幾個緩衝區，或多個緩衝區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> </dl>

 

 




