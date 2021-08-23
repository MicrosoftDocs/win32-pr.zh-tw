---
title: 將腳本資料新增至標頭
description: 將腳本資料新增至標頭
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- Windows媒體格式 SDK，將腳本資料新增至標頭
- Advanced Systems Format (ASF) ，將腳本資料新增至標頭
- ASF (Advanced Systems Format) ，將腳本資料新增至標頭
- 腳本，將資料加入至標頭
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19a8ad34a69427dc26435a6a599b8d91db2ebe2b8be700483189b2e7ba22846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027316"
---
# <a name="to-add-script-data-to-the-header"></a>將腳本資料新增至標頭

您可以在 ASF 檔案的標頭中包含指令碼命令。 若要在編碼時將指令碼命令寫入標頭，請執行下列步驟。 在呼叫 [**IWMWriter：： BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)之前，請先執行下列步驟。

1.  藉由呼叫 **IWMWriter：： QueryInterface** 來取得 **IWMHeaderInfo** 介面的指標。
2.  藉由呼叫 [**IWMHeaderInfo：： AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript)來新增每個所需的指令碼命令。 每個呼叫會分別採用兩個字串，並將呈現時間用於命令作為參數。

當應用程式讀取檔案時，它將需要取出所有的指令碼命令。 若要在檔案的標頭中尋找所有指令碼命令，請執行下列步驟。 這應該會在開始播放之前完成。

1.  藉由呼叫物件中另一個介面的 **QueryInterface** 方法，取得讀取器物件 (或同步讀取器物件) 的 **IWMHeaderInfo** 介面指標。
2.  藉由呼叫 [**IWMHeaderInfo：： GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount)，取得標頭中的腳本總數。
3.  使用 [**IWMHeaderInfo：： >getscript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript)的呼叫，以迴圈方式逐一查看標頭中的所有腳本。
4.  建立展示時間清單，讓您的應用程式可以在適當的時間回應命令。

> [!Note]  
> 使用 DRM 加密檔案時，沒有指令碼命令可以有0的呈現時間。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMHeaderInfo 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMWriter 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**使用指令碼命令**](using-script-commands.md)
</dt> </dl>

 

 




