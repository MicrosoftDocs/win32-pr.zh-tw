---
title: 停用自動編制索引
description: 停用自動編制索引
ms.assetid: 41fe18de-3a94-4001-83ce-0bb5dd086995
keywords:
- Windows Media Format SDK，停用自動編制索引
- Windows Media Format SDK，自動編制索引
- Advanced Systems Format (ASF) ，停用自動編制索引
- ASF (Advanced 系統格式) ，停用自動編制索引
- Advanced Systems Format (ASF) ，自動編制索引
- ASF (Advanced Systems Format) ，自動編制索引
- 索引，停用自動編制索引
- 索引，自動編制索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0235ddac8093d9b1c6d40fde341ee32d078b84b7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932939"
---
# <a name="to-disable-automatic-indexing"></a>停用自動編制索引

寫入 ASF 檔案時，預設不一定會想要產生索引。 您可以使用 [**IWMWriterFileSink3：： SetAutoIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setautoindexing) 方法停用自動編制索引。

下列範例程式碼示範如何停用寫入器的自動編制索引。


```C++
IWMWriterFileSink*  pBaseFileSink = NULL;
IWMWriterFileSink3* pMySink       = NULL;

BOOL    fAutoIndex;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer file sink.
hr = WMCreateWriterFileSink(&pBaseFileSink);

// Retrieve an IWMWriterFileSink3 interface pointer for the new sink.
hr = pBaseFileSink->QueryInterface(IID_IWMWriterFileSink3,
                                    (void**)&pMySink);

// Release the base file sink.
pBaseFileSink->Release();
pBaseFileSink = NULL;

// Check the state of automatic indexing.
hr = pMySink->GetAutoIndexing(&fAutoIndex);

// If auto indexing is enabled, turn it off.
if(fAutoIndex)
   pMySink->SetAutoIndexing(FALSE);

// You can now write to this sink and the file will not have an index.

// Release the remaining interface.
pMySink->Release();
pMySink = NULL;

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMWriterFileSink3::GetAutoIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getautoindexing)
</dt> <dt>

[**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)
</dt> <dt>

[**使用索引**](working-with-indexes.md)
</dt> </dl>

 

 




