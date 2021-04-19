---
title: '介面 (控制項和屬性頁) '
description: 下列介面可用來建立標準 COM 物件和屬性頁。
ms.assetid: f0d655b3-fa92-4553-ba21-617649a922a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e143ab1793eaf0335bbcf04093707bdc359e868e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106968136"
---
# <a name="interfaces-controls-and-property-pages"></a>介面 (控制項和屬性頁) 

下列介面可用來建立標準 COM 物件和屬性頁。



| 介面                                             | 描述                                                                                                                                                                                                  |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**>ifont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)                                | 提供 Windows 字型物件周圍的包裝函式。                                                                                                                                                             |
| [**>ifontdisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)                        | 透過 Automation 公開字型物件的屬性。 它會提供 [**>ifont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) 方法的子集。                                                                                           |
| [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol)                    | 提供在控制項物件中支援鍵盤助憶鍵、環境屬性和事件的功能。                                                                                                  |
| [**>iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)            | 提供的方法可讓網站物件管理容器內的每個內嵌控制項。                                                                                                           |
| [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)  | 抓取物件所提供之屬性頁中的資訊。                                                                                                                                        |
| [**圖片**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture)                          | 管理圖片物件和其屬性。 圖片物件提供點陣圖、圖示和中繼檔的非語言相關抽象概念。                                                                       |
| [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)                  | 透過 Automation 公開圖片物件的屬性。 它提供透過 [**圖片**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) 方法提供的功能子集。                                                |
| [**IPointerInactive**](/windows/desktop/api/OCIdl/nn-ocidl-ipointerinactive)          | 讓物件在大部分的時間都保持非使用中狀態，但仍參與與滑鼠的互動，包括拖放。                                                                         |
| [**IPrint**](/windows/desktop/api/DocObj/nn-docobj-iprint)                              | 在一般和使用中的檔案中啟用複合檔案，以支援以程式設計方式列印。                                                                                                   |
| [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)    | 由接收物件實作為輸出介面，從支援 [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) 的物件接收有關屬性變更的通知。                       |
| [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage)                | 提供屬性頁物件的主要功能，此物件會管理屬性工作表內的特定頁面。                                                                                                 |
| [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)              | [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage)的延伸模組，可支援在頁面上進行屬性的初始選擇。                                                                                                 |
| [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite)        | 提供屬性頁面網站物件的主要功能。                                                                                                                                                  |
| [**IQuickActivate**](/windows/desktop/api/OCIdl/nn-ocidl-iquickactivate)              | 啟用控制項和容器，以避免載入控制項時發生效能瓶頸。 它會將控制項與其容器之間的載入時間或初始化時間的信號結合成單一呼叫。 |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)          | 提供簡單的框架控制項，作為其他嵌套控制項的簡單容器。                                                                                                                      |
| [**ISpecifyPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages) | 表示物件支援屬性頁。                                                                                                                                                            |



 

 

 
