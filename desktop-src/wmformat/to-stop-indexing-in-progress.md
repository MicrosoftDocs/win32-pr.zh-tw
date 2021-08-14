---
title: 若要停止進行編制索引
description: 若要停止進行編制索引
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- Windows媒體格式 SDK，正在停止編制索引
- Advanced Systems Format (ASF) ，正在停止編制索引
- ASF (Advanced Systems Format) ，正在停止編制索引
- 索引，正在停止編制索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d441e42bc3c7033e776d353cf64fc5938183a4f8d720f086b4fb5fd9828be02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432621"
---
# <a name="to-stop-indexing-in-progress"></a>若要停止進行編制索引

當您開始使用 [**IWMIndexer：： StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing)的呼叫來編制索引時，索引子通常會繼續進行，直到檔案編制索引為止。 您可以藉由呼叫 [**IWMIndexer：： Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) 方法來停止編制索引作業。 取消編制索引之後，您可以再次呼叫 **StartIndexing** ，但索引子會從檔案的開頭開始，而不是從取消點繼續。

由於 **StartIndexing** 是非同步呼叫，因此您通常需要從應用程式中的其他執行緒或事件處理常式呼叫 **Cancel** 。 通常會從與 Windows 應用程式的按鈕控制項相關聯的事件程式中呼叫 **Cancel** 。

取消編制索引時，索引子會傳遞 WMT 已關閉的狀態訊息 \_ ，就像檔案已正確編制索引一樣。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMIndexer 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**使用索引**](working-with-indexes.md)
</dt> </dl>

 

 




