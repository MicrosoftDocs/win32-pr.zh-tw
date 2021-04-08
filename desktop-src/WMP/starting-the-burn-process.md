---
title: 啟動燒錄流程
description: 啟動燒錄流程
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Windows Media Player、CD 燒錄
- Windows Media Player 物件模型，CD 燒錄
- 物件模型，CD 燒錄
- Windows Media Player ActiveX 控制項、CD 燒錄
- ActiveX 控制項，CD 燒錄
- Windows Media Player 的行動 ActiveX 控制項、CD 燒錄
- Windows Media Player Mobile、CD 燒錄
- CD 燒錄，開始進行燒錄流程
- 燒錄 Cd，開始進行燒錄流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a35f473eebe35bffd48ac802dcfe79082689de
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932944"
---
# <a name="starting-the-burn-process"></a>啟動燒錄流程

開始燒錄之前，您必須指派要燒錄的播放清單。 使用 [IWMPCdromBurn：:p \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) ] 來指定燒錄播放清單。


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



如需使用播放清單的詳細資訊，請參閱 [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)。

若要開始燒錄作業，請呼叫 [IWMPCdromBurn：： startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn)。


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



您可以藉由呼叫 [IWMPCdromBurn：： stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn)來停止燒錄操作。


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**燒錄 CD**](burning-a-cd.md)
</dt> <dt>

[**擷取 CD 燒錄介面**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**清除可讀寫 CD**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**正在抓取磁片磁碟機和光碟狀態**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**正在取出燒錄狀態**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




