---
title: 如何處理 WM_GETOBJECT
description: 當它收到 \_ 包含 OBJID 用戶端的 WM GETOBJECT 訊息時 \_ ，伺服器必須將指標傳回至執行 IAccessible 的物件。
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674011"
---
# <a name="how-to-handle-wm_getobject"></a>如何處理 WM \_ GETOBJECT

當它收到包含 [**OBJID \_ 用戶端**](object-identifiers.md)的 [**WM \_ GETOBJECT**](wm-getobject.md)訊息時，伺服器必須將指標傳回至執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)的物件。 此指標是透過呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)取得的 LRESULT。 Microsoft Active Accessibility，結合元件物件模型 (COM) 程式庫時，會執行適當的封送處理，並將 **IAccessible** 介面指標從伺服器傳遞至用戶端。

伺服器必須正確處理可存取物件上的參考計數。 請記住，當您建立 COM 物件時，參考計數為1。 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 之後，會進一步遞增參考計數數次。 當不再需要物件時，會自動釋放 **LresultFromObject** 所建立的所有參考，但是伺服器會負責釋出初始參考，除非它這麼做，否則物件永遠不會被終結。 下列各節中的範例示範如何釋放可存取物件的參考。

伺服器通常會以下列其中一種方式處理 [**WM \_ GETOBJECT**](wm-getobject.md) ：

-   [建立新的可存取物件](create-new-accessible-objects.md)
-   [重複使用物件的現有指標](reuse-existing-pointers-to-objects.md)
-   [建立相同物件的新介面](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> 在本節的其餘部分中，討論到 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的指標時，此指標實際上可能是包裝 **IAccessible** 介面之 proxy 物件的指標。 如需 proxy 物件的詳細資訊，請參閱 [建立 Proxy 物件](creating-proxy-objects.md)。

 

如需有關 [**wm \_ getobject**](wm-getobject.md)的總覽，請參閱 [Wm getobject 的 \_ 運作方式](how-wm-getobject-works.md)。

 

 




