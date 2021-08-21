---
title: 持續性
description: 持續性
ms.assetid: 4916ea52-a21c-4938-81cb-392b5ca1f6c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c8600307bfe6c29f72fb9d29e633358062c4e8c1c61da8898173cf190f1d08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500328"
---
# <a name="persistence"></a>持續性

控制項會執行多個持續性介面中的一或多個，以支援其狀態的持續性。 例如， [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) 介面支援以資料流程為基礎的控制項狀態持續性。 **IPersistStreamInit** 是 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) 的取代，並新增 [**InitNew**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-initnew)的初始化方法。 這兩個介面中的其他方法都相同。 **IPersistStreamInit** 並非衍生自 **IPersistStream**;物件只支援兩個介面的其中一個，根據是否需要能夠初始化本身的新實例。

控制項可提供的其他持續性介面包括： [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、 [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))、 [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)、 [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))。 控制項實施者必須決定哪些類型的持續性最重要，並執行適當的持續性介面。 控制項實施者也會決定要儲存的內容。 例如，控制項可以儲存其屬性的目前值，或其在其容器內的位置和大小。 用戶端會決定要使用的介面。

從持續性狀態載入控制項之前，用戶端可以檢查 OLEMISC \_ SETCLIENTSITEFIRST 旗標，以判斷控制項是否支援在載入其持續狀態之前取得其用戶端網站和環境屬性。 這項優化可以節省具現化控制項的時間，因為控制項接著可以自由忽略其持續性值，而不是只載入它們，讓用戶端所提供的環境屬性覆寫這些值。

控制項也可以支援在 OLE 屬性集中儲存和還原其狀態，也就是指定格式的一組識別碼和值。 這項功能對容器（例如 Visual Basic）很有用，可將其程式儲存為文字形式。 想要支援這項功能的控制項會實 [**IDataObject：：**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) IDataObject [**：： SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata) ，以將其屬性值分別傳遞至容器。 它是將此資訊轉換成文字並加以儲存的容器作業。 控制項使用的識別碼會對應至控制項的屬性名稱和值。 請參閱 OLE CDK 以取得這個屬性集的定義。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ActiveX控制](activex-controls.md)
</dt> </dl>

 

 