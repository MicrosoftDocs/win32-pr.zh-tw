---
description: 建立 ASF 分隔器物件
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: 建立 ASF 分隔器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42c8033a0861102f6d66b22e43516a616d6428b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847638"
---
# <a name="creating-the-asf-splitter-object"></a>建立 ASF 分隔器物件

ASF *分隔器* 物件是 WMContainer 層物件，可剖析 Advanced Systems 格式的 Asf 資料物件 (asf) 檔。 若要建立 ASF 分隔器物件的新實例，請呼叫 [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) 函數。 此函式會傳回 [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) 介面的指標，該介面表示空的分隔器物件。

在分隔器開始剖析之前，應用程式必須使用 ASF 標頭物件的資訊來初始化分隔器。 若要初始化分隔器，請呼叫 [**IMFASFSplitter：： initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) 方法。 這個方法會採用 [Asf ContentInfo 物件](asf-contentinfo-object.md) 的指標，其中包含要剖析之 ASF 檔案的標頭資訊。 應用程式必須先初始化 ContentInfo 物件，才能將它傳遞給分隔器，讓應用程式知道媒體檔案的特性。 分隔器的 **Initialize** 方法會從 ContentInfo 物件（例如資料流程號碼）解壓縮資料流程資訊，讓分隔器可以剖析資料封包。

### <a name="example"></a>範例

下列程式碼範例示範如何建立分隔器，並使用現有的 ContentInfo 物件將它初始化。


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



> [!Note]  
> 此範例會使用 [SafeRelease](saferelease.md) 函式來釋放介面指標。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 分隔器](asf-splitter.md)
</dt> </dl>

 

 



