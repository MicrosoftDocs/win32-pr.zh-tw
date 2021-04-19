---
title: 緩衝區物件
description: 緩衝區物件
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- Windows Media 格式 SDK，緩衝區物件
- Advanced Systems Format (ASF) ，buffer 物件
- ASF (Advanced Systems Format) ，buffer 物件
- 物件，緩衝區物件
- 緩衝區物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a9a3c6acfa0b0780b07f2853f60fdd68d0eaf
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "106968271"
---
# <a name="buffer-object"></a>緩衝區物件

緩衝區物件是用來保存範例，並在 Windows Media 格式 SDK 的物件和您的應用程式之間傳遞它們。 當您寫入檔案時，您會使用緩衝區物件，將輸入範例傳遞給寫入器。 當您讀取檔案時，讀取器物件或同步讀取器物件會在緩衝區物件中提供應用程式的範例。

針對將範例寫入檔案，您可以使用 [**IWMWriter：： AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) 方法建立緩衝區物件。 若要讀取範例，讀取器物件和同步讀取器物件都會在內部建立緩衝區物件。 如果您選擇，您可以使用 [**IWMReaderAllocatorEx：： AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) 或 [**IWMReaderAllocatorEx：： AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)，配置您自己的緩衝區物件來讀取檔案。

每個緩衝區物件都支援下列介面。



| 介面                          | 描述                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | 控制項並提供緩衝區的存取權。                          |
| [**INSSBuffer2**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | 未實作。                                                     |
| [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | 支援用於資料單位延伸的緩衝區屬性。 |
| [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | 列舉緩衝區屬性。                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> </dl>

 

 




