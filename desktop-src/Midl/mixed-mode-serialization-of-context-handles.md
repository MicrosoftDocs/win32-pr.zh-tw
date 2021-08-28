---
title: 內容控制碼的混合模式序列化
description: 在 Microsoft Windows XP 中，單一介面可以容納序列化和非序列化的內容控制碼，也就是所謂的混合模式序列化。
ms.assetid: b52c1d6f-cdc5-4597-a36e-bb957e4aab01
keywords:
- MIDL 語言參考 MIDL，內容控制碼的混合模式序列化
- 內容控制碼 MIDL
- 混合模式序列化 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aaa35f02a939a50e2484ace29630783ee219d6313d7538cba54b1f54cd83007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787428"
---
# <a name="mixed-mode-serialization-of-context-handles"></a>內容控制碼的混合模式序列化

從 Windows XP 開始，單一介面可以容納序列化和非序列化的內容控制碼，在介面上啟用一種方法，以獨佔方式 (序列化) 來存取內容控制碼，而其他方法則會在共用模式中存取該內容控制碼 (非序列化) 。 如需內容控制碼的詳細資訊，請參閱下列屬性：

-   [**內容 \_ 控制碼**](context-handle.md)
-   [**內容 \_ 控制碼 \_ 序列化**](context-handle-serialize.md)
-   [**內容 \_ 控制碼 \_ noserialize**](context-handle-noserialize.md)

序列化和共用模式存取功能相當於讀取/寫入鎖定機制;使用序列化內容控制碼的方法是 (寫入器) 的專屬使用者，而使用非序列化內容控制碼的方法則是 (讀取器) 的共用使用者。 損毀或修改內容控制碼狀態的方法必須序列化。 未修改內容控制碼狀態的方法（例如直接從內容控制碼讀取的方法）可以是非序列化的。 在混合模式中使用內容控制碼，可大幅改善伺服器的擴充性，特別是當多個執行緒同時呼叫相同的內容控制碼時。

RPC 不會在共用模式中使用內容控制碼在方法上強制執行「寫入鎖定」，這表示應用程式必須確保不會修改共用模式內容控制碼。 修改共用模式所使用的內容控制碼可能會導致內容控制碼內容的微妙損毀，而這種情況可能無法進行偵錯工具。

變更內容控制碼的序列化邏輯只會影響伺服器。 此外，變更內容控制碼的序列化邏輯並不會影響電傳格式，因此，對伺服器上序列化邏輯的變更不會影響現有用戶端與伺服器互動的功能。

不建議只使用非序列化的內容控制碼。 使用非序列化控制碼的伺服器應該針對關閉內容控制碼的方法切換至序列化存取。

僅限輸出的內容控制碼 \[ \] 通常會由建立方法使用，且不需要任何序列化。 因此， \[ \] RPC 會忽略套用至僅限輸出內容控制碼（例如 [**內容 \_ 控制碼 \_ 序列化**](context-handle-serialize.md) 或 [**內容 \_ 控制碼 \_ noserialize**](context-handle-noserialize.md)）的任何序列化屬性。

> [!Note]  
> 建立方法會以隱含方式序列化。

 

## <a name="examples"></a>範例

下列兩個範例示範如何啟用內容控制碼的混合模式序列化。

第一個範例顯示如何在 IDL 檔案中執行此動作：

``` syntax
typedef [context_handle] void *TestContextHandleExclusive;
typedef [context_handle] TestContextHandleExclusive TestContextHandleShared;

void
UseShared(...
          [in] TestContextHandleShared *Ctx,
          ...);

void
UseExclusive(...
             [in, out] TestContextHandleExclusive *Ctx,
             ...);
```

第二個範例顯示如何在 ACF 檔中啟用內容控制碼的混合模式序列化：

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**內容 \_ 控制碼**](context-handle.md)
</dt> <dt>

[**內容 \_ 控制碼 \_ 序列化**](context-handle-serialize.md)
</dt> <dt>

[**內容 \_ 控制碼 \_ noserialize**](context-handle-noserialize.md)
</dt> </dl>

 

 




