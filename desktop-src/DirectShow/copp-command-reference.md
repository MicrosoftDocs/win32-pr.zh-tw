---
description: COPP 命令參考
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: COPP 命令參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dfeebe42b877604ab880ef1855035242d6eca8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972323"
---
# <a name="copp-command-reference"></a>COPP 命令參考

本節說明 (COPP) 命令的經認證輸出保護通訊協定。 已定義下列命令。



| 命令              | GUID                             |
|----------------------|----------------------------------|
| 設定保護層級 | **DXVA \_ COPPSetProtectionLevel** |
| 設定信號        | **DXVA \_ COPPSetSignaling**       |



 

設定保護等級命令

設定指定之輸出保護機制的保護層級。 視連接器而定，可能會在相同的連接器上套用一個以上的保護機制，每個機制各有不同的設定。

**GUID**： DXVA \_ COPPSetProtectionLevel

**輸入資料**： [**DXVA \_ COPPSetProtectionLevelCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) 結構。

設定信號命令

指定保護層級以外的視訊訊號相關資訊。

針對 CGMS-A，某些保護標準要求 televsion 信號包含與 CGMS-A 位相同之 VBI 波形封包內的外觀比例和其他資訊的相關資訊。 如果外觀比例資訊與影片串流不一致，則電視可能會顯示不良。 應用程式可以使用此命令來指定外觀比例，讓圖形驅動程式能夠產生正確的 VBI 封包。

如果未來的標準需要額外的信號資訊，則此命令也設計為可延伸。

**GUID**： DXVA \_ COPPSetSignaling

**輸入資料**： [**DXVA \_ COPPSetSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) 結構。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用認證輸出保護通訊協定 (COPP) ](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



