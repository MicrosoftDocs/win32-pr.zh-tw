---
description: Windows 網路功能 \_ 會在成功時傳回 WN 成功，如果函式遇到錯誤，則會傳回唯一的非零值。 此外，它們還會使用 WNetSetLastError 和 SetLastError 傳回擴充的錯誤資訊。
ms.assetid: cb9d29a1-b3a5-4440-a069-3cd1565b1699
title: 傳回值給 MPR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c96a5636f57d5c926af4e43e676f0b6db75d164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944135"
---
# <a name="returning-values-to-the-mpr"></a>傳回值給 MPR

Windows 網路功能 \_ 會在成功時傳回 WN 成功，如果函式遇到錯誤，則會傳回唯一的非零值。 此外，它們還會使用 [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) 和 [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror)傳回擴充的錯誤資訊。

為了支援上述行為，網路提供者函式不應該在傳回之前呼叫 [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) 。 這是因為 MPR 傳回之後，會在網路提供者 API 中呼叫函式的 **SetLastError** 。 如果網路提供者直接呼叫 **SetLastError** ，則會進行重複的函式呼叫。 網路提供者函式應該只傳回錯誤碼。 錯誤碼是在函數描述或傳回 [值](network-security-return-values.md)中指定。 此外，網路提供者函式可能會傳回任何 [系統錯誤代碼](../debug/system-error-codes.md)，例如記憶體不足。 唯一的例外是 [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps)，它應該會傳回遮罩，指出網路提供者所支援的函式。

如果網路提供者函式需要傳回擴充的錯誤資訊，則應該呼叫 [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora)。 這項功能是由 Windows 作業系統提供，供網路提供者使用。 當提供者呼叫 **WNetSetLastError** 時，可以設定字串，其中包含有關錯誤的其他資訊。 這項資訊是以每個執行緒為基礎來儲存。 這類似于 [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) Windows 應用程式。 Windows 作業系統會呼叫 **WNetSetLastError** 來檢查使用 **WNetSetLastError** 儲存的字串，如果找到的話，會將擴充的錯誤資訊傳回給起始網路要求的呼叫應用程式。

> [!Note]  
> [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora)的 WNet 前置詞會誤導，因為此 API 與 **WNetSetLastError** 不同，它不是 Windows 網路功能 API 集的一部分。 **WNetSetLastError** 僅供網路提供者使用。 名稱 **WNetSetLastError** 會保留，以提供與現有提供者的相容性。

 

 

 
