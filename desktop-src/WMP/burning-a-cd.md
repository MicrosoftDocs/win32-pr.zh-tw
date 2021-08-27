---
title: 燒錄 CD
description: 燒錄 CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Windows Media Player、CD 燒錄
- Windows Media Player 物件模型，CD 燒錄
- 物件模型，CD 燒錄
- Windows Media Player ActiveX 控制項、CD 燒錄
- ActiveX 控制項，CD 燒錄
- Windows Media PlayerMobile ActiveX control、CD 燒錄
- Windows Media Player行動電話、CD 燒錄
- CD 燒錄，關於
- 燒錄 Cd，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c7cfee7468b2cd376b7b25d4cff4a04e0d057dcc7a792ac7471843de2b74a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118840767"
---
# <a name="burning-a-cd"></a>燒錄 CD

本節說明如何使用 [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) 介面將音樂燒錄至 CD。 **IWMPCdromBurn** 介面提供將播放清單燒錄至 cd 的功能，以作為資料或音訊播放軌，以及清除 cd RWs。

程式碼使用方式

本節中的程式碼範例會使用 Active Template Library (ATL) 類別，例如 **CComPtr**。

包含的標頭

若要使用本節中的程式碼，請包含下列標頭：


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



介面指標

Windows Media Player 的介面會儲存在下列成員變數中：


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



下列主題描述如何使用 CD 燒錄 API。

-   [擷取 CD 燒錄介面](retrieving-the-cd-burning-interface.md)
-   [啟動燒錄流程](starting-the-burn-process.md)
-   [清除可讀寫 CD](erasing-a-rewritable-cd.md)
-   [正在抓取磁片磁碟機和光碟狀態](retrieving-the-drive-and-disc-status.md)
-   [正在取出燒錄狀態](retrieving-the-burn-status.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**播放機控制指南**](player-control-guide.md)
</dt> </dl>

 

 




