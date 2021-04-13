---
description: 如何執行 IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: 如何執行 IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509786"
---
# <a name="how-to-implement-iunknown"></a>如何執行 IUnknown

Microsoft DirectShow 是以元件物件模型 (COM) 為基礎。 如果您撰寫自己的篩選準則，則必須將它實作為 COM 物件。 DirectShow 基類提供可從中進行此作業的架構。 不需要使用基類，但可以簡化開發流程。 本文說明 COM 物件的一些內部詳細資料，以及它們在 DirectShow 基類中的實作為。

本文假設您已瞭解如何程式設計 COM 用戶端應用程式（亦即，您瞭解 **IUnknown** 中的方法），但不會假設任何先前的開發 com 物件體驗。 DirectShow 處理許多開發 COM 物件的詳細資料。 如果您有開發 COM 物件的經驗，請參閱 [使用 CUnknown](using-cunknown.md)的章節，其中描述 [**CUnknown**](cunknown.md) 基類。

COM 是一種規格，不是實作為。 它會定義元件必須遵循的規則;讓這些規則生效，讓開發人員得以運用。 在 DirectShow 中，所有物件都衍生自一組 c + + 基類。 基底類別的函式和方法會執行大部分的 COM "簿記" 工作，例如保留一致的參考計數。 藉由從基類衍生您的篩選，您就可以繼承類別的功能。 若要有效地使用基類，您需要先瞭解它們如何實行 COM 規格。

本文包含下列主題。

-   [IUnknown 的運作方式](how-iunknown-works.md)
-   [使用 CUnknown](using-cunknown.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 和 COM](directshow-and-com.md)
</dt> </dl>

 

 



