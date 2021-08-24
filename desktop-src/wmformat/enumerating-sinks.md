---
title: 列舉接收
description: 列舉接收
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- Advanced Systems Format (ASF) ，列舉接收
- ASF (Advanced 系統格式) ，列舉接收
- Advanced Systems Format (ASF) 、接收
- ASF (Advanced 系統格式) 、接收
- 接收，列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b51b46f3efdf95902b1ca5b359227da845292c4b0f23dbf0bd52039fba151cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029069"
---
# <a name="enumerating-sinks"></a>列舉接收

寫入器可以有許多相關聯的接收。 您可以使用 [**IWMWriterAdvanced：： GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) 和 [**IWMWriterAdvanced：： GetSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink)來列舉已新增至寫入器的接收。

[從接收取得錯誤訊息](getting-error-messages-from-a-sink.md)的範例程式碼會示範接收列舉。

> [!Note]  
> 列舉接收時，為了回應 [**IWMWriter：： SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) 的呼叫所建立的預設檔案接收，會與您已新增的任何其他接收器一起列舉。 如果您只使用預設的檔案接收，您可以呼叫 **GetSink** 來存取接收器索引0。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMWriterAdvanced 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**使用寫入器接收器**](working-with-writer-sinks.md)
</dt> </dl>

 

 




