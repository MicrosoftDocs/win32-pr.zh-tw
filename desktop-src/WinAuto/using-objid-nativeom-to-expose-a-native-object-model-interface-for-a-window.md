---
title: 使用 OBJID \_ NATIVEOM 來公開視窗的原生介面
description: 這項技術可讓用戶端取得視窗的自訂物件。 伺服器可以使用這個來公開視窗之自訂檔物件的指標。
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed99db4641235ceee57688865710c19a41f0a517d70d4601d138150cb88dd470
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098088"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a>使用 OBJID \_ NATIVEOM 來公開視窗的原生介面

這項技術可讓用戶端取得視窗的自訂物件。 伺服器可以使用這個來公開視窗之自訂檔物件的指標。

**若要公開視窗 (伺服器的原生物件模型介面)**

1.  處理視窗程式中的 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息。 當 *lParam* 值為 [**OBJID \_ NATIVEOM**](object-identifiers.md)時，會使用 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)將介面指標傳回給自訂物件。
2.  如有需要，請在呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)之後釋放介面指標。 如需詳細資訊，請參閱 **LresultFromObject**。

用戶端可以取得這個自訂物件的指標。

**若要為視窗 (用戶端取得自訂物件的指標)**

-   呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 並傳遞 [**OBJID \_ NATIVEOM**](object-identifiers.md) 做為第二個參數。

請注意這項技術的下列問題：

-   這項技術類似于傳回 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標，但所使用的物件識別碼不同，而 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 會傳回自訂物件，而不是 **IAccessible**。
-   伺服器開發人員可能需要發佈資訊，讓用戶端能夠唯一識別 **HWND** ，讓它們可以在其視窗控制碼上呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 之前找到。
-   請勿在傳回的自訂物件上，執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。 如果您這樣做，OLEACC 會將它視為標準 **IAccessible** ，而且可能會導致無法使用自訂介面。
-   為了跨進程使用，傳回物件上的介面可能必須向元件物件模型註冊 (COM) 。

許多 Microsoft Office 元件都支援此技術。 如需詳細資訊，請參閱 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)。

 

 




