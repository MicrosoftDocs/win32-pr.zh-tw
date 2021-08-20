---
title: 使用伺服器注釋
description: 本主題提供使用伺服器批註來指定回呼物件的相關資訊。
ms.assetid: eeeebddc-2752-4d8f-b4fa-38ce156acc08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b2955d49431b502c8587484208321bc1ab1bc0c8201fabf466b60b68f548a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823902"
---
# <a name="using-server-annotation"></a>使用伺服器注釋

本主題提供使用伺服器批註來指定回呼物件的相關資訊。

**覆寫指定回呼物件的屬性**

1.  取得要加上批註之可存取元素的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標。
2.  在可存取的專案上呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，以取得 [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) 介面指標。
3.  在 [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity)介面指標上呼叫 [**IAccIdentity：： GetIdentityString ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccidentity-getidentitystring) ，以取得可唯一識別要標注之可存取專案的字串。
4.  使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 或 [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) 來建立 [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) 物件。
5.  建立元件物件模型 (COM) 物件，該物件會執行 [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)。
6.  呼叫 [**IAccPropServices：： SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)，傳遞識別字串、指出要覆寫之屬性的 GUID，以及 [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) 回呼物件的指標。
7.  發行介面指標和可用記憶體。

當用戶端要求可存取專案的屬性時，將會呼叫回呼物件，並將值傳回給用戶端。

當指定值時，伺服器開發人員也可以使用 [**IAccPropServices：： ComposeHwndIdentityString**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-composehwndidentitystring) 方法來取得識別字串;或者，他們可以使用 [**IAccPropServices：： SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) 方法，並指定 *hwnd*、 *idObject* 或 *idChild* 參數，而非識別字串。

在容器物件上使用 [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver) 或 [**SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) 時，伺服器開發人員可以選擇性地指定覆寫資訊也應套用至該容器的所有元素子系。

伺服器可以使用 [**IAccPropServices：： ClearProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearprops)，隨時明確清除註釋。 這通常不是必要的，因為批註服務會在批註的可存取專案消失時，自動清除和釋放批註資訊。

以下是可使用此程式標注的屬性清單。

## <a name="properties-supported-when-specifying-a-callback"></a>指定回呼時支援的屬性

指定回呼時，可以標注下列屬性。 這些屬性目前無法藉由指定值來直接批註。



| 屬性                      | 類型                                                             |
|-------------------------------|------------------------------------------------------------------|
| PROPID \_ ACC \_ 名稱             | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ 描述      | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ 角色             | VT \_ I4                                                           |
| PROPID \_ ACC \_ 狀態            | VT \_ I4                                                           |
| PROPID \_ ACC \_ 說明             | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ KEYBOARDSHORTCUT | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR                                                         |
| PROPID \_ ACC 的 \_ VALUEMAP         | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ ROLEMAP          | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ STATEMAP         | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ 焦點            | VT \_ 分派<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ 選取專案        | VT \_ 分派<br/> VT \_ I4<br/> VT \_ 不明<br/> |
| PROPID \_ ACC \_ 父系           | VT \_ 分派                                                     |
| PROPID \_ ACC \_ NAV \_          | VT \_ 分派<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_        | VT \_ 分派<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ 左方        | VT \_ 分派<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ 右移       | VT \_ 分派<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ 上一頁        | VT \_ 分派<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ 下一頁        | VT \_ 分派<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ FIRSTCHILD  | VT \_ 分派<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ LASTCHILD   | VT \_ 分派<br/> VT \_ I4<br/>                        |



 

 

