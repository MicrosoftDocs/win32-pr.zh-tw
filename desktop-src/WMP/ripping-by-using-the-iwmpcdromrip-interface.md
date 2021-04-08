---
title: 使用 IWMPCdromRip 介面進行翻錄
description: 使用 IWMPCdromRip 介面進行翻錄
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Windows Media Player、CD 翻錄
- Windows Media Player 物件模型，CD 翻錄
- 物件模型、CD 翻錄
- Windows Media Player ActiveX 控制項、CD 翻錄
- ActiveX 控制項，CD 翻錄
- Windows Media Player 的行動 ActiveX 控制項、CD 翻錄
- Windows Media Player 行動電話、CD 翻錄
- CD 翻錄，IWMPCdromRip 介面
- 將 Cd、IWMPCdromRip 介面翻錄
- IWMPCdromRip 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841908"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a>使用 IWMPCdromRip 介面進行翻錄

本節說明如何使用 [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) 介面，從 CD 翻錄音樂。

使用 **IWMPCdromRip** 介面來將 CD 翻錄，與使用 Windows Media Player 使用者介面來將音樂翻錄的效果相同。 已翻錄的內容會根據使用者的喜好設定自動新增至程式庫。 如需 CD 翻錄的詳細資訊，請參閱 Windows Media Player 說明中的「從 Cd 翻錄音樂」。

本節中的程式碼範例會使用 Active Template Library (ATL) 類別，例如 **CComPtr**。

## <a name="included-headers"></a>包含的標頭

若要使用本節中的程式碼，請包含下列標頭：


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a>介面指標

Windows Media Player 的介面會儲存在下列成員變數中。


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



下列各節說明如何使用 IWMPCdromRip 介面

-   [擷取轉錄介面](retrieving-the-ripping-interface.md)
-   [啟動 Rip 進程](starting-the-rip-process.md)
-   [正在抓取 Rip 狀態](retrieving-the-rip-status.md)
-   [選取要進行翻錄的專案](selecting-items-for-ripping.md)

 

 




