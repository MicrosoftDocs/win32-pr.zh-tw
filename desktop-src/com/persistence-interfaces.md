---
title: 持續性介面
description: 持續性介面
ms.assetid: a93582b3-bdbf-430d-b4a6-c0df7bc35dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e1acbd1074fd5fa4e87e571a1e21ab48d5d075
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550503"
---
# <a name="persistence-interfaces"></a>持續性介面

具有任何類型之持續性狀態的物件必須至少執行一個 IPersist \* 介面（最好是多個介面），才能為容器提供最具彈性的選擇來儲存控制項的狀態。

如果控制項有任何持續性狀態，則至少必須執行 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) 或 [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) (這兩個互斥，而且不應該同時針對大部分的) 來執行。 當控制項想要知道何時建立新的，而不是從現有的持續狀態重載時，會使用後者， (**IPersistStream** 沒有建立的新功能) 。 其中一個介面存在表示控制項可以將其持續狀態儲存並載入至資料流程，也就是 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)的實例。

除了這兩個以資料流程為基礎的介面之外， \* 下表所列的 IPersist 介面也可以選擇性地提供，以支援擴充 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)以外位置的持續性。

識別出一組元件類別，以涵蓋持續性介面的支援，請參閱 [元件類別](component-categories.md)。



| 介面                                                              | 使用方式                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))<br/>           | 物件可以將其狀態儲存並載入固定長度的連續位元組陣列 (記憶體) 。<br/>                                                                                                                                                                                                                                                    |
| [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/>                  | 物件可將其狀態儲存並載入至 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 實例。 希望將可插入的控制項標示為其他複合檔案物件 (插入非控制項感知容器中) 必須支援此介面。<br/>                                                                                               |
| [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)<br/> | 物件可以將其狀態儲存並載入至容器所執行之 IPropertyBag 的個別屬性。 這是用來在某些容器中以文字功能的形式儲存。<br/>                                                                                                                                                          |
| [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/>  | 物件可以儲存其狀態，並將其載入至以標記命名的位置。 此控制項會呼叫 [**IMoniker：： BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) ，以抓取其所需的儲存介面，例如 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage)、 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)、 [**ILockBytes**](/windows/desktop/api/objidl/nn-objidl-ilockbytes)、 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)等。<br/> |



 

雖然 [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) 的支援是選擇性的，但強烈建議使用「儲存為文字」功能的容器做為優化，例如 Visual Basic。

除了 [**IPersistStream：： GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax)、 [**IPersistStreamInit：： GetSizeMax**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-getsizemax)和 [**IPersistMemory：： GetSizeMax**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768208(v=vs.85))之外，每個介面的所有方法都必須完全實作為。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項](controls.md)
</dt> </dl>

 

