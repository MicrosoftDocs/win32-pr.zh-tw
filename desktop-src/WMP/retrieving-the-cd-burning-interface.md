---
title: 擷取 CD 燒錄介面
description: 擷取 CD 燒錄介面
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Windows Media Player、CD 燒錄
- Windows Media Player 物件模型，CD 燒錄
- 物件模型，CD 燒錄
- Windows Media Player ActiveX 控制項、CD 燒錄
- ActiveX 控制項，CD 燒錄
- Windows Media PlayerMobile ActiveX control、CD 燒錄
- Windows Media Player行動電話、CD 燒錄
- CD 燒錄，正在抓取 IWMPCdromCollection 介面
- 燒錄 Cd，正在抓取 IWMPCdromCollection 介面
- IWMPCdromCollection 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84013d5df4244fc30c9cb52e3447d15f60e559befe1223f0964934dd8ca1e1cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123198"
---
# <a name="retrieving-the-cd-burning-interface"></a>擷取 CD 燒錄介面

若要列舉使用者電腦上的 CD 磁片磁碟機，請使用 **IWMPCdromCollection** 介面。 您可以藉由呼叫 [IWMPCore：： get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)，來取得這個介面的指標。

藉由使用 **get \_ count** 和 **item** 方法，您可以逐一查看集合，以取得使用者電腦上每個 CD 光碟機的 [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) 介面指標。

**IWMPCdrom** 介面代表個別的 CD 光碟機。 開始燒錄 CD 之前，您必須先透過 **IWMPCdrom** 指標呼叫 **QueryInterface** ，以取得 [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)介面的指標。

下列程式碼範例示範如何取出介面，以將 CD 燒錄到特定磁片磁碟機：


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

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
HRESULT CMainDlg::GetCdromBurnInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromBurn interface.
        m_spCdromBurn.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromBurn);
    }

    return hr;
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**燒錄 CD**](burning-a-cd.md)
</dt> <dt>

[**啟動燒錄流程**](starting-the-burn-process.md)
</dt> <dt>

[**清除可讀寫 CD**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**正在抓取磁片磁碟機和光碟狀態**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**正在取出燒錄狀態**](retrieving-the-burn-status.md)
</dt> <dt>

[**IWMPCdromCollection 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




