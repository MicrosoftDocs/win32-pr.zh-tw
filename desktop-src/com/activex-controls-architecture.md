---
title: ActiveX 控制項架構
description: ActiveX 控制項技術是以 OLE 中許多較低層級物件和介面的基礎為基礎。 控制項上可用的確切介面會因其功能而有所不同。 本節將進一步探討控制項可能提供的功能。
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0592d774e1930623803d0769fb7890709a2f21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672568"
---
# <a name="activex-controls-architecture"></a>ActiveX 控制項架構

ActiveX 控制項技術是以 OLE 中許多較低層級物件和介面的基礎為基礎。 控制項上可用的確切介面會因其功能而有所不同。 本節將進一步探討控制項可能提供的功能。

ActiveX 控制項可用來提供在應用程式中建立使用者介面的建立區塊。 例如，當按下容器應用程式時，在容器應用程式中起始動作的按鈕是一個簡單的控制項。 以下是提供這些使用者介面建立區塊的相關層面：

-   控制項可以內嵌在其容器用戶端內，以支援用戶端內的一些使用者介面活動。 因此，當控制項內嵌在容器內時，必須提供其本身的視覺標記法，並需要提供方法來儲存其狀態，例如其屬性值及其在容器中的位置。 用戶端必須支援做為内嵌物件的容器。
-   藉由使用鍵盤或滑鼠啟用控制項，終端使用者就會在用戶端應用程式中起始一些動作。 因此，控制項必須回應鍵盤活動，而且必須能夠與用戶端通訊，如此它就可以通知其活動的容器，並在用戶端觸發事件。
-   用戶端通常也會提供程式設計語言，讓使用者可以透過它來起始控制項的屬性和方法所提供的動作。 因此，控制項必須支援自動化，以及一組設計階段與執行時間功能。

由於其在提供使用者介面建立區塊中的角色，因此，控制項通常會使用 OLE 技術來支援下欄區域中的功能，如下所示：

<dl> <dt>

<span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>屬性和方法
</dt> <dd>

控制項和任何 OLE 物件一樣，都可以透過一組包含屬性和方法的傳入介面，提供大部分的功能。 容器可以提供其他環境屬性，也可以支援透過匯總延伸控制項的屬性。 這些功能可在 OLE automation、屬性頁、可連線物件和 ActiveX 控制項技術上 rest。

</dd> <dt>

<span id="Events"></span><span id="events"></span><span id="EVENTS"></span>事件
</dt> <dd>

除了提供屬性和方法之外，ActiveX 控制項也可以提供輸出介面，通知其事件的用戶端。 用戶端必須支援這些事件的處理。 這些功能使用 OLE automation 和可連接的物件。

</dd> <dt>

<span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>視覺標記法
</dt> <dd>

控制項可以支援定位，並在其容器內顯示本身。 容器會定位控制項並判斷其大小。 這些功能使用複合檔案技術，包括 OLE 拖放技術。

</dd> <dt>

<span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>鍵盤處理
</dt> <dd>

控制項可以回應鍵盤快速鍵，讓終端使用者可以起始控制項所執行的動作。 容器會管理其所有內嵌控制項的鍵盤活動。 這些功能使用控制項和複合檔案技術。

</dd> <dt>

<span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>堅持
</dt> <dd>

控制項可以儲存其狀態。 用戶端會管理其內嵌控制項的持續性。 這些功能使用結構化儲存體和物件持續性技術。

</dd> <dt>

<span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>註冊和授權
</dt> <dd>

控制項通常支援自我註冊，並且在具現化時，會建立一組登錄專案。 您也可以授權控制項來協助防止未經授權的使用。

</dd> </dl>

大部分的功能都牽涉到控制項及其用戶端容器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ActiveX 控制項](activex-controls.md)
</dt> </dl>

 

 




