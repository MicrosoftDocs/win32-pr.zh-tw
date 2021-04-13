---
description: IWebProxy 介面會定義下列屬性。
ms.assetid: 449b19ec-dc95-40f7-87af-84fb7dacb328
title: IWebProxy 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96628e7c799232b741e1834964a3a8ef6f6264c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386094"
---
# <a name="iwebproxy-properties"></a><span data-ttu-id="bebbd-103">IWebProxy 屬性</span><span class="sxs-lookup"><span data-stu-id="bebbd-103">IWebProxy Properties</span></span>

<span data-ttu-id="bebbd-104">[**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="bebbd-104">The [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) interface defines the following properties.</span></span>



| <span data-ttu-id="bebbd-105">屬性</span><span class="sxs-lookup"><span data-stu-id="bebbd-105">Property</span></span>                                                   | <span data-ttu-id="bebbd-106">描述</span><span class="sxs-lookup"><span data-stu-id="bebbd-106">Description</span></span>                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bebbd-107">**位址**</span><span class="sxs-lookup"><span data-stu-id="bebbd-107">**Address**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)                       | <span data-ttu-id="bebbd-108">取得和設定 proxy 伺服器的位址和小數埠號碼。</span><span class="sxs-lookup"><span data-stu-id="bebbd-108">Gets and sets the address and the decimal port number of the proxy server.</span></span>                                                |
| [<span data-ttu-id="bebbd-109">**自動**</span><span class="sxs-lookup"><span data-stu-id="bebbd-109">**AutoDetect**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_autodetect)                 | <span data-ttu-id="bebbd-110">取得和設定布林值，這個值會指出 [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) 是否會自動偵測 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="bebbd-110">Gets and sets a Boolean value that indicates whether [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) automatically detects proxy settings.</span></span> |
| [<span data-ttu-id="bebbd-111">**BypassList**</span><span class="sxs-lookup"><span data-stu-id="bebbd-111">**BypassList**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypasslist)                 | <span data-ttu-id="bebbd-112">取得和設定未使用 proxy 伺服器的位址集合。</span><span class="sxs-lookup"><span data-stu-id="bebbd-112">Gets and sets a collection of addresses that do not use the proxy server.</span></span>                                                 |
| [<span data-ttu-id="bebbd-113">**BypassProxyOnLocal**</span><span class="sxs-lookup"><span data-stu-id="bebbd-113">**BypassProxyOnLocal**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypassproxyonlocal) | <span data-ttu-id="bebbd-114">取得和設定布林值，指出本機位址是否略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="bebbd-114">Gets and sets a Boolean value that indicates whether local addresses bypass the proxy server.</span></span>                             |
| [<span data-ttu-id="bebbd-115">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="bebbd-115">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_readonly)                     | <span data-ttu-id="bebbd-116">取得布林值，指出 [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) 物件是否為唯讀。</span><span class="sxs-lookup"><span data-stu-id="bebbd-116">Gets a Boolean value that indicates whether the [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) object is read-only.</span></span>                        |
| [<span data-ttu-id="bebbd-117">**使用者**</span><span class="sxs-lookup"><span data-stu-id="bebbd-117">**UserName**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_username)                     | <span data-ttu-id="bebbd-118">取得並設定要提交給 proxy 伺服器進行驗證的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="bebbd-118">Gets and sets the user name to submit to the proxy server for authentication.</span></span>                                             |



 

 

 



