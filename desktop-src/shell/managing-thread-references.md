---
description: 本文包含使用 Shell 輕量公用程式函式的函式管理執行緒參考的相關資訊。
ms.assetid: d8d479fd-c45a-4dfa-b496-76abc7c09a42
title: 管理執行緒參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b629cd97c99e3b30e66810b5f54720d0dbb1c87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973368"
---
# <a name="managing-thread-references"></a>管理執行緒參考

本文包含使用 Shell 輕量公用程式函式的函式管理執行緒參考的相關資訊。


當父執行緒必須在子執行緒的存留期保持作用中時，就會發生這種情況。 比方說，如果元件物件模型 (COM) 物件是在父執行緒上建立並封送處理至子執行緒，則該父執行緒無法在子執行緒之前終止。 為了達成此目的，Shell 會提供這些函數。

-   [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)
-   [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref)
-   [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref)

在您的父執行緒中使用這些函數，如下所述。

1.  在 [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) 函式的形式之後，宣告應用程式定義的執行緒程式。

    ``` syntax
    DWORD WINAPI ThreadProc(LPVOID lpParameter);
    ```

2.  在您的 [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))中，呼叫 [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) 以建立執行緒的參考。 這會提供 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)實例的指標。 此 **IUnknown** 會使用 *pcRef* 所指向的值來維護參考計數。 只要這個計數大於0，執行緒就會維持使用中狀態。
3.  使用該指標指向 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)，在您的 [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))中呼叫 [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref) 。 這會設定參考，讓後續的 [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) 呼叫有一些要抓取的部分。
4.  如果您 [*的 ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))建立另一個執行緒，該執行緒的 *ThreadProc* 可以使用 [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)所取得的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)指標來呼叫 [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) 。 這會遞增 **SHCreateThreadRef** 中 *pcRef* 參數所指向的參考計數。
5.  建立執行緒。 這通常是透過呼叫 [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread)來完成，將指標傳遞至 *pfnThreadProc* 參數中的 [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) 。 也請 \_ \_ 在 *dwFlags* 參數中傳遞 CTF 執行緒 REF 旗標。 只要 *ThreadProc* 正在執行，執行緒就會處於作用中狀態。
6.  建立子執行緒時，請在對其 [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread)的呼叫中，傳遞 *dwFlags* 參數中的 **CTF \_ REF \_ 計數** 旗標。
7.  當子執行緒完成並釋放時，父執行緒的 *pcRef* 所指向的值會減少。 所有子執行緒都完成後，原始 [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) 就可以完成並釋放最後一個執行緒參考，將參考計數卸載至0。 屆時， [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) 所開啟之原始執行緒的參考會釋出，並完成執行緒。

另一個相關函數為 [**SHReleaseThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreleasethreadref)。 如果已使用 [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread)搭配 **CTF \_ 執行緒 \_ REF** 旗標建立執行緒， [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))就會呼叫這個函式。 不過， *ThreadProc* 並不是隱含的必要動作。 在指向透過 [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)取得之 [**iunknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)的指標上呼叫 [**iunknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ，全都是需要完成的。

 

 
