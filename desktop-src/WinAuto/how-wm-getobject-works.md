---
title: WM_GETOBJECT 的運作方式
description: '\_當用戶端呼叫其中一個 AccessibleObjectFromX 函數時，Microsoft Active Accessibility 會將 WM GETOBJECT 訊息傳送至適當的伺服器應用程式。'
ms.assetid: 53f7b3db-97e4-4ff2-9f7a-4555ec7956ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24309b304baede0c7b93c9e609b469991e737ca819e8014effa03a4f39b8772c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795758"
---
# <a name="how-wm_getobject-works"></a>WM \_ GETOBJECT 的運作方式

當用戶端呼叫其中一個 **AccessibleObjectFrom**_X_ 函式時，Microsoft Active Accessibility 會將 [**WM \_ GETOBJECT**](wm-getobject.md)訊息傳送至適當的伺服器應用程式。 下列清單說明發生的各種案例：

-   如果接收 [**WM \_ GETOBJECT**](wm-getobject.md)的視窗或控制項執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)，則視窗會傳回使用 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)的 **IAccessible** 介面參考。 Microsoft Active Accessibility，結合元件物件模型 (COM) 程式庫時，會執行適當的封送處理，並將介面指標從伺服器傳遞回用戶端。
-   如果接收訊息的視窗沒有執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)，它應該會傳回零。
-   如果視窗未處理 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息， [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) 函數會傳回零。

即使伺服器傳回零，Microsoft Active Accessibility 仍會為用戶端提供物件的相關資訊。 針對大部分系統提供的物件（例如清單方塊和按鈕），Microsoft Active Accessibility 提供完整的資訊。對於其他物件，則會限制資訊。 例如，Microsoft Active Accessibility 不會提供沒有視窗控制碼之控制項的資訊。 Microsoft Active Accessibility 會傳回 proxy [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標，用戶端會使用此指標來取得物件的相關資訊。

如需詳細資訊，請參閱 [WM \_ GETOBJECT Message](the-wm-getobject-message.md)。

 

 