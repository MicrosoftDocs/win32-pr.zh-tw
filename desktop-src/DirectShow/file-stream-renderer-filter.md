---
description: 檔案資料流程轉譯器篩選
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: 檔案資料流程轉譯器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3da8651d61559a9b22b722f91563426cb067f7a3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470563"
---
# <a name="file-stream-renderer-filter"></a>檔案資料流程轉譯器篩選

檔案資料流程轉譯器篩選器會轉譯由 [多](multi-file-parser-filter.md) 檔案剖析器篩選器剖析的檔案名。 如需詳細資訊，請參閱該篩選器的檔。

此篩選器的使用已被取代。 若要在相同的篩選圖形中轉譯多個檔案，應用程式應該只呼叫 **RenderFile** 或 **AddSourceFilter** 多次。




| | |篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | |輸入 pin 媒體類型 | <ul><li>主要類型： MEDIATYPE_File</li><li>子類型： GUID_Null</li><li>格式類型： MEDIATYPE_File</li></ul> | |輸入 pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |輸出釘選媒體類型 |無 | |輸出 pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a> | |篩選 CLSID |CLSID_FileRend | |可執行檔 |Quartz.dll | | <a href="merit.md">業績</a> |MERIT_UNLIKELY | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>備註

篩選的 CLSID 未定義于 Uuid. h 中。 在您自己的標頭檔中使用此宏：


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



