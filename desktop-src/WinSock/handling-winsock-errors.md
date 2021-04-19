---
description: Winsock 中的錯誤處理。
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: 處理 Winsock 錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbad01ad7add7995cf978e101535104f6dc0da6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973269"
---
# <a name="handling-winsock-errors"></a>處理 Winsock 錯誤

大部分的 Windows 通訊端2函式在函式傳回時，不會傳回錯誤的特定原因。 如果成功，部分 Winsock 函數會傳回零的值。 否則，會傳回值通訊端 \_ 錯誤 (-1) ，而且可以藉由呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 函式來取出特定的錯誤號碼。 針對傳回控制碼的 Winsock 函式，無效通訊端的傳回值 \_ (0xffff) 表示錯誤，而且可以藉由呼叫 **WSAGetLastError** 來抓取特定的錯誤號碼。 針對傳回指標的 Winsock 函式，傳回值為 **Null** 表示錯誤，而且可以藉由呼叫 **WSAGetLastError** 函數來抓取特定的錯誤號碼。

您可以將 Winsock 錯誤碼轉換成 HRESULT，以便在遠端程序呼叫中使用， (RPC) 使用 WIN32 的 HRESULT \_ \_ 。 在舊版平臺軟體發展工具組 (SDK) 中， \_ 從 \_ WIN32 定義為 WINERROR.H 的 HRESULT 已定義為 *.h* 標頭檔中的宏。 在 Microsoft Windows 軟體開發套件 (SDK) 中， \_ 來自 WIN32 的 HRESULT \_ 會定義為 *winerror.h .h* 標頭檔中的內嵌函式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 通訊端錯誤碼](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



