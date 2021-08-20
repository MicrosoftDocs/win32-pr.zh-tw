---
description: 以下是編譯各種 TAPI 3 應用程式所需的 .lib 檔案清單，1/22/01。
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: 需要的程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8337042681d84b5f93d5d0218cff18c4bef9259543f60fd13f692ebe5611835
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621358"
---
# <a name="libraries-required"></a>需要的程式庫

編譯各種 TAPI 3 應用程式所需的 .lib 檔案清單，1/22/01：

-   Advapi32.dll .lib
-   Amstrmid .lib (ActiveMovie Guid) 
-   Kernel32.lib
-   Mdhcpid .lib (多播 Guid) 
-   Ole32.lib .lib (COM) 
-   Oleaut32.lib .lib (COM Automation) 
-   Rendid .lib (會合 Guid) 
-   Rpcndr .lib
-   Rpcns4 .lib
-   Rpcrt4 .lib
-   Sdpblbid .lib (會話描述項通訊協定 (SDP) Guid) 
-   Strmiids .lib
-   User32
-   Uuid
-   Wldap32.dll .lib
-   Ws2 \_ 32 .lib

如果您使用 Microsoft Visual Studio，可能需要更新您的版本。 尤其是 Link.exe 必須執行3/19/98 或更新版本的日期。

編譯器定義必須包含 \_ \_ 至少設定為0x500 和 win32 DCOM 的 win32 WINNT \_ \_ 。

 

 



