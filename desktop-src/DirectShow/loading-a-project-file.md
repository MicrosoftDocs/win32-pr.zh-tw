---
description: 載入專案檔
ms.assetid: f8d142bd-e51d-4714-893b-8e3d02506891
title: 載入專案檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9a710795a29481740bf85390cc7122cc801a22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187470"
---
# <a name="loading-a-project-file"></a>載入專案檔

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

若要載入專案檔，您需要兩個元件： XML 剖析器和空白的時間軸。 XML 剖析器會讀取 XML 專案檔，並建立檔案中定義的每個物件。 然後，它會將物件插入至時間軸，並設定任何時間軸屬性，例如預設的畫面播放速率。 下列程式碼範例會載入檔案。


```C++
HRESULT         hr;
IAMTimeline     *pTL = NULL;
IXml2Dex        *pXML = NULL; 
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
            IID_IAMTimeline, (void**)&pTL);
hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
            IID_IXml2Dex, (void**)&pXML);
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
hr = pXML->ReadXMLFile(pTL, bstrFile); 
SysFreeString(bstrFile);
pXML->Release();
```



剖析器會公開 [**IXml2Dex**](ixml2dex.md) 介面，其中包含載入和儲存專案檔案的方法。 時間軸會顯示 [**IAMTimeline**](iamtimeline.md) 介面，其中包含操作時間軸和建立新時程表物件的方法。 呼叫 **CoCreateInstance** 函數以建立每個元件，如下所示。 請記住，藉由建立新的實例，您將會遞增介面上的參考計數。 若要避免記憶體流失，請一律在使用介面時釋放介面。 在此範例中，不需要 **IXml2Dex** 的指標來進行任何動作，因此您可以釋放介面。 預覽時間軸仍需要 **IAMTimeline** 的指標。

[**IXml2Dex：： ReadXMLFile**](ixml2dex-readxmlfile.md)方法會讀取指定的檔案，並將檔案中定義的物件填入時間軸。 使用 **BSTR** 值指定檔案名。 為了縮短範例，範例中的檔案名會以常值字串的形式提供。 一般來說，您可以從 [開啟檔案] 對話方塊或類似的內容取得它。

如果 **ReadXML** 方法成功，它會傳回成功的程式碼。 否則，它會傳回錯誤碼，例如 VFW \_ E \_ 不正確 \_ 檔 \_ 格式。 請一律檢查傳回值，以便正常地處理錯誤狀況。 同樣地，為了簡潔起見，範例程式碼不會檢查錯誤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[載入和預覽專案](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



