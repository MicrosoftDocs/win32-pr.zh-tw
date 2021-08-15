---
title: 多載 IPropertyNotifySink
description: 多載 IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4faca0027144498138e1a60bf3df9a29b618aeb7eb09198ff97a3dd7616be67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310021"
---
# <a name="overloading-ipropertynotifysink"></a>多載 IPropertyNotifySink

許多 ActiveX 控制容器都採用非強制回應屬性流覽視窗。 如果控制項的屬性是透過控制項的屬性頁改變的，則控制項的屬性可能會與這些屬性的容器視圖不同步 (控制項一律是正確的) 。 為了確保它一律具有控制項屬性的目前值，ActiveX 的控制項容器可以多載 [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)介面 (資料系結) ，也可以使用它來通知控制項屬性已變更。 這項技術是選擇性的，不是 ActiveX 控制容器或 ActiveX 控制項的必要項。

請注意，控制項只能使用 [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) 進行資料系結;這兩種用途都可免費使用 [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) 。

 

 




