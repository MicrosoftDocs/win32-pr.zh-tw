---
description: 下列函式搭配輸出保護管理員使用 (OPM) 。
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: OPM 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b4ef210ace3f7f179b59980cedb962a5bee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980735"
---
# <a name="opm-functions"></a>OPM 函式

下列函式搭配 [輸出保護管理員](output-protection-manager.md) 使用 (OPM) 。



| 函式                                                                                             | 描述                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**OPMGetVideoOutputForTarget**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | 傳回指定介面卡上之 VidPN 目標的影片輸出物件。                                                          |
| [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | 針對每個與特定 **HMONITOR** 控制碼相關聯的實體監視器，建立輸出保護管理員 (OPM) 物件。 |
| [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | 為每個與特定 Direct3D 裝置相關聯的實體監視器建立 OPM 物件。                                 |



 

OPM 會使用下列功能來存取顯示驅動程式中的功能。 應用程式不應呼叫這些函式。

-   [**ConfigureOPMProtectedOutput**](configureopmprotectedoutput.md)
-   [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)
-   [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md)
-   [**GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [**GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [**GetCOPPCompatibleOPMInformation**](getcoppcompatibleopminformation.md)
-   [**GetOPMInformation**](getopminformation.md)
-   [**GetOPMRandomNumber**](getopmrandomnumber.md)
-   [**GetSuggestedOPMProtectedOutputArraySize**](getsuggestedopmprotectedoutputarraysize.md)
-   [**SetOPMSigningKeyAndSequenceNumbers**](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[OPM 程式設計參考](opm-programming-reference.md)
</dt> <dt>

[輸出保護管理員](output-protection-manager.md)
</dt> </dl>

 

 



