---
description: VMR 視窗 (相容性) 模式
ms.assetid: e9fb1c83-860a-44c1-9633-c86f5d0fdadd
title: VMR 視窗 (相容性) 模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d27a5a115ac87475a27365a0211d93cf18e785983cda12ee338e73b24fb0f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049290"
---
# <a name="vmr-windowed-compatibility-mode"></a>VMR 視窗 (相容性) 模式

VMR 的設計目的是要與所有現有的 DirectShow 應用程式相容。 當它與現有的應用程式搭配使用時，VMR 會以視窗模式使用單一影片串流（也稱為相容性模式）來運作。 提供此模式的原因是，VMR-7 是 Windows XP 上的預設轉譯器，因此會自動用於對 [智慧型連線](intelligent-connect.md)方法的呼叫，例如 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)。 如果您的應用程式使用智慧型連線，而且只需要基本的轉譯功能，則不需要任何特殊的程式碼，就能在 Windows XP 上正確地轉譯為 VMR-7。

VMR-9 預設也會在視窗型/相容性模式下執行。 不過，VMR-9 永遠不是預設的影片轉譯器。 若要在應用程式中使用 VMR-9，您必須明確地將它加入至篩選圖形。 基於這個理由，而且因為無視窗模式提供比視窗模式更好的功能，所以在視窗型/相容性模式中使用 VMR-9 沒有特定的優點。

**在視窗型/相容性模式中使用 VMR-7**

不需要進行任何特殊的程式設計，就能在視窗型/相容性模式下設定或控制 VMR-7。 只要使用標準的圖形建立呼叫來建立篩選圖形，VMR 就會預設為這種模式。

在視窗型/相容性模式中，VMR 7 會建立自己的視窗來顯示影片。 若要這樣做，它會載入可公開 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 和 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面的視窗管理員元件。 您的應用程式可以為這些介面查詢篩選 Graph 管理員，與使用舊的影片轉譯器篩選器的方式完全相同。 如需詳細資訊，請參閱 [使用視窗模式](using-windowed-mode.md)。

下圖顯示視窗型/相容性模式中的 VMR-7。

![在相容性模式中 vmr](images/vmr-compat-mode.png)

為了保證最大的相容性層級，影片視窗的類別名稱會與舊的影片轉譯器篩選器所建立的相同，而且 VMR 仍會使用舊影片轉譯器的大部分視窗管理員程式碼。 在視窗型/相容性模式中，VMR 所耗用的系統資源不會超過舊的影片轉譯器。 因為 VMR-7 只有一個輸入資料流程處於視窗型/相容性模式，所以不會載入其混音器或組合器元件。

根據預設，VMR 會伸展影像以填滿影片視窗。 若要保留來源的外觀比例，請使用 VMR ARMODE LETTER 方塊旗標來呼叫 [**IVMRAspectRatioControl：： SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmraspectratiocontrol-setaspectratiomode) 方法 \_ \_ \_ 。

> [!Note]  
> 將影片視窗放在子視窗中的 MFC 應用程式必須定義空的 WM \_ ERASEBKGND 訊息處理常式，否則影片顯示區域將無法正確地重新繪製。

 

**在具有多個資料流程的視窗型/相容性模式中使用 VMR-7**

在視窗型/相容性模式中，VMR-7 預設會建立單一輸入的 pin，並停用混合模式。 若要啟用混合模式，您必須先設定 VMR，然後再進行連接。 如需詳細資訊，請參閱 [使用多個資料流程 (混合模式) 的 VMR ](vmr-with-multiple-streams--mixing-mode.md)。 在混合模式中，VMR 會載入混合和組合器元件，這需要更多的系統資源。

**在視窗模式中使用 VMR-9**

由於 VMR-9 不是預設轉譯器，因此它的相容性模式不會像這樣。 相反地，VMR-9 預設為視窗模式，具有四個輸入圖釘。 您可以使用此模式來混合最多四個影片串流。 如果您需要混用較大量的資料流程，您必須如 VMR 中所述，設定 [多個資料流程 (混合模式) ](vmr-with-multiple-streams--mixing-mode.md)。 否則，以視窗模式模式的 VMR-9 在視窗型/相容性模式中的行為就如同 VMR-7 一樣。

 

 



