---
title: 複合檔案介面
description: 複合檔案介面
ms.assetid: 3192ee58-55fd-43cb-b7d5-7270e91b8131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e146bf26ef8d0c5c2fc189255389982a7e737a0556343cb095217c55ff8d712
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410508"
---
# <a name="compound-document-interfaces"></a>複合檔案介面

下表列出 OLE 容器、OLE 伺服器和複合檔案物件所執行的介面。 必要的介面必須在其列出的元件上執行。 所有其他功能都是選擇性的。 但是，如果您想要在應用程式中包含特定功能，則必須在下表中執行該功能所顯示的介面。 只有當您要包含特定功能時，才需要所有其他介面。

下表列出 OLE 容器的必要和選擇性行為，以及您必須為每個容器執行的介面。



| 行為                               | 介面                                                                                                                                                              |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 必要行為<br/>          | [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/> [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                                                       |
| 訊息篩選<br/>           | [**Imessagefilter.prefiltermessage**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)<br/>                                                                                                                     |
| 連結<br/>                     | 無<br/>                                                                                                                                                         |
| 連結至内嵌物件<br/> | [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer)<br/> [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/> [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)<br/>             |
| 就地啟用<br/>         | [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/> [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/> [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> |
| 拖放<br/>               | [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                               |



 

下表列出 OLE 伺服器及其複合檔案物件的必要和選擇性行為，以及您必須為每個物件執行的介面。 表格會區分 OLE 伺服器及其物件，以闡明哪個元件會執行哪些介面。 此表也注明跨進程與同進程伺服器所提供之物件的不同需求。



| 功能                        | OLE 伺服器                                                                                                                                | 物件 (跨進程)                                                                                                                          | 物件 (同進程)                                                                                                                                                                                                                          |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 必要行為             | [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)<br/>                                                                                         | [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/> | [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/> [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)<br/> [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2)<br/> |
| 訊息篩選<br/>   | [**Imessagefilter.prefiltermessage**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)<br/>                                                                                       |                                                                                                                                                 |                                                                                                                                                                                                                                             |
| 連結<br/>             | [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer)<br/> [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                 |                                                                                                                                                 | [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)<br/> [**IExternalConnection**](/windows/win32/api/objidlbase/nn-objidlbase-iexternalconnection)<br/>                                                                                                                                       |
| 就地啟用<br/> |                                                                                                                                           | [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> [**IOleInPlaceActiveObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceactiveobject)<br/>                 | [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> [**IOleInPlaceActiveObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceactiveobject)<br/>                                                                                                             |
| 拖放<br/>       | [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> |                                                                                                                                                 |                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[複合檔案](compound-documents.md)
</dt> </dl>

 

