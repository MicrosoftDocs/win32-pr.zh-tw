---
description: 若要在處理許多符號檔時節省時間和記憶體，請使用 SymSetOptions 函式來設定延遲的符號載入 (SYMOPT \_ 延後 \_ 載入) 選項。
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: 延遲的符號載入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8682de9ac8eaea78e037bf85ea8a17cd88e63bb56468ab39df3d1887fcc66801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957147"
---
# <a name="deferred-symbol-loading"></a>延遲的符號載入

若要節省處理許多符號檔時的時間和記憶體，請使用 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) 函式來設定延遲的符號載入 (SYMOPT \_ 延 \_ 後載入) 選項，然後使用 [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) 或 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 函式來載入針對所有模組延後的符號。 符號處理常式會列出可用於模組的符號，但在要求之前，不會將偵錯工具資訊對應到記憶體。 這是有效率地使用偵錯工具符號的慣用方法。 所有使用符號的函式都會受到延遲符號載入的影響。

 

 



