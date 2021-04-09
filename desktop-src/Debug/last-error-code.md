---
description: 發生錯誤時，大部分的系統函數都會傳回錯誤碼，通常是0、Null 或 &\# 8211; 1。
ms.assetid: fd5b0d6e-78cf-4f51-b61d-d32576cd485a
title: Last-Error 程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bf0fe2f544fc3d87690be81b0d09767745ef95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936129"
---
# <a name="last-error-code"></a>Last-Error 程式碼

發生錯誤時，大部分的系統函數都會傳回錯誤碼，通常是0、 **Null** 或–1。 許多系統函數也會設定一個額外的錯誤碼，稱為 *最後一個錯誤碼*。 每個執行中的執行緒都會個別維護此錯誤碼;某個執行緒中的錯誤不會覆寫另一個執行緒中的最後一個錯誤碼。 任何函式都可以呼叫 [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) 或 [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex) 函數來設定目前線程的最後錯誤碼。 這些函式主要適用于動態連結程式庫 (DLL) ，因此可以將資訊提供給呼叫端應用程式。 請注意，有些函式會在成功時呼叫 **SetLastError** 或 **SetLastErrorEx** ，但會抹除最近失敗的函式所設定的錯誤碼，而其他函式則不會。

應用程式可以使用 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式取出最後一個錯誤碼;錯誤碼可能會告訴更多實際發生的情況，讓函數失敗。 系統函式的檔將會指出函式設定最後一個錯誤碼所用的條件。

系統會定義一組可設為最後錯誤碼或由這些函式傳回的錯誤碼。 錯誤碼為32位值 (位31是) 最重要的位。 Bit 29 保留給應用程式定義的錯誤碼;未設定此位的系統錯誤碼。 如果您定義應用程式的錯誤碼，請設定此位以指出錯誤碼已由應用程式定義，並確保錯誤碼不會與任何系統定義的錯誤碼衝突。 如需詳細資訊，請參閱 Winerror.h .h 和 [系統錯誤碼](system-error-codes.md)。

 

 
