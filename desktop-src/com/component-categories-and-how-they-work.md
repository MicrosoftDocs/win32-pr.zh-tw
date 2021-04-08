---
title: 元件類別及其運作方式
description: 元件類別及其運作方式
ms.assetid: efbf4a25-3c73-4d09-a172-6676c6d6501b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf8065584ae2dc83e470428b7345eb2d9321d32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931908"
---
# <a name="component-categories-and-how-they-work"></a>元件類別及其運作方式

元件類別可識別軟體元件支援和需要的功能區域，每個類別或已識別的功能區域都使用一個登錄專案。 每個元件類別都是由全域唯一識別碼 (GUID) 在安裝控制項時，它會使用控制項的元件類別識別碼，將本身註冊為系統登錄中的控制項，請參閱 [自我註冊控制項](self-registration-for-controls.md)。 在控制項自我註冊中，它也會註冊它所執行的元件類別，以及需要容器來支援以成功裝載控制項的元件類別。

當控制項容器將控制項提供給要插入的使用者時，它只會讓使用者選取並具現化這些控制項，這些控制項將能夠在該環境中充分發揮作用。 例如，如果控制項容器不支援資料系結，則容器將不會允許使用者選取並具現化在登錄中具有專案的控制項，表示它們需要資料系結元件類別。 您可以使用控制項插入和 Api 的通用對話方塊來處理登錄專案。

元件類別不是累積或排除的，控制項可能需要任何混合的元件類別才能運作。 對於元件類別沒有任何必要專案的控制項，可能預期會在任何控制項容器中運作，而不需要控制項容器的任何特定功能就能運作。

以下是在這裡識別的元件類別，其中可能有更詳細的類別規格。

-   [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) 控制項內含專案。
-   透過 [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) 介面的簡單資料系結。
-   VB 4.0) 的其他資料系結介面所支援的 Advanced Databinding (。
-   Visual Basic 私用介面- [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat)、 [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol)
-   網際網路感知控制項。
-   無視窗控制項。

這不是類別的最終清單;當識別出新的需求時，未來可能會定義進一步的類別。 您可以從 Microsoft 取得最新的元件類別清單;這份清單反映了 Microsoft 所識別的元件類別，以及任何其他廠商已告知 Microsoft 的元件類別。

請務必記住，控制項應該盡可能嘗試在多個環境中工作。 如果有可能，當控制項放在不支援特定介面的容器時，控制項應該會降低其功能。 元件類別的目的是要防止控制項放在不適合的環境中，且控制項無法達成所需工作的情況。 一般情況下，當介面不存在時，控制項應該會正常地降級，控制項可能會選擇通知使用者有某些功能無法使用或清楚記載控制項容器所需的功能，以獲得最佳效能。

請注意，較舊的控制項和容器不會使用元件類別，而是會依賴登錄中控制項所存在的 control 關鍵字。 為了讓較舊的容器控制項能夠辨識，您可能會想要在登錄中註冊 control 關鍵字，控制項開發人員應該先檢查控制項是否可以成功裝載在這類容器中，再執行這項操作。 使用元件類別目錄的容器可能會成功地使用它們來裝載較舊的控制項，因為元件類別目錄 DLL 會處理對應，較舊的控制項 CATID ControlV1 有個別的分類， \_ 因此容器可以視需要選擇性地將其排除。

由於元件類別是由 Guid 所識別，因此提供特定特定功能的容器可能會有自己的類別識別碼，並使用 GUID 產生工具產生。 不過，這可能會破壞控制項和容器互通性的優點，因此最好是盡可能使用現有的元件類別。 當您定義新的元件類別以確保其符合 marketplace 的一般需求，並遵循 ActiveX 控制項的互通性精神時，我們鼓勵廠商一起參考。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[元件類別](component-categories.md)
</dt> </dl>

 

 




