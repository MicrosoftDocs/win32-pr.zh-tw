---
title: 頻寬共用
description: 頻寬共用
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- Windows媒體格式 SDK，頻寬共用
- Advanced Systems Format (ASF) 、頻寬共用
- ASF (Advanced 系統格式) 、頻寬共用
- Windows媒體格式 SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- 頻寬共用、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b01ff94e82f2ce3609a93278fef30c68e1a59445eea22f68f4b0a5d92371a19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709408"
---
# <a name="bandwidth-sharing"></a>頻寬共用

您可以在檔案中指定資料流程（當兩者一起使用）時，使用的頻寬比其所指定位速率的總和低。 藉由在設定檔中指定頻寬共用，您將會明確說明如何讀取應用程式，以串流檔案所需的可用頻寬，不是其他可能的情況。

Windows 媒體格式 SDK 的物件都不會變更其行為，以回應頻寬共用資訊，這只是為了讓讀取應用程式能在判斷檔案是否可以在受限制的頻寬傳遞時加以考慮。

頻寬共用的設定是使用頻寬共用物件，並在開始寫入檔案之前新增至設定檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ASF 檔案功能**](asf-file-features.md)
</dt> <dt>

[**頻寬共用物件**](bandwidth-sharing-object.md)
</dt> <dt>

[**IWMBandwidthSharing 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[**IWMProfile3 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[**使用頻寬共用**](using-bandwidth-sharing.md)
</dt> </dl>

 

 




