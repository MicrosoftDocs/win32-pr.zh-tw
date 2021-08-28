---
title: 擷取轉錄介面
description: 擷取轉錄介面
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Windows Media Player、CD 翻錄
- Windows Media Player 物件模型，CD 翻錄
- 物件模型、CD 翻錄
- Windows Media Player ActiveX 控制項、CD 翻錄
- ActiveX 控制項，CD 翻錄
- Windows Media PlayerMobile ActiveX control、CD 翻錄
- Windows Media Player行動電話、CD 翻錄
- CD 翻錄，IWMPCdromRip 介面
- 將 Cd、IWMPCdromRip 介面翻錄
- IWMPCdromRip 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2179e4f38eee121d7b8fefc028adf232eb724264362396c8cacedfcc55b162d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002548"
---
# <a name="retrieving-the-ripping-interface"></a>擷取轉錄介面

若要列舉使用者電腦上的 CD 磁片磁碟機，請使用 **IWMPCdromCollection** 介面。 呼叫 [IWMPCore：： get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)，以抓取這個介面的指標。

藉由使用 [get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) 和 [item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) 方法，您可以逐一查看集合，以取得使用者電腦上每個 CD 光碟機的 [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) 介面。

**IWMPCdrom** 介面代表個別的 CD 光碟機。 開始將 CD 翻錄之前，您必須先透過 **IWMPCdrom** 指標呼叫 **QueryInterface** ，以取出 [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)介面。

下列程式碼範例示範如何取出介面，以從特定磁片磁碟機翻錄 CD：


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    HRESULT hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromRipInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromRip interface.
        m_spCdromRip.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromRip);
    }

    return hr;
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將 CD 翻錄**](ripping-a-cd.md)
</dt> <dt>

[**啟動 Rip 進程**](starting-the-rip-process.md)
</dt> <dt>

[**正在抓取 Rip 狀態**](retrieving-the-rip-status.md)
</dt> <dt>

[**選取要進行翻錄的專案**](selecting-items-for-ripping.md)
</dt> <dt>

[**IWMPCdromCollection 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




