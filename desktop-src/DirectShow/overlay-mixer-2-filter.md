---
description: 覆蓋混音器2篩選
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: 覆蓋混音器2篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22976a58b272cf04c098c102d32d154e361b8b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106997467"
---
# <a name="overlay-mixer-2-filter"></a>覆蓋混音器2篩選

覆迭混音器2篩選與覆迭 [混音](overlay-mixer-filter.md) 器篩選器相同，不同之處如下：

-   它僅支援具有 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式的媒體類型。
-   它有更高的優點，可讓它自動新增至篩選圖形。

系統會提供重迭混音器2，讓篩選圖形管理員在轉譯非 DVD MPEG-2 影片時，將它新增至圖形。 選擇是否要使用覆迭混音器或覆迭混音器2，是由建立圖形的元件（[篩選圖形管理員]、[Capture Graph Builder] 或 [DVD 圖形產生器]）所處理。 從應用程式的觀點來看，它們是相同的篩選器，具有相同的介面和功能。

下表包含重迭混音器2的特定資訊。 針對其他所有篩選資料，請參閱重迭混音器的檔。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>輸入 Pin 媒體類型</td>
<td>格式類型： Format_VIDEOINFO2</td>
</tr>
<tr class="even">
<td>篩選 CLSID</td>
<td>CLSID_OverlayMixer2</td>
</tr>
<tr class="odd">
<td><a href="merit.md">優點</a></td>
<td><ul>
<li>MERIT_UNLIKELY</li>
<li>Windows Vista 或更新版本： MERIT_DO_NOT_USE</li>
</ul></td>
</tr>
</tbody>
</table>



 

在 Windows Vista 或更新版本中， \_ \_ \_ 因為較新的影片轉譯器 (VMR-7、VMR-9 和 EVR) 全部支援 **VIDEOINFOHEADER2** 格式，所以不需要使用覆迭混音器，因此不會使用覆迭混音器2篩選器的優點。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



