---
title: 管理封包大小
description: 管理封包大小
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows媒體格式 SDK，管理封包大小
- Windows媒體格式 SDK，封包大小
- 設定檔，封包大小
- 設定檔，管理封包大小
- 封包，大小
- 封包，IWMPacketSize 介面
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b8755eccdcc0042532be4359cd51fce2ef379b51882e6cc4585c48c8769a55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846710"
---
# <a name="managing-packet-size"></a>管理封包大小

寫入器是設計用來管理內部的封包大小。 不過，您可能會有應用程式的特定需求，而這些需求會以手動方式控制您所撰寫之 ASF 檔案中的封包大小。 Windows 媒體格式 SDK 提供兩種介面： [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)和 [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) ，可讓您控制封包的大小上限和最小值。

這兩個封包大小介面都會公開于設定檔物件中。 讀取器物件也可以使用它們。 如同其他設定檔相關的介面，讀取器只能存取讀取方法。

封包大小對效能有一些影響。 一般而言，封包大小越小，檔案內的資料就越分散。 檔案越分散，重建它的效率就愈低。 在串流處理案例中，這可能不是很重要的考慮，因為從網際網路來源讀取檔案的程式通常沒有效率。 不過，在本機處理檔案時，這可能是一個考慮。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMPacketSize 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[**IWMPacketSize2 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[**使用設定檔**](working-with-profiles.md)
</dt> </dl>

 

 




