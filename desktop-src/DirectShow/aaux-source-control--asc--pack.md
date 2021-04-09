---
description: AAUX 原始檔控制 (ASC) 套件
ms.assetid: 3df80895-81e1-42a4-a095-913e77b199e5
title: AAUX 原始檔控制 (ASC) 套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab942ccff1cf38e6962d508c9c9bfc99ea9fed6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688268"
---
# <a name="aaux-source-control-asc-pack"></a>AAUX 原始檔控制 (ASC) 套件

下表列出 MSDV 驅動程式用來填入 **dwDVAAuxCtl** 的值，以及

**DwDVAAuxCtl1** [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) 結構的成員。 如需詳細資訊，請參閱 [MSDV 驅動程式中的 DVINFO 欄位設定](dvinfo-field-settings-in-the-msdv-driver.md)。

DVCR 設定



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

CGMS (2) 

00

00

00

00

ISR (2) 

11

11

11

11

CMP (2) 

11

11

11

11

SS (2) 

11

11

11

11

REC ST (1) 

1

1

1

1

REC 結束 (1) 

1

1

1

1

REC 模式 (3) 

001

001

001

001

插入 CH (3) 

111

111

111

111

DRF (1) 

1

1

1

1

加速 (7) 

010:0000

010:0000

010:0000

010:0000

保留的 (1) 

1

1

1

1

類型 (7) 

111:1111

111:1111

111:1111

111:1111

 (兩個音訊區塊的 ASC 套件) \*

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F



 

DVCR 25 與 DVCPRO 50 設定 (計畫的) 



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

CGMS (2) 

00

00

00

00

保留 (4) 

1111

1111

1111

1111

EFC (2) 

00

00

00

00

REC ST (1) 

1

1

1

1

REC 結束 (1) 

1

1

1

1

淡化 ST (1) 

1

1

1

1

淡化 END (1) 

1

1

1

1

保留 (4) 

1111

1111

1111

1111

DRF (1) 

1

1

1

1

加速 (7) 

111:1000

110:0100

111:1000

110:0100

保留 (8) 

1111:1111

1111:1111

1111:1111

1111:1111

 (兩個音訊區塊的 ASC 套件) \*

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F



 

\**DVINFO* 結構包含兩個 AAUX，做為音訊區塊1和2的套件。 DV50 有四個音訊區塊;區塊3和4不會在 *DVINFO* 結構中表示。

規劃)  (DVCR 100 設定



DV 標準

DVCPRO 100-已規劃

FOURCC

dvh1

系統

1080-60i

720-60p

1080-50i

CGMS (2) 

00

00

00

保留 (4) 

1111

1111

1111

EFC (2) 

00

00

00

REC ST (1) 

1

1

1

REC 結束 (1) 

1

1

1

淡化 ST (1) 

1

1

1

淡化 END (1) 

1

1

1

保留 (4) 

1111

1111

1111

DRF (1) 

1

1

1

加速 (7) 

111:1000

111:1000

110:0100

保留 (8) 

1111:1111

1111:1111

1111:1111

 (兩個音訊區塊的 ASC 套件) \*

0xFFF8FF3C

0xFFF8FF3C

0xFFE4FF3C



 

\* DVCPRO 100 有8個音訊區塊;區塊3到8不會在 *DVINFO* 結構中表示。

## <a name="remarks"></a>備註

以下是您感興趣的欄位代碼：

-   **CGMS**：複製世代管理系統。 0 = 允許複製而不受限制。

    DV 串流中的實際 ASC 套件可能包含不同的值。

<!-- -->

-   **REC 模式**：錄製模式。 1 = 原始
-   **速度**： VTR 播放速度。

    IEC 61834 定義：

    -   010:0000 = 一般速度、525-60 或625-50

    SMPTE 314M 定義：

    -   111:1000 = 一般速度、525-60
    -   110:0100 = 一般速度、625-50

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> <dt>

[MSDV 驅動程式中的 DVINFO 欄位設定](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



