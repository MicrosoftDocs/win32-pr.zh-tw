---
title: 使用頻寬共用
description: 使用頻寬共用
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- Windows Media Format SDK，頻寬共用
- 頻寬共用、關於
- 設定檔，頻寬共用
- 串流，頻寬共用
- 頻寬共用，IWMProfile 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104374813"
---
# <a name="using-bandwidth-sharing"></a>使用頻寬共用

您可以使用頻寬共用物件來指定特定資料流程合併時，不會使用超過指定的頻寬。 頻寬共用物件中的資訊不會由寫入器產生或驗證，讀取器也不會使用它來進行任何作業。

寫入設定檔中有頻寬共用資訊的檔案時，資料會儲存在其標頭區段中。 播放檔案時，您可以使用讀取器中的 [**IWMProfile**](iwmprofile.md) 介面來檢查頻寬共用資訊。

每個頻寬共用物件都是由兩個設定所定義。 第一個是頻寬，如頻寬和緩衝區視窗所定義。 第二個設定是頻寬共用類型，可以是專有或部分。 獨佔頻寬共用表示會一次播放一次組成的資料流程，而部分表示資料流程會同時傳遞。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMProfile 介面**](iwmprofile.md)
</dt> <dt>

[**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[**IWMProfile3::GetBandwidthSharingCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[**使用設定檔**](working-with-profiles.md)
</dt> </dl>

 

 




