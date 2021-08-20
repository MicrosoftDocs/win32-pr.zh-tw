---
title: 管理寫入器延遲
description: 管理寫入器延遲
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Advanced Systems Format (ASF) ，管理寫入器延遲
- ASF (Advanced Systems Format) ，管理寫入器延遲
- Advanced Systems Format (ASF) ，寫入器延遲
- ASF (Advanced Systems Format) ，寫入器延遲
- 寫入器延遲
- 延遲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0adb18814cc8153ae81ed9517834d62345f18b61f51de6aacd38e9028699331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845478"
---
# <a name="to-manage-writer-latency"></a>管理寫入器延遲

寫入器會花一些時間來處理範例。 傳遞輸入範例和寫入輸出範例之間的時間長度，稱為寫入器的延遲。 有許多因素會導致寫入器延遲，而且您可以透過數種方式來減少。

寫入器延遲最明顯的因素是壓縮範例所需的時間。 在大部分的情況下，您將不會有太多控制權。 如果頻寬不是大問題，您可以使用較少的壓縮來降低延遲。 當然，您可以傳遞已壓縮的範例來達到最少的延遲。

下一個因素是您通常有控制權的因素，是範例傳遞給讀取器的順序。 您可以藉由以簡報時間的順序傳遞範例，以及確保輸入樣本在所有輸入資料流程之間有妥善的同步處理，以達到更好的延遲。 不同資料流程範例之間的呈現時間差異愈大，就會產生更多延遲。 您可以藉由呼叫 [**IWMWriterAdvanced：： SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance)，設定輸入樣本之間差異的最大值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 




