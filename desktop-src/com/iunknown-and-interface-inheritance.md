---
title: IUnknown 和介面繼承
description: IUnknown 和介面繼承
ms.assetid: c45f0947-6020-4aa1-9250-561603a46a68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce4d9d164607745b78001bb92b7dc5331296abe
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966272"
---
# <a name="iunknown-and-interface-inheritance"></a>IUnknown 和介面繼承

COM 中的繼承不表示程式碼重複使用。 因為沒有任何與介面相關聯的執行，所以介面繼承不表示程式碼繼承。 這表示，只有與介面相關聯的合約會以 c + + 純虛擬基類方式繼承，並修改（藉由加入新的方法或進一步限定允許的方法使用方式）。 COM 中沒有選擇性繼承。 如果某個介面繼承自另一個介面，則會包含其他介面所定義的所有方法。

預先定義的 COM 介面會謹慎使用繼承。 所有預先定義的介面 (以及您定義的任何自訂介面) 都會從重要的介面 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)繼承其定義，其中包含三個重要的方法： [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))、 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)。 所有 COM 物件都必須執行 **IUnknown** 介面，因為它提供了使用 **QueryInterface** 的方法，可在物件支援的不同介面之間自由移動，以及使用 **AddRef** 和 **Release** 來管理其存留期的方法。

在建立支援 [匯總](aggregation.md)的物件時，您必須為所有介面和獨立 **IUnknown** 介面各執行一組 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)函數。 在任何情況下，任何物件實作項都會執行 **IUnknown** 方法。 如需詳細資訊，請參閱 [使用和執行 IUnknown](using-and-implementing-iunknown.md) 一節。

雖然有一些介面除了 [**iunknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)之外還會從第二個介面繼承其定義，但大部分只會繼承 **iunknown** 介面方法。 這使得大部分的介面相對較簡潔，而且容易封裝。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 物件和介面](com-objects-and-interfaces.md)
</dt> </dl>

 

 