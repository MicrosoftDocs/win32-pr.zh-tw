---
title: 多媒體檔案 i/o 參考
description: 多媒體檔案 i/o 參考
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows 多媒體，檔案 i/o 參考
- 多媒體、檔案 i/o 參考
- 多媒體輸入，file i/o 參考
- 多媒體檔案 i/o，參考
- 檔案 i/o，參考
- 輸入和輸出 (i/o) ，參考
- I/o (輸入和輸出) ，參考
- 多媒體檔案 i/o 參考，關於
- 多媒體檔案 i/o 參考，關於
- 檔案 i/o 參考，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06d61b06c16b12a9276adc0d858a3170dae2f7d636cc63a9ac6cc032a65c978c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136899"
---
# <a name="multimedia-file-io-reference"></a>多媒體檔案 i/o 參考

本節說明與多媒體檔案輸入和輸出相關聯的函式、宏、訊息和結構。 這些元素的分組方式如下。

## <a name="basic-io"></a>基本 i/o

-   [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a>緩衝的 I/O

-   [**mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [**mmioFlush**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))
-   [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a>RIFF I/O

-   [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a>自訂 i/o 程式

-   [**IOProc**](/previous-versions//dd757098(v=vs.85))
-   [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [**MMIOM \_ 關閉**](mmiom-close.md)
-   [**MMIOM \_ 開啟**](mmiom-open.md)
-   [**MMIOM \_ 讀取**](mmiom-read.md)
-   [**MMIOM \_ 重新命名**](mmiom-rename.md)
-   [**MMIOM \_ 搜尋**](mmiom-seek.md)
-   [**MMIOM \_ 寫入**](mmiom-write.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)
-   [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[多媒體檔案 i/o](multimedia-file-i-o.md)
</dt> </dl>

 

 