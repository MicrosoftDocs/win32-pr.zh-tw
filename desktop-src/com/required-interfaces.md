---
title: 'COM (所需的介面) '
description: 必要的介面
ms.assetid: ae238882-d0c9-4120-b8a8-001bf9559cfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df483f8c8aa5eb5ecb6799b834fccab42f42ca1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106969745"
---
# <a name="required-interfaces-com"></a>COM (所需的介面) 

下表列出 ActiveX 控制項容器介面，並表示哪些介面是選擇性的，哪些是必要的，而且必須由控制項容器來執行。



| 介面                                                                      | 必要？      | 註解                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/>                            | Yes<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                  | No<br/>  | 只有當容器需要 () 資料變更通知 (以 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)) 的控制項時， (b) 視圖變更通知 (不在使用中、具有 [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) 或 [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)) 的控制項，以及 (c) 作為標準内嵌物件之控制項的其他通知。<br/> |
| [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/>                          | Yes<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**>iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)<br/>                          | Yes<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/>                        | Yes<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer)<br/>                              | Yes<br/> | 請參閱附注1<br/>                                                                                                                                                                                                                                                                                                                                        |
| **IDispatch** 的環境屬性<br/>                                | Yes<br/> | 請參閱附注2和 [控制項的環境屬性](ambient-properties-for-controls.md)<br/>                                                                                                                                                                                                                                                             |
| 控制事件集<br/>                                                  | Yes<br/> | 請參閱附註 2<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)<br/>                        | No<br/>  | [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) 和支援嵌套的簡單框架是選擇性的。<br/>                                                                                                                                                                                                                                                    |
| [IPropertyNotifySink](data-binding-through-ipropertynotifysink.md)<br/> | No<br/>  | 只有 () 的容器具有自己的屬性編輯 UI，而每當控制項變更屬性本身或 (b) 想要控制 \[ [**requestedit**](/windows/desktop/Midl/requestedit) \] 屬性變更和其他這類資料系結功能時，才需要進行更新。<br/>                                                                            |
| [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>       | Yes<br/> | 如果容器支援雙重介面，則為必要。 請參閱附注2。<br/>                                                                                                                                                                                                                                                                                      |
| [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)<br/>                            | No<br/>  | 強烈建議您提供支援。<br/>                                                                                                                                                                                                                                                                                                                  |



 

1.  [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer) 會在檔或表單物件 (，或保存容器網站的適當類比) 上執行。 控制項使用 **IOleContainer** 流覽至相同檔或表單中的其他控制項。
2.  雙介面的支援並非強制性的，但強烈建議使用。 撰寫 ActiveX 控制項容器以利用雙介面，可透過提供雙重介面支援的控制項，提供更好的效能。

ActiveX 控制項容器必須支援 OLE Automation 例外狀況。 如果控制項容器支援雙重介面，則必須透過 [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)來捕捉自動化例外狀況。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[容器](containers.md)
</dt> </dl>

 

