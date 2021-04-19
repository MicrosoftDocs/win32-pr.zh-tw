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
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a><span data-ttu-id="7006d-103">Direct2D 不支援在 Internet Explorer 9 中轉譯為豐富的中繼檔</span><span class="sxs-lookup"><span data-stu-id="7006d-103">Direct2D does not support rendering to rich metafiles in Internet Explorer 9</span></span>

## <a name="platforms"></a><span data-ttu-id="7006d-104">平台</span><span class="sxs-lookup"><span data-stu-id="7006d-104">Platforms</span></span>

<span data-ttu-id="7006d-105">**用戶端** -windows Vista、windows 7、Windows 8</span><span class="sxs-lookup"><span data-stu-id="7006d-105">**Clients** – Windows Vista, Windows 7, Windows 8</span></span>  
<span data-ttu-id="7006d-106">**伺服器** – windows server 2008、windows Server 2008 R2、windows server 2012</span><span class="sxs-lookup"><span data-stu-id="7006d-106">**Servers** – Windows Server 2008, Windows Server 2008 R2, Windows Server 2012</span></span>  




## <a name="description"></a><span data-ttu-id="7006d-107">描述</span><span class="sxs-lookup"><span data-stu-id="7006d-107">Description</span></span>

<span data-ttu-id="7006d-108">由於 Internet Explorer 9 的內部轉譯變更， [IHTMLElementRender：:D rawtodc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) 和 [IViewObject：:D 原始](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) api 現在會建立包含單一點陣圖的中繼檔，以代表 web 內容，而不是包含文字和向量資訊的豐富中繼檔。</span><span class="sxs-lookup"><span data-stu-id="7006d-108">Due to internal rendering changes in Internet Explorer 9, the [IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) and [IViewObject::Draw](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) APIs will now create a metafile containing a single bitmap that represents the web content instead of a rich metafile containing text and vector info.</span></span> <span data-ttu-id="7006d-109">這種變更是因為從 GDI 轉譯移至硬體加速 Direct2D (D2D) 轉譯。</span><span class="sxs-lookup"><span data-stu-id="7006d-109">This change was due to the move from GDI rendering to hardware-accelerated Direct2D (D2D) rendering.</span></span>

<span data-ttu-id="7006d-110">這項變更會影響使用這些 Api 的應用程式，並依賴中繼檔中的文字或向量資訊。</span><span class="sxs-lookup"><span data-stu-id="7006d-110">This change affects apps that use these APIs and rely on text or vector info in the metafile.</span></span>

## <a name="manifestation"></a><span data-ttu-id="7006d-111">表現</span><span class="sxs-lookup"><span data-stu-id="7006d-111">Manifestation</span></span>

<span data-ttu-id="7006d-112">根據受此變更影響的應用程式，使用者可能會在其應用程式中看到中斷或不正確的行為。</span><span class="sxs-lookup"><span data-stu-id="7006d-112">Depending on the app that is affected by this change, users might see broken or incorrect behavior in their apps.</span></span>

## <a name="mitigation"></a><span data-ttu-id="7006d-113">降低</span><span class="sxs-lookup"><span data-stu-id="7006d-113">Mitigation</span></span>

<span data-ttu-id="7006d-114">只需要從 web 檔解壓縮文字資訊 (沒有定位資訊) 的應用程式可以使用 [innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) 屬性來將文字解壓縮。</span><span class="sxs-lookup"><span data-stu-id="7006d-114">Apps that only need to extract text info from a web document (without positioning info) can use the [innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) property to extract text.</span></span>

<span data-ttu-id="7006d-115">使用 IViewObject：:D raw 的應用程式可以使用 [功能 \_ IVIEWOBJECTDRAW \_ DMLT9 \_ 搭配 \_ gdi](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) 功能控制索引鍵，以在檔案模式時還原為 gdi 轉譯：</span><span class="sxs-lookup"><span data-stu-id="7006d-115">Apps that use IViewObject::Draw can use the [FEATURE\_IVIEWOBJECTDRAW\_DMLT9\_WITH\_GDI](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) feature control key to revert to GDI rendering if the document mode:</span></span>

-   <span data-ttu-id="7006d-116">小於或等於8</span><span class="sxs-lookup"><span data-stu-id="7006d-116">Is less or equal to 8</span></span>
-   <span data-ttu-id="7006d-117">FCK 授權該主機使用 GDI</span><span class="sxs-lookup"><span data-stu-id="7006d-117">The FCK authorizes that host to use GDI</span></span>
-   <span data-ttu-id="7006d-118">並將中繼檔 DC 傳遞給 API</span><span class="sxs-lookup"><span data-stu-id="7006d-118">And a metafile DC is passed to the API</span></span>

## <a name="resources"></a><span data-ttu-id="7006d-119">資源</span><span class="sxs-lookup"><span data-stu-id="7006d-119">Resources</span></span>

-   <span data-ttu-id="7006d-120">[IHTMLElementRender：:D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7006d-120">[IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span></span>
-   [<span data-ttu-id="7006d-121">IViewObject：:D 原始</span><span class="sxs-lookup"><span data-stu-id="7006d-121">IViewObject::Draw</span></span>](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   <span data-ttu-id="7006d-122">[IHTMLElement：： innerText 屬性](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7006d-122">[IHTMLElement::innerText Property](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span></span>
-   <span data-ttu-id="7006d-123">[ (我的網際網路功能控制項L) ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7006d-123">[Internet Feature Controls (I..L)](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span></span>

 

 