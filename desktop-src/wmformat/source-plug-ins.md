---
title: 來源外掛程式
description: 來源外掛程式
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- Windows媒體格式 SDK，來源外掛程式
- Advanced Systems Format (ASF) 、source 外掛程式
- ASF (Advanced Systems Format) 、source 外掛程式
- 來源外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f16d0edc82423a43e50591fa07e14623adc23b94234a28985afca8a496822a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845802"
---
# <a name="source-plug-ins"></a>來源外掛程式

來源外掛程式是一種可供開發人員使用的選項，可讓想要為 Windows 媒體®檔執行自己的儲存系統。 來源外掛程式可讓您透過執行稱為 **IStream** 的 COM 介面，這是提供資料的標準介面。

來源外掛程式應以 dll 的形式寫入，而 SDK 會透過登錄專案對其提供已知的狀態。 您可以用這種方式來執行任何數量的來源外掛程式。 來源外掛程式必須匯出 [**WMCreateStreamForURL**](wmcreatestreamforurl.md) 函式。

若要註冊來源外掛程式，應新增下列登錄專案：

HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows 媒體 \\ WMSDK \\ 來源

Name = "任何唯一名稱"

值 = 來源外掛程式 dll 的路徑名稱

註冊 dll 之後，應用程式可以使用 **IWMReader：： Open** 方法 (搭配適當的 URL 做為參數) 來存取串流資料，而這些資料可以儲存在檔案或使用者定義的資料容器中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[**程式設計參考**](programming-reference.md)
</dt> <dt>

[**WMCreateStreamForURL**](wmcreatestreamforurl.md)
</dt> </dl>

 

 




