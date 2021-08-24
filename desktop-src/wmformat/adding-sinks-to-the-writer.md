---
title: 將接收器新增至寫入器
description: 將接收器新增至寫入器
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- Advanced Systems Format (ASF) ，將接收器新增至寫入器
- ASF (Advanced Systems Format) ，將接收器新增至寫入器
- Advanced Systems Format (ASF) 、接收
- ASF (Advanced 系統格式) 、接收
- Advanced Systems Format (ASF) 、寫入器接收
- ASF (Advanced 系統格式) 、寫入器接收
- 接收，加入寫入器
- 寫入器接收，加入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca64b412dd83e9bbba1d8de66b2aef335573c9e50073c2afe898fed0c34761b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810018"
---
# <a name="adding-sinks-to-the-writer"></a>將接收器新增至寫入器

寫入器接收是與寫入器不同的物件，而且必須加入至要使用的寫入器。 如果您要寫入檔案，您可以直接呼叫 [**IWMWriter：： SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename)，這會自動設定 file sink。 否則，若要將接收新增至寫入器，請呼叫 [**IWMWriterAdvanced：： AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) 方法。 **AddSink** 需要接收器的 [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) 介面指標。

當您完成使用接收時，您應該呼叫適當的方法來關閉它，視接收的類型而定，然後呼叫 [**IWMWriterAdvanced：： RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink)將它從寫入器中移除。

下列範例程式碼示範如何建立寫入器檔案接收，並將其新增至寫入器。 如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。


```C++
HRESULT AddFileSink(IWMWriterFileSink** ppFileSink, IWMWriter* pWriter)
{
    HRESULT hr = S_OK;
    IWMWriterSink*     pSinkBase       = NULL;
    IWMWriterAdvanced* pWriterAdvanced = NULL;

    hr = CreateWriterFileSink(ppFileSink);
    GOTO_EXIT_IF_FAILED(hr);

    hr = *ppFileSink->QueryInterface(IID_IWMWriterSink, 
                                     (void**) &pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced,
                                 (void**) &pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriterAdvanced->AddSink(pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

Exit:
    SAFE_RELEASE(pSinkBase);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**從接收取得錯誤訊息**](getting-error-messages-from-a-sink.md)
</dt> <dt>

[**IWMWriterAdvanced 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**使用寫入器接收器**](working-with-writer-sinks.md)
</dt> </dl>

 

 




