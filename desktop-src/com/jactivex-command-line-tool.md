---
title: JActiveX Command-Line 工具
description: JActiveX 命令列應用程式是 Visual j + + 6.0 的元件。
ms.assetid: b356eb85-5dd4-475b-8d53-8c13a84aa976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae611e56c44b78398817cd0c78804d343fa97754f80fb3b036ea2705c801070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992648"
---
# <a name="jactivex-command-line-tool"></a>JActiveX Command-Line 工具

JActiveX 命令列應用程式是 Visual j + + 6.0 的元件。 它會讀取 Microsoft ActiveX 控制項的類型程式庫，並產生對應的 JAVA 原始程式檔。 然後，您可以編譯這些原始程式檔，然後將它們匯入至您的 JAVA 應用程式。

若要產生 COM 物件的 JAVA 來源檔案，請從命令提示字元執行：

**jactivex** *檔案名*

其中 *filename* 是包含類型程式庫之檔案的名稱。 這個檔案可能會有下列任何副檔名： .tlb、. .olb、.ocx、.dll 或 .exe。

如需您可以在 JActiveX 中設定之選擇性參數的詳細資訊，請參閱 Visual c + + 檔，或輸入下列命令列：

**jactivex /?**

> [!WARNING]
> 請勿使用1.02.3920 版之前的 Visual c + + 編譯器來編譯 JActiveX.exe 所產生的檔案。 這是因為產生的原始程式檔必須使用編譯器進行編譯 @com-aware 。 只有版本1.02.3920 之後的 Visual j + + 編譯器才是 @com-aware 。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉換成 JAVA](translating-to-java.md)
</dt> </dl>

 

 




