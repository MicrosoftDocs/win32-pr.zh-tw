---
title: 啟動 Rip 進程
description: 啟動 Rip 進程
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Windows Media Player、CD 翻錄
- Windows Media Player 物件模型，CD 翻錄
- 物件模型、CD 翻錄
- Windows Media Player ActiveX 控制項、CD 翻錄
- ActiveX 控制項，CD 翻錄
- Windows Media Player 的行動 ActiveX 控制項、CD 翻錄
- Windows Media Player 行動電話、CD 翻錄
- CD 翻錄，啟動 rip 進程
- 翻錄 Cd，啟動 rip 進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2107b053abf8747d7add8fcedc26a2386ae5fd84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106965415"
---
# <a name="starting-the-rip-process"></a>啟動 Rip 進程

當您依照上一節所述取出翻錄介面之後，請呼叫 [IWMPCdromRip：： startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip)來啟動翻錄程式。


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



您可以藉由呼叫 [IWMPCdromRip：： stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip)來停止翻錄作業。


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將 CD 翻錄**](ripping-a-cd.md)
</dt> <dt>

[**擷取轉錄介面**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**正在抓取 Rip 狀態**](retrieving-the-rip-status.md)
</dt> <dt>

[**選取要進行翻錄的專案**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




