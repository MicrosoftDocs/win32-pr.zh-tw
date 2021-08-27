---
title: Microsoft RPC Binding-Handle 擴充功能
description: IDL 語言的 Microsoft 擴充功能支援多個控制碼參數，這些參數會出現在第一個、最左邊的參數以外的位置。
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c93b68b20628bf6f7f65cee026412846e0b497d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475364"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a>Microsoft RPC Binding-Handle 擴充功能

IDL 語言的 Microsoft 擴充功能支援多個控制碼參數，這些參數會出現在第一個、最左邊的參數以外的位置。 下列步驟描述 MIDL 編譯器在 DCE 相容性模式中解析系結控制碼參數的順序 (/**憑證**) ，以及預設 (Microsoft 延伸的) 模式。

## <a name="dce-compatibility-mode"></a>DCE 相容模式

-   出現在第一個位置的系結控制碼。
-   \[[**內容 \_ 控制碼**](/windows/desktop/Midl/context-handle)參數 [**的最左邊**](/windows/desktop/Midl/in) \] 。
-   \[[**隱含 \_ 控制碼**](/windows/desktop/Midl/implicit-handle) \] 或 \[ [**自動 \_ 控制碼**](/windows/desktop/Midl/auto-handle)所指定的隱含系結控制碼 \] 。
-   如果沒有 ACF 存在，則預設為使用 \[ **auto \_ 控制碼** \] 。

## <a name="default-mode"></a>預設模式

-   最左邊的明確系結控制碼。
-   \[[**隱含 \_ 控制碼**](/windows/desktop/Midl/implicit-handle) \] 或 \[ [**自動 \_ 控制碼**](/windows/desktop/Midl/auto-handle)所指定的隱含系結控制碼 \] 。
-   如果沒有 ACF 存在，則預設為使用 \[ [**auto \_ 控制碼**](/windows/desktop/Midl/auto-handle) \] 。

DCE IDL 編譯器會尋找明確的系結控制碼做為第一個參數。 當第一個參數不是系結控制碼，且指定了一個或多個內容控制碼時，會使用最左邊的內容控制碼作為系結控制碼。 當第一個參數不是控制碼，而且沒有內容控制碼時，程式會使用 ACF 屬性 \[ [**隱含 \_ 控制碼**](/windows/desktop/Midl/implicit-handle) \] 或 \[ [**自動 \_ 控制碼**](/windows/desktop/Midl/auto-handle)來使用隱含系結 \] 。

IDL 的 Microsoft 擴充功能允許系結控制碼位於第一個參數以外的位置。 \[ [](/windows/desktop/Midl/in) \] 明確控制碼參數中最左邊的參數（不論是基本、程式設計人員定義或內容控制碼）是系結控制碼。 如果沒有控制碼參數，程式會使用 ACF 屬性 \[ [**隱含 \_ 控制碼**](/windows/desktop/Midl/implicit-handle) \] 或 \[ [**自動 \_ 控制碼**](/windows/desktop/Midl/auto-handle)來使用隱含系結 \] 。

下列規則適用于 DCE 相容性 (/osf) 模式和預設模式：

-   當沒有 ACF 存在時，會使用自動控制碼系結。
-   明確 \[ [**in**](/windows/desktop/Midl/in) \] 或 \[ **in**， [](/windows/desktop/Midl/out-idl) \] 個別函式的 out 控制碼會優先採用針對介面指定的任何隱含系結。
-   不支援多個 \[ [**in**](/windows/desktop/Midl/in) \] 或 \[ **in**、out \] 基本控制碼。
-   中有多個 \[ [**in**](/windows/desktop/Midl/in) \] 或 \[ **in**， \] 可使用 out 明確的內容控制碼。
-   所有程式設計師定義的控制碼參數（系結控制碼參數除外）都會被視為 transmissible 資料。

下表包含範例，並說明如何在每個編譯器模式中指派系結控制碼。




| 範例 | 描述 | 
|---------|-------------|
| <pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre> | 未指定明確的控制碼。 使用 [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] 或 [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>] 所指定的隱含系結控制碼。 如果沒有 ACF 存在，則會使用自動控制碼。 | 
| <pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,           [in] short s );</code></pre> | 已指定 handle_t 類型的明確控制碼。 參數 <em>H</em> 是程式的系結控制碼。 | 
| <pre class="syntax" data-space="preserve"><code>void proc3([in] short s,           [in] handle_t H );</code></pre> | 第一個參數不是控制碼。 在預設模式中，最左邊的控制碼參數 <em>H</em>為系結控制碼。 在/osf 模式中，會使用隱含系結。 系統會報告錯誤，因為第二個參數應為 transmissible，而且 handle_t 無法傳輸。 | 
| <pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;void proc1([in] short s,           [in] MY_HDL H );</code></pre> | 第一個參數不是控制碼。 在預設模式中，最左邊的控制碼參數 <em>H</em>為系結控制碼。 存根會呼叫使用者提供的常式 MY_HDL_bind 和 MY_HDL_unbind。 在/憑證模式中，會使用隱含系結。 程式設計師定義的控制碼參數 <em>H</em> 會視為 transmissible 資料。 | 
| <pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;void proc1([in] MY_HDL H,            [in] MY_HDL p );</code></pre> | 第一個參數是系結控制碼。 參數 <em>H</em> 是系結控制碼參數。 第二個程式設計師定義的控制碼參數會被視為 transmissible 資料。 | 
| <pre class="syntax" data-space="preserve"><code>Typedef [context_handle] void * CTXT_HDL;void proc1([in] short s,           [in] long l,           [in] CTXT_HDL H ,           [in] char c);</code></pre> | 系結控制碼是一個內容控制碼。 參數 <em>H</em> 是系結控制碼。 | 




 

 

 
