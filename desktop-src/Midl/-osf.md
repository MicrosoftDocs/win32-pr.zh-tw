---
title: /osf 參數
description: /Osf 交換器會強制與憑證 DCE 具有嚴格的相容性。
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- /osf 參數 MIDL
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb887997642b0d0ff81314d6cf81dc148e57547727a09b1fe646f04d0391f967
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014116"
---
# <a name="osf-switch"></a>/osf 參數

**/Osf** 交換器會強制與憑證 DCE 具有嚴格的相容性。

``` syntax
midl /osf
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

如果您的應用程式需要與憑證 DCE 的嚴格相容性，以提供可攜性的原因。

在 **/osf** 模式中，當您使用完整指標、引數需要記憶體配置，或當您使用 [ [**啟用 \_ 配置**](enable-allocate.md) ] 屬性時，便會自動啟用 RpcSs 套件。 這表示您不需要在用戶端和伺服器應用程式中提供 [**midl \_ 使用者 \_ 配置**](/windows/desktop/Rpc/the-midl-user-allocate-function) 和 [**midl \_ 使用者 \_ 免費**](/windows/desktop/Rpc/the-midl-user-free-function) 函數。

當您使用 **/osf** 參數進行編譯時，無法使用下列 Microsoft 擴充功能：

-   在 IDL 檔案中)  (未具名引數的抽象宣告子。
-   COM 物件的介面定義。
-   具有超過17個字元的介面名稱。
-   僅限 MIDL 屬性（例如， [**電傳 \_ 封送**](wire-marshal.md)處理、 [**使用者 \_ 封送**](user-marshal.md)處理和 typelib） (ODL) 擴充功能。
-   在 IDL 檔案中使用 ACF 關鍵字 (MIDL **/app \_ config** 選項) 。
-   用戶端上的靜態回呼函數。
-   [**Async**](async.md)屬性。
-   [**.cpp \_ 引號**](cpp-quote.md)和 **\# pragma midl \_ echo**。
-   [**wchar \_ t**](wchar-t.md) 寬字元類型、常數和字串。
-   [**列舉**](enum.md) 初始化 (稀疏列舉值) 。
-   僅限 [**輸出**](out-idl.md)大小的規格。
-   混合大小的指標和大小的陣列。
-   用於大小和鑒別子規范的運算式。
-   引數清單中任何位置的明確控制碼參數。 在 **/osf** 模式中，MIDL 編譯器會尋找明確的系結控制碼做為第一個參數。 當第一個參數不是系結控制碼，且指定了一個或多個內容控制碼時，會使用最左邊的內容控制碼作為系結控制碼。 當第一個參數不是控制碼，而且沒有內容控制碼時，程式會使用 ACF 屬性 [**隱含 \_ 控制碼**](implicit-handle.md) 或 [**自動 \_ 控制碼**](auto-handle.md)來使用隱含系結。
-   指標屬性型別繼承。 憑證 DCE 不允許未歸屬指標。 因此，在 **/osf** 模式中，每個 IDL 檔案都必須定義其指標的屬性。 如果有任何指標沒有明確的屬性，則 IDL 檔案必須具有 [**指標 \_ 預設**](pointer-default.md) 規格，才能設定指標類型。
-   IDL 檔案中的多個介面。
-   介面區塊外部的定義。
-   類型限定詞，例如 **遠** 和 **stdcall**。
-   省略方向屬性。

當您使用 **/osf** 參數編譯時，無法使用下列 C/c + + 語言延伸模組：

-   結構和等位中的位欄位。
-   以兩個斜線字元分隔的單行批註 (//) 。
-   外部宣告。
-   參數清單中有省略號的程式。
-   輸入 [**int**](int.md)。
-   輸入 **void \** _ (，但 [_ *內容 \_ 控制碼* *](context-handle.md)屬性) 除外。
-   類型限定詞，包括具有 ANSI 一致前置詞的表單，其中包含兩個底線字元： **\_ \_ cdecl**、 **cdecl**、 [**const**](const.md)、 **const**、 **\_ \_ export**、 **export**、 **\_ \_ far**、 **far**、 **\_ \_ loadds**、 **loadds**、 **\_ \_ near**、 **near**、 **\_ \_ pascal**、 **pascal**、 **\_ \_ stdcall**、 **stdcall**、 **\_ \_ volatile** 和 **volatile**。
-   任何 \# [**pragma**](pragma.md)警告或 **\# pragma** 批註。
-   類型序列化。
-   [**\_ \_ Int3264**](--int3264.md)資料類型。
-   [**/Protocol**](-protocol.md)參數和 ndr64 傳輸語法。

## <a name="examples"></a>範例

**midl/osf 檔案名 .idl**

**midl/osf/app \_ config 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/app \_ 設定**](-app-config.md)
</dt> <dt>

[**/ms \_ ext**](-ms-ext.md)
</dt> <dt>

[Rpcss 記憶體管理套件](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 