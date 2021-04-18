---
title: 多載 IPropertyNotifySink
description: 多載 IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037b27650ae68f355962454ae154d7c332c73518
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372521"
---
# <a name="overloading-ipropertynotifysink"></a>多載 IPropertyNotifySink

許多 ActiveX 控制項容器會執行無模式的屬性流覽視窗。 如果控制項的屬性是透過控制項的屬性頁改變的，則控制項的屬性可能會與這些屬性的容器視圖不同步 (控制項一律是正確的) 。 為了確保它一律具有控制項屬性的目前值，ActiveX 控制項容器可以 (資料系結) 多載 [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) 介面，也可以使用它來通知控制項屬性已變更。 這項技術是選擇性的，且不是 ActiveX 控制項容器或 ActiveX 控制項的必要項。

請注意，控制項只能使用 [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) 進行資料系結;這兩種用途都可免費使用 [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) 。

 

 




