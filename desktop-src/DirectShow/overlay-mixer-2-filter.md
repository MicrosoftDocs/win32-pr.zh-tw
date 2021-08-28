---
description: 覆迭 Mixer 2 篩選
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: 覆迭 Mixer 2 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b51dceb2a7f82a91fe30275cacfaad4ad78eded
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987351"
---
# <a name="overlay-mixer-2-filter"></a>覆迭 Mixer 2 篩選

覆迭 Mixer 2 篩選與覆迭[Mixer](overlay-mixer-filter.md)篩選器相同，不同之處在于：

-   它僅支援具有 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式的媒體類型。
-   它有更高的優點，可讓它自動新增至篩選圖形。

系統會提供重迭 Mixer 2，讓篩選器 Graph 管理員在轉譯非 DVD mpeg-2 影片時將其新增至圖形。 選擇是否要使用覆迭 Mixer 或覆迭 Mixer 2 是由建立圖形的元件（篩選 Graph 管理員、Capture Graph Builder 或 DVD Graph 產生器）所處理。 從應用程式的觀點來看，它們是相同的篩選器，具有相同的介面和功能。

下表包含重迭 Mixer 2 的特定資訊。 針對其他所有篩選資料，請參閱覆迭 Mixer 的檔。




| 標籤 | 值 |
|--------|-------|
| 輸入 Pin 媒體類型 | 格式類型： Format_VIDEOINFO2 | 
| 篩選 CLSID | CLSID_OverlayMixer2 | 
| <a href="merit.md">優點</a> | <ul><li>MERIT_UNLIKELY</li><li>WindowsVista 或更新版本： MERIT_DO_NOT_USE</li></ul> | 




 

在 Windows Vista 或更新版本中， \_ \_ \_ 因為較新的影片轉譯器 (VMR-7、VMR-9 和 EVR) 全部支援 **VIDEOINFOHEADER2** 格式，所以不會使用重迭 Mixer 2 篩選器的優點，因此不需要使用重迭 Mixer。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



