---
description: AAUX 來源 (作為) 套件
ms.assetid: 0e173fe5-0b9d-48e8-bcbd-403614d51558
title: AAUX 來源 (作為) 套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe479a0740da08f42ca5d80e1f0b6f5174f6917b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187552"
---
# <a name="aaux-source-as-pack"></a>AAUX 來源 (作為) 套件

下表列出 MSDV 驅動程式用來填入 [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo)結構之 **dwDVAAuxSrc** 和 **dwDVAAuxSrc1** 成員的值。 如需詳細資訊，請參閱 [MSDV 驅動程式中的 DVINFO 欄位設定](dvinfo-field-settings-in-the-msdv-driver.md)。

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

LF (1) 

1

1

1

1

保留的 (1) 

1

1

1

1

AF 大小 (6) 

00:1111

01:0000

00:1111

01:0000

SM (1) 

0

0

0

0

CHN (2) 

01

01

01

01

PA (1) 

1

1

1

1

音訊模式 (4) 

    Audio Block 1\*

0000

0000

0000

0000

    Audio Block 2\*

0000

0000

1111

1111

保留的 (1) 

1

1

1

1

ML (1) 

1

1

1

1

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

EF (1) 

1

1

1

1

TC (1) 

1

1

1

1

SMP (3) 

010

010

010

010

QU (3) 

001

001

001

001

AS Pack

    Audio Block 1\*

0xD1C130CF

0xD1E130D0

0xD1C030CF

0xD1E030D0

    Audio Block 2\*

0x00000000

0x00000000

0xD1C03FCF

0xD1E03FD0



 

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

LF (1) 

0

0

0

0

保留的 (1) 

1

1

1

1

AF 大小 (6) 

01:0110

01:1000

01:0110

01:1000

保留的 (1) 

0

0

0

0

CHN (2) 

00

00

00

00

保留的 (1) 

1

1

1

1

音訊模式 (4) 

    Audio Block 1\*

0000

0000

0000

0000

    Audio Block 2\*

0001

0001

0001

0001

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

0:0010

0:0010

保留 (2) 

11

11

11

11

SMP (3) 

000

000

000

000

QU (3) 

000

000

000

000

AS Pack

    Audio Block 1\*

0xC0C01056

0xC0E01058

0xC0C21056

0xC0E21058

    Audio Block 2\*

0xC0C01156

0xC0E01158

0xC0C21156

0xC0E21158



 

> [!Note]  
> \*[**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo)結構包含兩個 AAUX，做為音訊區塊1和2的套件。 DV50 有四個音訊區塊;區塊3和4不會在 **DVINFO** 結構中表示。

 

規劃)  (DVCR 100 設定



DV 標準

DVCPRO 100-已規劃

FOURCC

dvh1

系統

1080-60i

720-60p

1080-50i

LF (1) 

0

0

0

保留的 (1) 

1

1

1

AF 大小 (6) 

01:0110

01:0110

01:1000

保留的 (1) 

0

0

0

CHN (2) 

00

00

00

保留的 (1) 

1

1

1

音訊模式 (4) 

    Audio Block 1\*

0000

0000

0000

    Audio Block 2\*

0001

0001

0001

保留 (2) 

11

11

11

50/60 (1) 

0

0

1

STYPE (5) 

0:0011

0:0011

0:0011

保留 (2) 

11

11

11

SMP (3) 

000

000

000

QU (3) 

000

000

000

AS Pack

    Audio Block 1\*

0xC0C31056

0xC0C31056

0xC0D31058

    Audio Block 2\*

0xC0C31156

0xC0C31156

0xC0D31158



 

> [!Note]  
> \* DVCPRO 100 有8個音訊區塊;區塊3到8不會在 [DVINFO](dvinfo-field-settings-in-the-msdv-driver.md) 結構中表示。

 

## <a name="remarks"></a>備註

以下是您感興趣的欄位代碼：

-   LF：鎖定模式旗標。 指出音訊是否已鎖定。
    -   0 = 已鎖定
    -   1 = 已解除鎖定
-   AF 大小：音訊框架大小。 指定每個畫面的音訊樣本數。

    IEC 61834 定義：

    -   00:1111 = 每個畫面的1068個樣本
    -   01:0000 = 每個畫面的1280個樣本

    SMPTE 314M 定義：

    -   01:0110 = 每個畫面的1602個樣本
    -   01:1000 = 每個畫面的1920個樣本

    根據畫面播放速率，框架中確切的樣本數目可能會不同。 例如，NTSC 是每秒30000/1001 個畫面格 (29.97 fps) 。 使用 32-kHz 音訊時，每個畫面有大約1067.73 個音訊樣本。 因此，名義的費率為1068，但實際的數位會因每個畫面格而異。 此外，在已解除鎖定的音訊中，每個畫面的音訊樣本數目，在一段時間內的特定範圍內都有變化。

<!-- -->

-   SM：立體模式。
    -   0 = 身歷聲
    -   1 = Mono
-   CHN：每個音訊區塊的音訊通道數目。
    -   0 = 每個音訊區塊一個通道
    -   1 = 每個音訊區塊的兩個通道
-   音訊模式：指出每個頻道的音訊信號內容。 此欄位的解釋取決於哪些值會放在 SM 和 CHN 欄位中。 以下定義適用于 MSDV 所使用的值;如需詳細資訊，請參閱規格。

    IEC 61834 定義：

    -   0000 = Ch a/c/e/g 是左方頻道，Ch b/d/f/h 是右聲道
    -   1111 = 沒有音訊資料

    SMPTE 314M 定義：

    -   0000 = CH1 (CH3) 
    -   0001 = CH2 (CH4) 

-   50/60：欄位數目。
    -   0 = 60 欄位
    -   1 = 50 欄位
-   STYPE：系統類型。

    IEC 61834 定義：

    -   00000 = 525-60 或625-50，dvsd
    -   00001 = 525-60 或625-50，dvsl (參閱 IEC 61883-5) 

    SMPTE 314M/SPMTE 370 定義：

    -   00000 = 每個影片畫面的2個音訊區塊
    -   00010 = 每個影片畫面的4個音訊區塊
    -   00011 = 每個影片畫面的8個音訊區塊

-   SMP：取樣頻率。
    -   000 = 48 kHz
    -   010 = 32 kHz
-   QU：量化。
    -   0 = 16 位線性
    -   1 = 12 個位非線性

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> <dt>

[MSDV 驅動程式中的 DVINFO 欄位設定](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



