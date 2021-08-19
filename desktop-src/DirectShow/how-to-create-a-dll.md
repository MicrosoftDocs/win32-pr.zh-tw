---
description: 如何建立 DirectShow 篩選 DLL
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: 如何建立 DirectShow 篩選 DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443f8aff88cf73198ed7c417da77f6febf33e18806efba5431e18117ddd2c32e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079008"
---
# <a name="how-to-create-a-directshow-filter-dll"></a>如何建立 DirectShow 篩選 DLL

本文說明如何在 Microsoft DirectShow 中將元件實作為動態連結程式庫 (DLL) 。 本文是 [如何執行 iunknown](how-to-implement-iunknown.md)的接續，其中描述如何藉由從 [**CUnknown**](cunknown.md)基類衍生您的元件來執行 **iunknown** 介面。

本文包含下列各節。

-   [Class factory 和 Factory 範本](class-factories-and-factory-templates.md)
-   [Factory 範本陣列](factory-template-array.md)
-   [DLL 函數](dll-functions.md)

註冊 DirectShow 篩選 (，而不是泛型 COM 物件) 需要本文未涵蓋的一些額外步驟。 如需註冊篩選準則的詳細資訊，請參閱[如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 和 COM](directshow-and-com.md)
</dt> </dl>

 

 



