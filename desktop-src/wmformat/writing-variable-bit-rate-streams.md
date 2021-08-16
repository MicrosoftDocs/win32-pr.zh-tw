---
title: 寫入變數位元速率資料流程
description: 寫入變數位元速率資料流程
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- Advanced Systems Format (ASF) ，撰寫 VBR 資料流程
- ASF (Advanced Systems Format) ，撰寫 VBR 資料流程
- 變數位元速率 (VBR) ，寫入資料流程
- VBR (變數位速率) ，寫入資料流程
- 資料流程，撰寫 VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694774613ada8b4be05eab55be3213898d423d3b6ac4438204d149a0bd606c90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930253"
---
# <a name="writing-variable-bit-rate-streams"></a>寫入變數位元速率資料流程

變數位元速率 (VBR) 資料流程的寫入方式與 (CBR) 資料流程的常數位元速率相同。 唯一的差異在於寫入器和編解碼器內部執行的處理。 不過，以位速率為基礎的 VBR (限制和不受限制的) 都需要在寫入器中進行前置處理。

您應該針對每個資料流程，檢查您對 [**IWMWriter：： WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) 進行第一個呼叫的傳回值。 如果傳回的錯誤碼是 NS \_ E \_ 不正確 \_ NUM \_ pass，則資料流程需要前置處理階段。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用 Two-Pass 編碼**](using-two-pass-encoding.md)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 




