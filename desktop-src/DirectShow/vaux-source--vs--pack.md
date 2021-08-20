---
description: VAUX 來源 (VS) 套件
ms.assetid: 5ffd2883-0e56-459f-b229-cc014b894237
title: VAUX 來源 (VS) 套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477e7a3257c11d6d8b42e16d2f066251452bc42a489abe9e666e374a565fa77c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072094"
---
# <a name="vaux-source-vs-pack"></a>VAUX 來源 (VS) 套件

下表列出 MSDV 驅動程式用來填入 [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo)結構之 **dwDVVAuxSrc** 成員的值。 如需詳細資訊，請參閱[MSDV 驅動程式中的 DVINFO 欄位設定](dvinfo-field-settings-in-the-msdv-driver.md)。

**DVCR 設定**



DV 標準

DVCR (IEC 61834) 

FOURCC

dvsl

dvsd

系統

525-60

625-50

525-60

625-50

電視頻道 (8) 

1111:1111

1111:1111

1111:1111

1111:1111

B/W (1) 

1

1

1

1

EN (1) 

1

1

1

1

CLF (2) 

11

11

11

11

電視頻道 (4) 

1111

1111

1111

1111

來源程式碼 (2) 

11

11

11

11

50/60 (1) 

0

1

0

1

STYPE (5) 

0:0001

0:0001

0:0000

0:0000

調諧器類別 (8) 

1111:1111

1111:1111

1111:1111

1111:1111

VS Pack

0xFFC1FFFF

0xFFE1FFFF

0xFFC0FFFF

0xFFE0FFFF



 

**DVCPRO 25 與 DVCPRO 50 設定 (規劃的)**



DV 標準

DVCPRO (SMPTE 314M) -已規劃

FOURCC

dv25

dv50

系統

525-60

625-50

525-60

625-50

保留 (8) 

1111:1111

1111:1111

1111:1111

1111:1111

B/W (1) 

1

1

1

1

EN (1) 

1

1

1

1

CLF (2) 

11

11

11

11

保留 (4) 

1111

1111

1111

1111

保留 (2) 

11

11

11

11

50/60 (1) 

0

1

0

1

STYPE (5) 

0:0000

0:0000

0:0100

0:0100

VISC (8) 

1111:1111

1111:1111

1111:1111

1111:1111

VS Pack

0x7FC0FFFF

0x7FE0FFFF

0x7FC4FFFF

0x7FE4FFFF



 

**DVCR 100 設定 (規劃的)**



DV 標準

DVCPRO 100-已規劃

FOURCC

dvh1

系統

1080-60i

720-60p

1080-50i

保留 (8) 

1111:1111

1111:1111

1111:1111

B/W (1) 

1

1

1

EN (1) 

1

1

1

CLF (2) 

11

11

11

保留 (4) 

1111

1111

1111

保留 (2) 

11

11

11

50/60 (1) 

0

0

1

STYPE (5) 

1:0100

1:1000

1:0100

VISC (8) 

1111:1111

1111:1111

1111:1111

VS Pack

0x7FD4FFFF

0x7FD8FFFF

0x7FF4FFFF



 

## <a name="remarks"></a>備註

以下是您感興趣的欄位代碼：

-   **B/W**：黑色和白色旗標。 1 = 色彩。
-   **50/60**：欄位數目。
    -   0 = 60 欄位
    -   1 = 50 欄位
-   **STYPE**：信號類型。

    IEC 61834 定義：

    -   0:0000 = 525-60 或625-50，dvsd
    -   0:0001 = 525-60 或625-50，dvsl (如 IEC 61883-5) 中所定義

    SMPTE 314M 定義：

    -   0:0000 = 4:1:1 壓縮
    -   0:0100 = 4:2:2 壓縮

    SMPTE 370 定義：

    -   1:0100 = 1080/60i (60 Hz) 或 1080/50i (50 Hz) 
    -   1:1000 = 720/60p

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> <dt>

[MSDV 驅動程式中的 DVINFO 欄位設定](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



