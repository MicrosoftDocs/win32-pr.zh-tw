---
description: 本主題提供有關建立媒體基礎所提供之預設索引子物件的資訊。
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: 建立和設定索引子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e97bb558866fda021245b1597ead2a073c659c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193779"
---
# <a name="indexer-creation-and-configuration"></a>建立和設定索引子

ASF *索引子* 是 WMContainer 層元件，可用來以 Advanced 系統格式讀取或寫入索引物件 (ASF) 檔。 本主題提供有關建立媒體基礎所提供之預設索引子物件的資訊。

如需 ASF 檔案結構的詳細資訊，請參閱 [asf 檔案結構](asf-file-structure.md)。

**建立並初始化 ASF 索引子**

1.  呼叫 [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) 函數，以接收索引子物件的 [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) 指標。
2.  呼叫 [**IMFASFIndexer：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) 來指定索引子物件的讀取或寫入模式。 根據預設，索引子會設定為向前搜尋。

    

    | 使用                       | 旗標                                           |
    |---------------------------|------------------------------------------------|
    | 讀取 (向前搜尋)  | 零 (預設值)                                  |
    | 讀取 (反向搜尋)  | **\_REVERSEPLAYBACK 的 MFASF 索引子 \_ 讀取 \_ \_** |
    | 寫入                   | MFASF \_ 索引子 \_ 寫入 \_ 新的 \_ 索引              |

    

     

    > [!Note]  
    > 相同的索引子實例無法用於讀取和寫入。 您必須設定一個或另一個的索引子。

     

3.  呼叫 [**IMFASFIndexer：： initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) 以初始化索引子，方法是指定 ContentInfo 物件的 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 指標，以描述要寫入或讀取的檔案。 ContentInfo 物件包含構成 [ASF 標頭物件](asf-file-structure.md)的資訊。 在產生或讀取 ASF 檔案的索引項目之前，索引子物件需要有效的 ContentInfo 物件。

下列程式碼範例會示範應用程式如何建立和初始化索引子物件，以使用特定的 ASF 內容。 ContentInfo 物件代表 ASF 標頭物件;內容會以位元組資料流程的形式傳遞。


```C++
HRESULT CreateASFIndexer(
    IMFASFContentInfo* pContentInfo, 
    DWORD dwFlags,
    IMFASFIndexer** ppIndexer
    )
{
    *ppIndexer = NULL;

    IMFASFIndexer *pIndexer = NULL;

    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pIndexer->SetFlags(dwFlags);
    if (FAILED(hr))
    {
        goto done;
    }

    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the object to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    // Clean up.
    SafeRelease(&pIndexer);
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 索引子](asf-index-object.md)
</dt> <dt>

[使用索引子在 ASF 檔案內搜尋](using-the-indexer-to-seek.md)
</dt> <dt>

[使用索引子來寫入新的索引](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



