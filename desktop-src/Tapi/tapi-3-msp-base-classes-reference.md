---
description: 下列材質提供媒體服務提供者基類的詳細資料。
ms.assetid: ef845c44-1ff5-42a1-8e91-38d66e6fe363
title: TAPI 3 MSP 基類參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4cca24b69a645b18cc0950288e0de983b54355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192731"
---
# <a name="tapi-3-msp-base-classes-reference"></a>TAPI 3 MSP 基類參考

下列材質提供媒體服務提供者基類的詳細資料。



| 媒體服務提供者基底類別 (字母順序)  | Description                                                                                                                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CAudioCaptureTerminal](caudiocaptureterminal.md)       | 衍生自 [CSingleFilterTerminal](csinglefilterterminal.md) ，並使用 DirectShow wavein 篩選器為 wave 裝置實行靜態音訊捕獲終端機。 定義于 MSPtmac 中。               |
| [CAudioRenderTerminal](caudiorenderterminal.md)         | 衍生自 [CSingleFilterTerminal](csinglefilterterminal.md) ，並使用 DirectShow waveout 篩選器來為 wave 裝置實行靜態音訊轉譯終端機。 定義于 MSPtrmar 中。              |
| [CBaseTerminal](cbaseterminal.md)                       | 適用于靜態和動態終端的終端基類。 它完全是泛型，因此任何的終端機都可以直接或間接衍生自這個類別。 定義于 MSPterm .h 中 |
| [**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)                       | 會實作為 MSP 位址物件，並支援 [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) 介面。 定義于 MSPaddr 中。                                                                                |
| [CMSPArray](cmsparray.md)                               | 此範本會執行隨需成長的智慧陣列。 定義于 MSPutils 中。                                                                                                               |
| [**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)                     | 提供呼叫物件的泛型實作為，並支援 [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) 介面。 定義于 MSPcall 中。                                                       |
| [**CMSPCallMultiGraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)         | 定義針對每個資料流程使用篩選圖形的呼叫。 定義于 MSPcall 中。                                                                                                                          |
| [**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)                         | 公開方法，以允許應用程式啟動、暫停或停止子流，以及選取或取消選取終端。 定義于 MSPstrm 中。                                                              |
| [CMSPThread](cmspthread.md)                             | 實行 MSP 的背景工作執行緒。 定義于 MSPthrd 中。                                                                                                                                               |
| [CSingleFilterTerminal](csinglefilterterminal.md)       | 另一個適用于靜態和動態終端的終端基類。 假設終端機有單一的 DirectShow 篩選器，讓更明確地執行。 定義于 MSPterm 中。    |
| [CVideoCaptureTerminal](cvideocaptureterminal.md)       | 衍生自 [CSingleFilterTerminal](csinglefilterterminal.md) ，並使用單一 DirectShow 篩選器來實行靜態影片捕捉終端機。 定義于 MSPtmvc 中。                                  |



 

 

 
