---
title: 安裝自訂 i/o 程式
description: 安裝自訂 i/o 程式
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- 多媒體檔案 i/o，自訂程式
- 檔案 i/o，自訂程式
- 輸入和輸出 (i/o) ，自訂程式
- I/o (輸入和輸出) ，自訂程式
- 安裝自訂 i/o 程式
- 自訂 i/o
- mmioInstallIOProc 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ec92542efe80c24e1e620983d78b4b9a6c246ff003934a1ace1cae159fbd1da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140460"
---
# <a name="installing-custom-io-procedures"></a>安裝自訂 i/o 程式

若要安裝與相關聯的 i/o 程式。ARC 副檔名，請使用 [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) 函數，如下所示：


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



當您使用 [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)安裝 i/o 程式時，程式會保持安裝，直到您將它移除為止。 只要檔案具有適當的副檔名，i/o 程式就會用於您開啟的任何檔案。

您也可以使用 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) 函數，暫時安裝 i/o 程式。 在此情況下，i/o 程式只適用于使用 **mmioOpen** 開啟的檔案，而且會在使用 [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) 函數關閉檔案時移除。 當您使用 **mmioOpen** 開啟檔案時，若要指定 i/o 程式，請使用 *Lpmmioinfo* 參數參考 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) 結構，如下所示：

1.  將 **fccIOProc** 成員設定為 **Null**。
2.  將 **pIOProc** 成員設定為 i/o 程式的程式實例位址。
3.  除非您要開啟記憶體檔案，或直接讀取或寫入檔案 i/o 緩衝區) ，否則請將所有其他成員設定為零 (。

在結束您的應用程式之前，請務必移除您已安裝的所有 i/o 程式。

 

 