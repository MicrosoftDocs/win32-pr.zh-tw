---
title: Errors
description: 本節將概述在執行命令失敗時，Windows Web 服務功能可能會發生的錯誤。
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Windows 的錯誤 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70f10d673bf8f37664d792d8cf969f0329dc363
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839583"
---
# <a name="errors"></a>Errors

本節將概述在執行命令失敗時，Windows Web 服務功能可能會發生的錯誤。

-   [Out 參數](#out-parameters)
-   [錯誤碼](#error-codes)
-   [豐富的錯誤](#rich-errors)
-   [錯誤和錯誤](#faults-and-errors)
-   [語言敏感性錯誤資訊](#language-sensitive-error-information)
-   [標準錯誤碼](#canonical-error-codes)
-   [API 使用方式無效](#invalid-api-usage)
-   [安全性](#security)

## <a name="out-parameters"></a>Out 參數

一般來說，如果函式失敗，就不會修改 out 參數的值。

如果函式失敗，則會有一些會修改 out 參數的實例。 這些案例會在每個參數的檔中明確地呼叫。 如果檔未提及在失敗情況下修改 out 參數的任何專案，則您可以安全地假設函式不會修改它們。

## <a name="error-codes"></a>錯誤碼

所有錯誤傳回碼都是 Hresult。 此 API 會在設備 WEBSERVICES 範圍中定義一組 Hresult \_ ，但也會傳回 WINDOWS API 中其他位置所定義的錯誤。

請參閱特定 API 的檔，以瞭解傳回的錯誤碼。 此清單並非針對每個 API 提供詳盡的清單，而是一份錯誤碼清單，其中包含明確處理的常見案例。 呼叫端應該一律假設任何 API 都有其他錯誤碼。

此 API 會定義相對較少的錯誤碼，這會對應至程式會想要根據錯誤採取動作的案例。 單獨使用錯誤碼可能不足以判斷發生錯誤的原因，或為了提供問題給使用者的良好描述。 最瞭解問題的原因是使用豐富的錯誤，如下所述。

## <a name="rich-errors"></a>豐富的錯誤

若要傳回錯誤碼，呼叫者可以選擇性地傳遞非 **Null** 的 [WS \_ error](ws-error.md)物件，要求任何 API 呼叫的豐富錯誤資訊。 若要建立錯誤物件，請使用 [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror)。 如果發生錯誤，則造成錯誤的 API 將會在錯誤物件中填入有關錯誤狀況的其他內容。 如果沒有發生錯誤，則錯誤物件是未修改的。 傳遞 **Null** 錯誤物件表示呼叫端對豐富的錯誤資訊不感興趣。 被呼叫端 (包括回呼) 必須準備處理 **Null** 錯誤物件。

請注意，相同的錯誤物件可以用於多個 API 呼叫，但是一次只能用於一個 API 呼叫 (因為它是單一執行緒) 。 每次發生錯誤時，就會將錯誤資訊附加至 error 物件。 當呼叫鏈回溯時，多個函式可能會將資訊新增至 error 物件，以提供有關錯誤的其他內容。 若要在重複使用之前清除 error 物件的內容 () 發生錯誤時，請使用 [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror)。 如果未發生任何錯誤，在重複使用之前，不需要重設錯誤物件。

豐富的錯誤資訊包含下列各項：

-   一組屬性值，提供錯誤的其他相關資訊（如果有的話）。 請參閱 [**WS \_ ERROR \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)。
-   零或多個錯誤字串。 您可以使用 [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)來新增字串，並且可以使用 [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring)來查詢。 您可以使用 [**WS \_ ERROR \_ PROPERTY \_ STRING \_ COUNT**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)來查詢字串的數目。

## <a name="faults-and-errors"></a>錯誤和錯誤

如需有關錯誤和錯誤如何相關的詳細資訊，請參閱 [錯誤](faults.md) 。

## <a name="language-sensitive-error-information"></a>語言敏感性錯誤資訊

建立錯誤物件時，會指定所需語言翻譯的 LANGID，以取得錯誤資訊。 這是在將錯誤資訊加入錯誤物件時使用。

您可以使用 [**WS \_ ERROR \_ 屬性 \_ LANGID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)來抓取或設定此語言值。

## <a name="canonical-error-codes"></a>標準錯誤碼

此 API 提供一組標準的錯誤碼 (WS \_ E \_ \*) ，可讓您使用不同的通訊技術，而不需要依賴特定基礎執行的特定錯誤碼。 如需這些錯誤碼的完整清單，請參閱 [Windows Web 服務傳回值](windows-web-services-return-values.md)。

例如，這可讓程式檢查是否有使用 TCP、UDP 或 HTTP 的錯誤代碼 **WS \_ E \_ 端點 \_ \_** ，並採取一些動作 (例如嘗試使用不同的端點) 。

當執行特定錯誤碼對應至標準錯誤時，原始錯誤碼會儲存在錯誤物件中，而且可能仍可供診斷之用。 如需詳細資訊，請參閱 [**WS \_ error \_ 屬性 \_ 原始 \_ 錯誤碼 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) 。

## <a name="invalid-api-usage"></a>API 使用方式無效

下列錯誤碼保留給不正確 API 使用，在其他情況下則不會傳回。 如果傳回任何錯誤，則可能是應用程式錯誤的指示。

-   **WS \_ E \_ 不正確作業 \_**
-   **E \_ INVALIDARG**

下列列舉是追蹤的一部分：

-   [**WS \_ ERROR \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**WS \_ 例外狀況 \_ 代碼**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

下列錯誤碼屬於追蹤的一部分：

-   **CERT \_ E \_ CN \_ 沒有 \_ 相符**
-   **CERT \_ E 已 \_ 過期**
-   **CERT \_ E \_ UNTRUSTEDROOT**
-   **CERT \_ E \_ 錯誤的 \_ 使用方式**
-   **\_離線 CRYPT 電子 \_ 撤銷 \_**
-   **E \_ INVALIDARG**
-   **E \_ OUTOFMEMORY**
-   **\_ \_ \_ 使用中的 WS E 位址 \_**
-   **WS \_ E \_ 位址 \_ 無法 \_ 使用**
-   **WS \_ E \_ ENDPOINT \_ \_ 拒絕存取**
-   **\_ \_ \_ \_ 不支援 WS E 端點 \_ 動作**
-   **WS \_ E \_ 端點已 \_ 中斷連線**
-   **WS \_ E \_ 端點 \_ 失敗**
-   **\_已收到 WS E \_ 端點 \_ 錯誤 \_**
-   **WS \_ E \_ 端點 \_ 無法 \_ 使用**
-   **\_ \_ \_ \_ 找不到 WS E 端點**
-   **WS \_ E \_ 端點 \_ 太 \_ 忙碌**
-   **無法連線到 WS \_ E \_ 端點 \_**
-   **WS \_ E \_ 不正確 \_ 端點 \_ URL**
-   **WS \_ E \_ 不正確 \_ 格式**
-   **WS \_ E \_ 不正確作業 \_**
-   **\_ \_ 不支援 WS \_ E**
-   **WS \_ E \_ 沒有 \_ 翻譯 \_ 可用**
-   **WS \_ E \_ 數值 \_ 溢位**
-   **WS \_ E \_ 物件發生錯誤 \_**
-   **已 \_ 放棄 WS E \_ 操作 \_**
-   **WS \_ E 作業已 \_ \_ 中止**
-   **WS \_ E \_ 作業 \_ 超時 \_**
-   **WS \_ E \_ OTHER**
-   **\_拒絕 WS E \_ PROXY \_ 存取 \_**
-   **WS \_ E \_ PROXY \_ 失敗**
-   **WS \_ E \_ PROXY \_ 需要 \_ 基本 \_ 身份驗證**
-   **WS \_ E \_ PROXY \_ 需要 \_ 摘要式 \_ 驗證**
-   **WS \_ E \_ PROXY \_ 需要 \_ 協商 \_ 驗證**
-   **WS \_ E \_ PROXY \_ 需要 \_ NTLM \_ 驗證**
-   **\_超過 WS E \_ 配額 \_**
-   **WS \_ E \_ 安全性 \_ 系統 \_ 失敗**
-   **WS \_ E \_ 安全性 \_ 權杖已 \_ 過期**
-   **WS \_ E \_ 安全性 \_ 驗證 \_ 失敗**
-   **WS \_ E \_ SERVER \_ 需要 \_ 基本 \_ 身份驗證**
-   **WS \_ E \_ SERVER \_ 需要 \_ 摘要式 \_ 驗證**
-   **WS \_ E \_ SERVER \_ 需要 \_ 協商 \_ 驗證**
-   **WS \_ E \_ SERVER \_ 需要 \_ NTLM \_ 驗證**
-   **WS \_ S \_ 非同步**
-   **WS \_ S \_ END**

下列函數是追蹤的一部分：

-   [**WS \_ ERROR \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**WS \_ 例外狀況 \_ 代碼**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

下列控制碼是追蹤的一部分：

-   [WS \_ 錯誤](ws-error.md)

下列結構是追蹤的一部分：

-   [**WS \_ ERROR \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a>安全性

錯誤物件的使用者應該注意的一些安全性考慮如下：

-   錯誤物件可能包含不受信任的資料。 這兩個範例包括： WS \_ 錯誤和錯誤字串，兩者都可以根據未受信任通道所收到的資訊儲存在錯誤物件中。 當您檢查 error 物件中的資訊，並根據其值做出決策時，錯誤物件的使用者應該要小心。
-   錯誤物件的使用者應該在檢查有關錯誤的資訊之後，呼叫 [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) 。 如果無法這麼做，可能會導致記憶體累積。
-   使用 \_ ws 錯誤洩漏列舉的 ws 完整錯誤洩漏值時，錯誤物件的使用者應該非常小心 \_ \_ ，因為產生的錯誤可能包含在錯誤記錄過程中累積的私用資訊。 [**\_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure)

 

 




