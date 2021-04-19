---
description: WinHTTP 中的錯誤處理
ms.assetid: 96bceda2-ca96-4f88-ab38-35021889c2dd
title: WinHTTP 中的錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf234220d0973e86c830063e4ecc25312fa2d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979966"
---
# <a name="error-handling-in-winhttp"></a>WinHTTP 中的錯誤處理

並非所有的 WinHTTP API 函數都會以相同的方式報告錯誤。

某些函式（例如 [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)）會傳回 **布林** 值，指出在 **FALSE** 時失敗。 如果傳回 **FALSE** ，則對錯誤感興趣的呼叫端應該呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。 如果 **在** 函式成功 (傳回的值為 **FALSE**) ，則傳回的值會無法預期，而且可能會在 Windows 版本、Service pack 之間，甚至在相同函式的呼叫之間變更。

某些函式（例如 [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)）會傳回 [HINTERNET](hinternet-handles-in-winhttp.md) 虛擬控制碼。 這些函式完全相同，但失敗是藉由傳回 **Null** 來表示。 如果傳回 **Null** ，則對錯誤感興趣的呼叫端應該呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。 如果 **在** 函式成功 (傳回的任何值都是 **Null**) ，則傳回的值會無法預期，而且可能會在 Windows 版本、Service pack 之間，甚至在相同函式的呼叫之間變更。

某些函式（例如 [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)）會傳回 **DWORD** 錯誤碼，而且不需要呼叫任何其他函式來取得更多錯誤資訊。 針對這些函式，不應呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 。 如果呼叫 **GetLastError** （不論函式成功或失敗），則傳回的值會無法預期，而且可能會在 Windows 版本、Service pack 之間，甚至在相同函式的呼叫之間變更。

 

 
