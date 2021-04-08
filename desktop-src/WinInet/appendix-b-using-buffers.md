---
title: 使用字串緩衝區
description: 傳回字串的函式包含輸入參數、lpszBuffer 和大小參數 lpdwBufferLength。 雖然 lpszBuffer 可以是 Null，但 lpdwBufferLength 必須是 DWORD 變數的有效指標。
ms.assetid: ae7f84ba-15d4-483b-bdda-0042854f9e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309d887458521b99069b381f8bf6650ebeda488a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682723"
---
# <a name="using-string-buffers"></a>使用字串緩衝區

傳回字串的函式包含輸入參數、 *lpszBuffer* 和大小參數 *lpdwBufferLength*。 雖然 *lpszBuffer* 可以是 **Null**，但 *lpdwBufferLength* 必須是 **DWORD** 變數的有效指標。 如果 *lpszBuffer* 所指向的輸入緩衝區為 **Null** 或太小，無法容納輸出字串，則函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 **錯誤的 \_ \_ 緩衝區不足**。 *LpdwBufferLength* 所指向的變數包含一個數位，表示函式傳回要求的字串所需的位元組數目，包括 **null** 結束字元。 應用程式應配置此大小的緩衝區，將 *lpdwBufferLength* 所指向的變數設定為此值，然後重新提交要求。 如果緩衝區大小足以接收要求的字串，則會將字串複製到具有 **null** 結束字元的輸出緩衝區，而函數會傳回成功指示。 *LpdwBufferLength* 所指向的變數現在包含儲存在緩衝區中的字元數，但不包括 **null** 結束字元。

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 