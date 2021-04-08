---
title: ADSI 錯誤碼
description: 所有 ADSI 錯誤碼都會以 COM HRESULT 值的形式傳回。
ms.assetid: 573889e4-37af-4aca-afd7-ef06bcf8aa0d
ms.tgt_platform: multiple
keywords:
- ADSI ADSI、參考、錯誤碼
- 錯誤碼 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d9383998429b2ec64dd16fbed0d0df314f0d72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839247"
---
# <a name="adsi-error-codes"></a>ADSI 錯誤碼

所有 ADSI 錯誤碼都會以 COM **HRESULT** 值的形式傳回。 它們可以分組為下列四種類型：

-   [一般 COM 錯誤碼](generic-com-error-codes.md)
-   [一般 ADSI 錯誤碼](generic-adsi-error-codes.md)
-   [ADSI 的 Win32 錯誤碼](win32-error-codes-for-adsi.md)
-   [ADSI 的 LDAP 錯誤碼](ldap-error-codes-for-adsi.md)

此外，某些介面會提供其他錯誤資訊，稱為 ADSI 擴充的錯誤訊息，可使用 [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) 函式取得。

最後，本節所示的 c + + [範例程式碼](code-example-for-working-with-adsi-error-messages.md) 會示範如何工作 ADSI 錯誤訊息。

 

 




