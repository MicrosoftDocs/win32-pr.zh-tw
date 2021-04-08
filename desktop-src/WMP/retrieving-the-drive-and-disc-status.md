---
title: 正在抓取磁片磁碟機和光碟狀態
description: 正在抓取磁片磁碟機和光碟狀態
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Windows Media Player、CD 燒錄
- Windows Media Player 物件模型，CD 燒錄
- 物件模型，CD 燒錄
- Windows Media Player ActiveX 控制項、CD 燒錄
- ActiveX 控制項，CD 燒錄
- Windows Media Player 的行動 ActiveX 控制項、CD 燒錄
- Windows Media Player Mobile、CD 燒錄
- CD 燒錄、取出磁片磁碟機和光碟狀態
- 燒錄 Cd、取出磁片磁碟機和光碟狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eab66581c336f642fd53b22f81949847d0a1c89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841911"
---
# <a name="retrieving-the-drive-and-disc-status"></a>正在抓取磁片磁碟機和光碟狀態

開始 CD 燒錄操作之前，您必須確定所選的 CD-ROM 光碟機支援您要執行的作業。 比方說，您必須先檢查 CD 是否能夠在呼叫 [IWMPCdromBurn：： erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase)之前被清除。 下列程式碼顯示使用 [IWMPCdromBurn：： isAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) 來判斷是否支援作業的範例：


```C++
VARIANT_BOOL vbResult;
    
// Check whether this drive can burn CDs.
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("Burn");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->isAvailable(bstrItem, &vbResult);
}
if (SUCCEEDED(hr))
{
    if (VARIANT_TRUE == vbResult)
    {
        // The current drive can burn CDs.
    }
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**燒錄 CD**](burning-a-cd.md)
</dt> <dt>

[**擷取 CD 燒錄介面**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**啟動燒錄流程**](starting-the-burn-process.md)
</dt> <dt>

[**清除可讀寫 CD**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**正在取出燒錄狀態**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




