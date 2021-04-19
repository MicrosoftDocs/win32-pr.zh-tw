---
description: 多重檔案剖析器篩選
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: 多重檔案剖析器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fc83a56bb12c307b85be875a3a2e7e73b744d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972312"
---
# <a name="multi-file-parser-filter"></a>多重檔案剖析器篩選

多重檔案剖析器篩選器會剖析簡單的檔案格式，讓您可以指定多個檔案名，就好像它們是一個檔案一樣。 這些檔案的格式如下範例所示：


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



此篩選器的使用已被取代。 若要在相同的篩選圖形中轉譯多個檔案，應用程式應該只呼叫 **RenderFile** 或 **AddSourceFilter** 多次。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>篩選介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>輸入 pin 媒體類型</td>
<td><ul>
<li>主要類型： MEDIATYPE_Stream</li>
<li>子類型： CLSID_MultFile</li>
<li>格式類型： GUID_Null</li>
</ul></td>
</tr>
<tr class="odd">
<td>輸入 pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>輸出 pin 媒體類型</td>
<td><ul>
<li>主要類型： MEDIATYPE_File</li>
<li>子類型： GUID_Null</li>
<li>格式類型： MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>輸出 pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>篩選 CLSID</td>
<td>CLSID_MultFile</td>
</tr>
<tr class="odd">
<td>可執行檔</td>
<td>Quartz.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">優點</a></td>
<td>MERIT_UNLIKELY</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">篩選準則分類</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

此篩選會針對原始程式檔中所列的每個檔案建立一個輸出圖釘。 輸出類型為「媒體類型」 \_ ，而輸出類型的格式區塊是包含檔案名的寬字元字串。 每個釘選都會連接到檔案 [資料流程](file-stream-renderer-filter.md) 轉譯器篩選準則的實例。 檔案資料流程轉譯器篩選器會建立一個輸出圖釘，以公開 [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) 介面。 輸出圖釘會轉譯指定的檔案。 在多檔案剖析器和檔案資料流程轉譯器之間，不會有媒體資料的移動。

篩選的 CLSID 未定義于 Uuid. h 中。 在您自己的標頭檔中使用此宏：


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



