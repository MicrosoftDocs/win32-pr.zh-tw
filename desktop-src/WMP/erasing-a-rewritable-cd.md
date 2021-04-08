---
title: 清除可讀寫 CD
description: 清除可讀寫 CD
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Windows Media Player、CD 燒錄
- Windows Media Player 物件模型，CD 燒錄
- 物件模型，CD 燒錄
- Windows Media Player ActiveX 控制項、CD 燒錄
- ActiveX 控制項，CD 燒錄
- Windows Media Player 的行動 ActiveX 控制項、CD 燒錄
- Windows Media Player Mobile、CD 燒錄
- CD 燒錄，抹除可讀寫 Cd
- 燒錄 Cd，抹除可讀寫 Cd
- 清除可讀寫 Cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023042"
---
# <a name="erasing-a-rewritable-cd"></a>清除可讀寫 CD

[IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)介面提供清除 cd-rw 光碟的方法。 清除 CD 之前，您必須先確定已支援此作業。 如需詳細資訊，請參閱 [取出磁片磁碟機和光碟狀態](retrieving-the-drive-and-disc-status.md)。

若要開始清除可讀寫 CD 的內容，請呼叫 [IWMPCdromBurn：： erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase)。


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**燒錄 CD**](burning-a-cd.md)
</dt> <dt>

[**擷取 CD 燒錄介面**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**啟動燒錄流程**](starting-the-burn-process.md)
</dt> <dt>

[**正在抓取磁片磁碟機和光碟狀態**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**正在取出燒錄狀態**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




