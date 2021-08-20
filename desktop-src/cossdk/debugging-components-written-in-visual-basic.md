---
description: 調試 Visual Basic 中撰寫的元件
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: 調試 Visual Basic 中撰寫的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0dc8e4d98a41f0059de8e3eb44deeb9dcd8e4fbfdc6dba0510bd227a189c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991178"
---
# <a name="debugging-components-written-in-visual-basic"></a>調試 Visual Basic 中撰寫的元件

您可以使用 Microsoft Visual Basic 6.0 開發環境，在某些情況下進行偵錯工具。 使用 Visual Basic 進行偵錯工具，可讓您存取 Visual Basic 程式設計人員熟悉的工具。 另一方面，因為在 Visual Basic 環境的程式中執行 Visual Basic 元件的偵錯工具時，您可能需要在使用 Microsoft Visual C++ 開發環境來編譯元件之後，對元件進行 debug。

如需在 Visual Basic 整合式開發環境內進行偵錯工具 (IDE) 的詳細資訊，請參閱[Visual Basic ide 中的調試](debugging-in-the-visual-basic-ide.md)程式。 如需使用 Visual C++ 開發環境來編譯 Visual Basic 元件的詳細資訊，請參閱[Visual Basic 元件的調試](debugging-compiled-visual-basic-components.md)程式。

此外，使用 Visual Basic 環境來對具有 MTS 的元件進行偵錯工具的幾項限制，已針對 com + 進行解析。 如需詳細資訊，請參閱[com + Visual Basic 與 MTS 對比的支援](com--visual-basic-debugging-support-contrasted-with-mts.md)。

> [!Note]  
> 如果您已在與 com + 相同的電腦上使用 Visual Basic，您可能已注意到 Visual Basic 環境中可用的元件服務增益集。 這項功能原本是在 MTS 中，每次您重新編譯 COM + 應用程式中的元件時，都必須更新登錄。 不過，由於 Microsoft Windows 登錄和 com + 註冊資料庫的互動本質，某些設定可能不會完全更新。 因此，您應該在重新編譯之後移除並重新安裝元件，以更新設定，而不是使用此增益集提供的命令。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[調試 Visual C++ 中撰寫的元件](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



