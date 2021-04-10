---
title: 'WM_GETOBJECT 訊息 (Winuser .h) '
description: 由 Microsoft Active Accessibility 和 Microsoft 消費者介面自動化傳送，可取得伺服器應用程式中所包含之可存取物件的相關資訊。
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- WM_GETOBJECT message Windows 協助工具
topic_type:
- apiref
api_name:
- WM_GETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcac5c7f6dd8203c32b9f6f3c4eb59144cc3f8ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106464"
---
# <a name="wm_getobject-message"></a>WM \_ GETOBJECT 訊息

由 Microsoft Active Accessibility 和 Microsoft 消費者介面自動化傳送，可取得伺服器應用程式中所包含之可存取物件的相關資訊。

應用程式永遠不會直接傳送此訊息。 Microsoft Active Accessibility 傳送此訊息以回應 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)、 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)或 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)的呼叫。 不過，伺服器應用程式會處理此訊息。 消費者介面自動化傳送此訊息以回應 [**IUIAutomation：： ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle)、 [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)和 [**system.windows.input.focusmanager.getfocusedelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)的呼叫，以及處理用戶端已註冊的事件時。


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* 
</dt> <dd>

提供訊息的其他相關資訊，而且僅供系統使用。 伺服器會在處理訊息時，將 *dwFlags* 傳遞為 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)呼叫中的 *wParam* 參數。

</dd> <dt>

*dwObjId* 
</dt> <dd>

物件識別碼。 此值是其中一個 [物件識別碼](object-identifiers.md) 常數或自訂物件識別碼。 伺服器應用程式必須檢查此值，以識別所要求的資訊類型。 在比較此值與 OBJID \_ 值之前，伺服器必須將它轉換成 **DWORD**; 否則，在64位的 Windows 上， *lParam* 的正負號延伸可能會干擾比較。

-   如果 *dwObjId* 是其中一個 OBJID \_ 值（例如 [**OBJID \_ 用戶端**](object-identifiers.md)），則要求是針對可執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)的 Microsoft Active Accessibility 物件。
-   如果 *dwObjId* 等於 **UiaRootObjectId**，則要求是針對消費者介面自動化提供者。 如果伺服器正在執行消費者介面自動化，則應該使用 [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) 函式傳回提供者。
-   如果 *dwObjId* 是 [**OBJID \_ NATIVEOM**](object-identifiers.md)，則要求是針對控制項的基礎物件模型。 如果控制項支援此要求，則會呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 函式來傳回適當的 COM 介面。
-   如果 *dwObjId* 是 [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md)，則要求會讓控制項將本身識別為標準的 Windows 控制項，或是通用控制項程式庫 (ComCtrl.dll) 所執行的通用控制項。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果視窗或控制項不需要回應這則訊息，則應該將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式;否則，視窗或控制項應傳回對應至 *dwObjId* 所指定之要求的值：

-   如果視窗或控制項執行消費者介面自動化，則視窗或控制項應該會傳回呼叫 [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) 函式所取得的值。
-   如果 *dwObjId* 是 [**OBJID \_ NATIVEOM**](object-identifiers.md) ，且視窗公開原生物件模型，則 Windows 應該會傳回呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 函數所取得的值。
-   如果 *dwObjId* 是 [**OBJID \_ 用戶端**](object-identifiers.md) 且視窗會執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)，則視窗應該會傳回 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 函式的呼叫所取得的值。

## <a name="remarks"></a>備註

當用戶端呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 或任何其他 **AccessibleObjectFrom**_X_ 函式，以抓取物件的介面時，Microsoft Active Accessibility 會將 **WM \_ GETOBJECT** 訊息傳送至適當的伺服器應用程式中適當的視窗程式。 處理 **WM \_ GETOBJECT** 時，伺服器應用程式會呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) ，並使用此函數的傳回值做為訊息的傳回值。 Microsoft Active Accessibility 與 COM 程式庫搭配使用，會執行適當的封送處理，並將介面指標從伺服器傳遞回用戶端。

在物件完全初始化或開始關閉之前，伺服器不會回應 **WM \_ GETOBJECT** 。 當應用程式建立新的視窗時，系統會傳送 [**事件 \_ 物件 \_ 建立**](event-constants.md) 來通知用戶端，然後再將 [WM \_ 建立](../winmsg/wm-create.md) 訊息傳送至應用程式的視窗程式。 因為許多應用程式都使用 WM \_ create 來啟動其初始化程式，所以在完成處理 **wm \_ 建立** 訊息之前，伺服器不會回應 **wm \_ GETOBJECT** 訊息。

伺服器會使用 **WM \_ GETOBJECT** 來執行下列工作：

-   [建立新的可存取物件](create-new-accessible-objects.md)
-   [重複使用物件的現有指標](reuse-existing-pointers-to-objects.md)
-   [建立相同物件的新介面](create-new-interfaces-to-the-same-object.md)

針對用戶端，這表示它們可能會接收相同使用者介面元素的相異介面指標，視伺服器的動作而定。 為了判斷兩個介面指標是否指向相同的使用者介面元素，用戶端會比較物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性。 比較指標無法運作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 可轉散發套件<br/>          | 使用 SP6 和更新版本和 Windows 95 在 Windows NT 4.0 上 Active Accessibility 1.3 的 RDK<br/>              |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[如何處理 WM \_ GETOBJECT](how-to-handle-wm-getobject.md)
</dt> <dt>

[WM \_ GETOBJECT 的運作方式](how-wm-getobject-works.md)
</dt> <dt>

[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

