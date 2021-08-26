---
title: 新增 Visual Basic Project 的參考
description: 新增 Visual Basic Project 的參考
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deba6030e57839e0f436239790aaa6f02e2fb29981ce021b0de2d09af2acdff6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097068"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a>新增 Visual Basic Project 的參考

下列程式描述如何將 COM 物件的參考加入至 Visual Basic 專案。 然後，您的應用程式可以使用該物件的類別。

當您加入物件做為參考時，您只能使用控制項所提供的類型程式庫，或使用「原始」類型程式庫。 相反地，將控制項加入為元件也會公開 Visual Basic 的擴充項屬性和方法，如同它們是控制項的一部分一樣。

**若要建立元件的 Visual Basic 參考**

1.  從 [專案] 功能表中，按一下 [參考]。
2.  按一下以選取您要新增之元件旁的核取方塊。 如果未列出元件，請使用 **[流覽]** 找出 .dll 或 .ocx 檔案。
3.  按一下 [確定]。

元件現在是專案的一部分。 您的應用程式可以使用 **New** 關鍵字來建立類別實例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將元件新增至 Visual Basic Project](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[翻譯為 Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




