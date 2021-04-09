---
title: 建立讀取器並開啟檔案
description: 建立讀取器並開啟檔案
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- Advanced Systems Format (ASF) ，建立讀取器
- ASF (Advanced Systems Format) ，建立讀取器
- Advanced Systems Format (ASF) ，開啟檔案
- ASF (Advanced Systems Format) ，開啟檔案
- 非同步讀取器，建立
- 非同步讀取器，開啟檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681555"
---
# <a name="to-create-a-reader-and-open-a-file"></a>建立讀取器並開啟檔案

在您可以使用讀取器執行任何工作之前，您必須先建立讀取器物件，並載入檔案進行讀取。 若要初始化讀取器並開啟檔案，請執行下列步驟。

1.  藉由呼叫 [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) 函數來建立讀取器物件。 您必須為新的讀取器物件指定所需的版權管理層級。 可用的模式會列在 [**WMT \_ 許可權**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) 列舉型別中。
2.  藉由呼叫 [**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)，指定要讀取的檔案。 您必須指定讀取器回呼介面，讓讀取器使用。 如需讀取器回呼的詳細資訊，請參閱 [在 OnStatus 回呼中執行讀取器訊息](to-implement-reader-messages-in-the-onstatus-callback.md)。
3.  等候讀取器開啟檔案。 當您呼叫 **Open** 來載入檔案時，它幾乎會立即傳回，並且在另一個執行緒上繼續處理。 您應等候作業完成，方法是在 **OnStatus** 回呼收到 WMT 開啟的狀態訊息時，發出事件的信號 \_ 。

讀取器也支援使用 **IStream** COM 介面來開啟檔案。 您可以選擇任何方式來執行 **IStream** 介面。 在 **IStream** 中開啟所需的檔案之後，您可以依照上面所列的步驟，但您必須在步驟2中呼叫 [**IWMReaderAdvanced2：： OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) 而不是 **IWMReader：： Open** 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMReaderAdvanced2 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**IWMStatusCallback 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[**使用非同步讀取器讀取檔案**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**使用回呼方法**](using-the-callback-methods.md)
</dt> </dl>

 

 




