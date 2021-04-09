---
title: 控制項屬性
description: 控制項屬性
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4749a7a7e408f6cd58951a72207ed801e4104d65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840784"
---
# <a name="control-properties"></a>控制項屬性

除了由控制項本身定義和執行的屬性之外，ActiveX 控制項技術也包含：

<dl> <dt>

<span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>環境屬性
</dt> <dd>

這些是由容器透過控制項用戶端網站所公開，以提供適用于所有內嵌在容器中之控制項的環境值。 例如，容器可以提供預設的背景色彩或控制項可使用的預設字型。 環境屬性會透過在容器的網站物件上實作為 **IDispatch** 來公開。 當容器的任何環境屬性變更值時，容器會呼叫控制項的 [**IOleControl：： OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) 方法。 在回應中，控制項可能需要更新自己的內部或視覺狀態以回應。 容器會指出哪些環境屬性以 DISPID 參數變更，或可能傳遞 DISPID \_ 未知，以指出多個環境屬性已變更。

</dd> <dt>

<span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>擴充屬性
</dt> <dd>

這些實際上是由容器執行，以包裝其包含的控制項，以提供容器管理的屬性，就像是原生控制項屬性一樣。 容器可以匯總控制項，加入擴充屬性來補充或覆寫控制項的屬性。 匯總的物件稱為「擴充控制項」。 在容器中，擴充控制項會顯示為控制項本身，而擴充屬性則顯示為由控制項公開。 容器透過其用戶端網站方法 [**>iolecontrolsite：： GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)支援擴充的控制項。 如果容器支援這項功能， **GetExtendedControl** 方法可讓控制項在網站之間流覽至容器提供的擴充控制項物件。 除了控制項通常透過 [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages)指定的頁面之外，容器也可以選擇顯示其擴充控制項的屬性頁。 因此，控制項必須先要求容器顯示內容框架，控制項才會嘗試這麼做。 此控制項會呼叫 [**>iolecontrolsite：： ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) 來執行此動作。 如果容器會執行此函式，則會顯示內容框架本身;如果方法傳回錯誤，控制項可以顯示內容框架。

</dd> </dl>

如需詳細資訊，請參閱下列主題：

-   [標準屬性](standard-properties.md)
-   [標準字型物件](standard-font-object.md)
-   [標準圖片物件](standard-picture-object.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項方法](control-methods.md)
</dt> </dl>

 

 




