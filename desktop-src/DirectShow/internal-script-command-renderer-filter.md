---
description: 內部指令碼命令轉譯器篩選
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: 內部指令碼命令轉譯器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b70fbcd7dc6347ec93a19558ef2306dffd5fb64
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982211"
---
# <a name="internal-script-command-renderer-filter"></a>內部指令碼命令轉譯器篩選

接收指令碼命令，並將它們分派至應用程式。

此篩選器會以下列兩種格式之一接受指令碼命令：

-   媒體 \_ 型文字：每個媒體範例都包含一個 ANSI 文字字串。
-   媒體 \_ 型 ScriptCommand：每個媒體範例都包含兩個以 Null 終止的 Unicode 字串，串連在一起。 第一個字串描述命令類型，而第二個字串則是指令碼命令。

    當篩選準則收到範例時，它會傳送 [**EC \_ OLE \_ 事件**](ec-ole-event.md) 事件通知。 第一個事件參數是具有命令類型的 **BSTR** ，或 `Text` 如果格式為媒體文字，則為 \_ 。 第二個事件參數是具有指令碼命令的 **BSTR** 。 應用程式可以取出事件並回應指令碼命令。

如需如何使用此篩選準則的範例，請參閱 [薩米文 (CC) ](sami--cc--parser-filter.md)剖析器。




| 標籤 | 值 |
|--------|-------|
| 篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a> | 
| 輸入 Pin 媒體類型 | <ul><li>MEDIATYPE_ScriptCommand，MEDIASUBTYPE_Null</li><li>MEDIATYPE_Text，MEDIASUBTYPE_Null</li></ul> | 
| 輸入 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| 輸出 Pin 媒體類型 | 不適用 | 
| 輸出 Pin 介面 | 不適用 | 
| 篩選 CLSID | {48025243-2D39-11CE-875D-00608CB78066} | 
| 屬性頁 CLSID | 沒有屬性頁 | 
| 可執行檔 | Quartz.dll | 
| <a href="merit.md">優點</a> | MERIT_PREFERRED + 1 | 
| <a href="filter-categories.md">篩選準則分類</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



