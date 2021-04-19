---
title: Direct2D 不支援在 Internet Explorer 9 中轉譯為豐富的中繼檔
description: Direct2D 不支援在 Internet Explorer 9 中轉譯為豐富的中繼檔
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f51ae6d098c08c0a18656aae2adf3d79d68652
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314821"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a>Direct2D 不支援在 Internet Explorer 9 中轉譯為豐富的中繼檔

## <a name="platforms"></a>平台

**用戶端** -windows Vista、windows 7、Windows 8  
**伺服器** – windows server 2008、windows Server 2008 R2、windows server 2012  




## <a name="description"></a>描述

由於 Internet Explorer 9 的內部轉譯變更， [IHTMLElementRender：:D rawtodc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) 和 [IViewObject：:D 原始](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) api 現在會建立包含單一點陣圖的中繼檔，以代表 web 內容，而不是包含文字和向量資訊的豐富中繼檔。 這種變更是因為從 GDI 轉譯移至硬體加速 Direct2D (D2D) 轉譯。

這項變更會影響使用這些 Api 的應用程式，並依賴中繼檔中的文字或向量資訊。

## <a name="manifestation"></a>表現

根據受此變更影響的應用程式，使用者可能會在其應用程式中看到中斷或不正確的行為。

## <a name="mitigation"></a>降低

只需要從 web 檔解壓縮文字資訊 (沒有定位資訊) 的應用程式可以使用 [innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) 屬性來將文字解壓縮。

使用 IViewObject：:D raw 的應用程式可以使用 [功能 \_ IVIEWOBJECTDRAW \_ DMLT9 \_ 搭配 \_ gdi](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) 功能控制索引鍵，以在檔案模式時還原為 gdi 轉譯：

-   小於或等於8
-   FCK 授權該主機使用 GDI
-   並將中繼檔 DC 傳遞給 API

## <a name="resources"></a>資源

-   [IHTMLElementRender：:D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))
-   [IViewObject：:D 原始](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   [IHTMLElement：： innerText 屬性](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))
-   [ (我的網際網路功能控制項L) ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))

 

 