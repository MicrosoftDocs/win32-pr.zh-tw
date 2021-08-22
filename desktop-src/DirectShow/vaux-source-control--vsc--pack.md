---
description: VAUX 原始檔控制 (VSC) 套件
ms.assetid: 9d5dd89e-9084-409d-86c0-30b57645d33d
title: VAUX 原始檔控制 (VSC) 套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcdc91d5c4b2cea460c85b696c59bfce7799d39aed0a6bfcbc03f3d3c522a6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072072"
---
# <a name="vaux-source-control-vsc-pack"></a>VAUX 原始檔控制 (VSC) 套件

下表列出 MSDV 驅動程式用來填入 [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo)結構之 **dwDVVAuxCtl** 成員的值。 如需詳細資訊，請參閱[MSDV 驅動程式中的 DVINFO 欄位設定](dvinfo-field-settings-in-the-msdv-driver.md)。

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

保留的 (1) 

1

1

1

1

REC 模式 (2) 

00

00

00

00

保留的 (1) 

1

1

1

1

 (3) 

000

000

000

000

FF (1) 

1

1

1

1

FS (1) 

1

1

1

1

FC (1) 

1

1

1

1

IL (1) 

1

1

1

1

ST (1) 

1

1

1

1

SC (1) 

1

1

1

1

BCSYS (2) 

00

01

00

01

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

VSC 套件

0xFFFCC83F

0xFFFDC83F

0xFFFCC83F

0xFFFDC83F



 

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

CGMS (2) 

00

00

00

00

保留 (6) 

11:1111

11:1111

11:1111

11:1111

保留 (2) 

11

11

11

11

保留 (2) 

00

00

00

00

保留的 (1) 

1

1

1

1

 (3) 

000

000

000

000

FF (1) 

1

1

1

1

FS (1) 

1

1

1

1

FC (1) 

1

1

1

1

IL (1) 

1

1

1

1

保留 (2) 

11

11

11

11

保留 (2) 

00

00

00

00

保留 (8) 

1111:1111

1111:1111

1111:1111

1111:1111

VSC 套件

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F



 

**DVCPRO 100 設定 (規劃的)**



DV 標準

DVCPRO 100-已規劃

FOURCC

dvh1

系統

1080-60i

720p-60p

1080-50i

CGMS (2) 

00

00

00

保留 (6) 

11:1111

11:1111

11:1111

保留 (2) 

11

11

11

保留 (2) 

00

00

00

保留的 (1) 

1

1

1

 (3) 

010

010

010

FF (1) 

1

1

1

FS (1) 

1

1

1

FC (1) 

1

1

1

IL (1) 

1

1

1

保留 (2) 

11

11

11

保留 (2) 

00

00

00

保留 (8) 

1111:1111

1111:1111

1111:1111

VSC 套件

0xFFFCCA3F

0xFFFCCA3F

0xFFFCCA3F



 

## <a name="remarks"></a>備註

以下是您感興趣的欄位代碼：

-   **CGMS**：複製世代管理系統。 0 = 允許複製而不受限制。

    DV 串流中的實際 VSC 套件可能包含不同的值。

<!-- -->

-   **REC 模式**：錄製模式。 1 = 原始。
-   顯示 **：顯示** 選取模式。 000 = 4:3 外觀比例，完整格式;010 = 16:9 外觀比例。
-   **BCSYS**：廣播系統。 此欄位定義寬螢幕信號資訊的類型。
    -   0 = 類型 0 (請參閱 IEC 61880) 
    -   1 = 類型 1 (請參閱 ETSI EN 300 294) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> <dt>

[MSDV 驅動程式中的 DVINFO 欄位設定](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



