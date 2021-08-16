---
title: DSP 外掛程式介面
description: DSP 外掛程式介面
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Windows Media Player 外掛程式、DSP 介面
- Windows Media Player 外掛程式，介面
- 外掛程式、DSP 介面
- 外掛程式，介面
- 數位信號處理外掛程式，介面
- 數位信號處理外掛程式，ISpecifyPropertyPage 介面
- DSP 外掛程式，介面
- DSP 外掛程式，ISpecifyPropertyPage 介面
- 介面、DSP 外掛程式
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bd030b09377adfe965698d6c411f1a39a745979f2db2eae9f0c613cad843d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863368"
---
# <a name="dsp-plug-in-interfaces"></a>DSP 外掛程式介面

數位信號處理 (DSP) 外掛程式介面，用來管理 Windows Media Player 和外掛程式之間的資料傳輸。 所有的 DSP 外掛程式都可以選擇性地執行 **ISpecifyPropertyPage** 介面，以提供屬性頁面的執行。

需要下列介面才能建立 DSP 外掛程式。



| 介面                                                | 描述                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IMediaObject**                                         | 使用 Windows Media Player 管理資料交換，並執行數位信號處理工作。 DirectX SDK 包含詳細的檔。 |
| [IWMPMediaPluginRegistrar](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | 管理外掛程式註冊。                                                                                                                          |
| [IWMPPlugin](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | 管理 Windows Media Player 的連接。                                                                                                        |
| [IWMPPluginEnable](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | 儲存 Windows Media Player 目前是否已啟用外掛程式。                                                                               |
| [IWMPServices](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | 從玩家抓取目前資料流程時間和資料流程狀態的相關資訊。                                                                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DSP 外掛程式程式設計參考**](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




