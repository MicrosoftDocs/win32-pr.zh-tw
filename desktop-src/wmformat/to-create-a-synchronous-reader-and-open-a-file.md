---
title: 建立同步讀取器並開啟檔案
description: 建立同步讀取器並開啟檔案
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- Advanced Systems Format (ASF) ，建立讀取器
- ASF (Advanced Systems Format) ，建立讀取器
- Advanced Systems Format (ASF) ，開啟檔案
- ASF (Advanced Systems Format) ，開啟檔案
- 同步讀取器，建立
- 同步讀取器，開啟檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d1c6897c05bb0d843e5818f078df5235a5afac4a485d6a719ab86b8e4f8267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807648"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a>建立同步讀取器並開啟檔案

在您可以使用同步讀取器執行任何工作之前，您必須先建立同步讀取器物件，並載入要讀取的檔案。 若要初始化同步讀取器並開啟檔案，請執行下列步驟。

1.  藉由呼叫 [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) 函數來建立同步讀取器物件。 您必須為新的讀取器物件指定所需的版權管理層級。 可用的模式會列在 **WMT \_ 許可權** 列舉型別中。
2.  藉由呼叫 [**IWMSyncReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open)，指定要讀取的檔案。

同步讀取器也支援使用 **IStream** COM 介面來開啟檔案。 您可以選擇任何方式來執行 **IStream** 介面。 在 **IStream** 中開啟所需的檔案之後，您可以依照上面所列的步驟，但您必須在步驟2中呼叫 [**IWMSyncReader：： OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) 而不是 **IWMSyncReader：： Open** 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMSyncReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**使用同步讀取器讀取檔案**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




