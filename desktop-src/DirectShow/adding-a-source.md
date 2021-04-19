---
description: 新增來源
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: 新增來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee583cd8971c183f2e03b92f68e2d6ba555c41db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106979709"
---
# <a name="adding-a-source"></a>新增來源

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

建立來源物件的方式與建立其他時程表物件的方式相同。 不過，在將它插入至時間軸之前，您必須至少在來源上指定下列屬性。

-   相對於時間軸的開始和停止時間。 呼叫 [**IAMTimelineObj：： SetStartStop**](iamtimelineobj-setstartstop.md) 方法。
-   要做為來源使用的媒體檔案。 使用代表檔案名的寬字元字串來呼叫 [**IAMTimelineSrc：： SetMediaName**](iamtimelinesrc-setmedianame.md) 方法。
-   媒體開始和停止時間，相對於原始檔案。 呼叫 [**IAMTimelineSrc：： SetMediaTimes**](iamtimelinesrc-setmediatimes.md) 方法。 如需媒體時間的詳細資訊，請參閱 [DirectShow 編輯服務中的時間](time-in-directshow-editing-services.md)。

在下列範例中，來源剪輯會在檔案中開始四秒。 媒體持續時間為10秒，時間軸持續時間長度的兩倍，表示來源會以兩倍的一般速度播放。 常數單位定義為 10000000 (10 ^ 7) ，等於1秒。


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> 目前，DES 無法同時轉譯超過75個以視訊壓縮管理員壓縮的來源 (BC-VCM-LVM-HYPERV) 編解碼器。 此外，如果整個專案包含75以上的來源，您必須使用動態重新連接，否則 DES 無法預覽專案。 如需詳細資訊，請參閱 [**IRenderEngine：： SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)。

 

如需來源的詳細資訊，請參閱 [使用來源](working-with-sources.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立時間軸](constructing-a-timeline.md)
</dt> </dl>

 

 



