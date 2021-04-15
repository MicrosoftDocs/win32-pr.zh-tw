---
title: 元件類別管理員
description: 元件類別管理員
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462196"
---
# <a name="the-component-categories-manager"></a>元件類別管理員

為了協助處理元件類別以及保證登錄的一致性，系統會提供元件類別目錄管理員，也就是具有 CLSID StdComponentCategoriesMgr CLSID 的 COM 物件 \_ 。 這個 COM 物件提供下列介面：

-   [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)

[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) 會提供方法，以取得特定類別所執行之類別的相關資訊，並提供在指定電腦上註冊之類別的相關資訊。

[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) 提供在登錄中註冊和取消註冊元件類別目錄資訊的方法。 這包括人類看得懂的類別名稱，以及指定元件或類別所執行或所需的類別。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將圖示與類別產生關聯](associating-icons-with-a-category.md)
</dt> <dt>

[依元件功能分類](categorizing-by-component-capabilities.md)
</dt> <dt>

[依容器功能分類](categorizing-by-container-capabilities.md)
</dt> <dt>

[預設類別和關聯](default-classes-and-associations.md)
</dt> <dt>

[定義元件類別](defining-component-categories.md)
</dt> </dl>

 

 




