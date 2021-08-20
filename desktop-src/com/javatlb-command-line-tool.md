---
title: JAVATLB Command-Line 工具
description: JAVATLB Command-Line 工具
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ade0a20a1c41310422c08310f2d0534914993d79909f51990c48aa04df0a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918622"
---
# <a name="javatlb-command-line-tool"></a>JAVATLB Command-Line 工具

JAVATLB 是 Visual j + + 5.0 的元件。 JAVATLB 是一種命令列應用程式，可產生 COM 物件的類別檔案。 包含無法準確且安全地在 JAVA 中表示之資料類型的方法，不會轉換。

與 [JAVA 類型程式庫 Wizard](java-type-library-wizard.md)不同的是，JAVATLB 不會產生包含 JAVA 類型程式庫資訊的摘要檔案。

若要產生單一 COM 物件的 JAVA 類別檔案，請從命令提示字元執行：

**javatlb** *檔案名*

其中 *filename* 是包含類型程式庫之檔案的名稱。 這個檔案可能會有下列任何副檔名： .tlb、. .olb、.ocx、.dll 或 .exe。

若要產生多個 COM 物件的 JAVA 類別檔案，請從命令提示字元執行：

**javatlb @**_TextFile_

其中 *TextFile* 是文字檔的名稱，其中包含包含 COM 物件類型程式庫的檔案清單。

> [!Note]  
> 在 Visual c + + 6.0 中，JAVATLB 命令列工具是由 [JActiveX 工具](jactivex-command-line-tool.md)所取代。 如需詳細資訊，請參閱 Visual c + + 6.0 檔。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉換成 JAVA](translating-to-java.md)
</dt> </dl>

 

 




