---
description: 內部指令碼命令轉譯器篩選
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: 內部指令碼命令轉譯器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b241643d991e9348015dc51ea5b2f1c4875f079d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510060"
---
# <a name="internal-script-command-renderer-filter"></a>內部指令碼命令轉譯器篩選

接收指令碼命令，並將它們分派至應用程式。

此篩選器會以下列兩種格式之一接受指令碼命令：

-   媒體 \_ 型文字：每個媒體範例都包含一個 ANSI 文字字串。
-   媒體 \_ 型 ScriptCommand：每個媒體範例都包含兩個以 Null 終止的 Unicode 字串，串連在一起。 第一個字串描述命令類型，而第二個字串則是指令碼命令。

    當篩選準則收到範例時，它會傳送 [**EC \_ OLE \_ 事件**](ec-ole-event.md) 事件通知。 第一個事件參數是具有命令類型的 **BSTR** ，或 `Text` 如果格式為媒體文字，則為 \_ 。 第二個事件參數是具有指令碼命令的 **BSTR** 。 應用程式可以取出事件並回應指令碼命令。

如需如何使用此篩選準則的範例，請參閱 [薩米文 (CC) ](sami--cc--parser-filter.md)剖析器。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>篩選介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>輸入 Pin 媒體類型</td>
<td><ul>
<li>MEDIATYPE_ScriptCommand，MEDIASUBTYPE_Null</li>
<li>MEDIATYPE_Text，MEDIASUBTYPE_Null</li>
</ul></td>
</tr>
<tr class="odd">
<td>輸入 Pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>輸出 Pin 媒體類型</td>
<td>不適用</td>
</tr>
<tr class="odd">
<td>輸出 Pin 介面</td>
<td>不適用</td>
</tr>
<tr class="even">
<td>篩選 CLSID</td>
<td>{48025243-2D39-11CE-875D-00608CB78066}</td>
</tr>
<tr class="odd">
<td>屬性頁 CLSID</td>
<td>沒有屬性頁</td>
</tr>
<tr class="even">
<td>可執行檔</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">優點</a></td>
<td>MERIT_PREFERRED + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">篩選準則分類</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



