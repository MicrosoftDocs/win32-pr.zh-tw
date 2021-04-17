---
description: 檔案資料流程轉譯器篩選
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: 檔案資料流程轉譯器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64c8d8a0c87dab3aa811c8246be24ded8ee04dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510240"
---
# <a name="file-stream-renderer-filter"></a>檔案資料流程轉譯器篩選

檔案資料流程轉譯器篩選器會轉譯由 [多](multi-file-parser-filter.md) 檔案剖析器篩選器剖析的檔案名。 如需詳細資訊，請參閱該篩選器的檔。

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
<li>主要類型： MEDIATYPE_File</li>
<li>子類型： GUID_Null</li>
<li>格式類型： MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>輸入 pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>輸出 pin 媒體類型</td>
<td>無</td>
</tr>
<tr class="odd">
<td>輸出 pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></td>
</tr>
<tr class="even">
<td>篩選 CLSID</td>
<td>CLSID_FileRend</td>
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

篩選的 CLSID 未定義于 Uuid. h 中。 在您自己的標頭檔中使用此宏：


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



