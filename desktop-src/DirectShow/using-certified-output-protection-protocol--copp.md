---
description: '使用認證輸出保護通訊協定 (COPP) '
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: '使用認證輸出保護通訊協定 (COPP) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76460e335985c2aab7f9047b55d2df05aace0269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990323"
---
# <a name="using-certified-output-protection-protocol-copp"></a><span data-ttu-id="9f226-103">使用認證輸出保護通訊協定 (COPP) </span><span class="sxs-lookup"><span data-stu-id="9f226-103">Using Certified Output Protection Protocol (COPP)</span></span>

<span data-ttu-id="9f226-104">經認證的輸出保護通訊協定 (COPP) 可讓應用程式在從圖形介面卡移至顯示裝置時，保護影片串流。</span><span class="sxs-lookup"><span data-stu-id="9f226-104">Certified Output Protection Protocol (COPP) enables an application to protect a video stream as it travels from the graphics adapter to the display device.</span></span> <span data-ttu-id="9f226-105">應用程式可以使用 COPP 來探索哪些類型的實體連接器連接到顯示裝置，以及可用的輸出保護類型。</span><span class="sxs-lookup"><span data-stu-id="9f226-105">An application can use COPP to discover what kind of physical connector is attached to the display device, and what types of output protection are available.</span></span> <span data-ttu-id="9f226-106">保護機制包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="9f226-106">Protection mechanisms include the following:</span></span>

-   <span data-ttu-id="9f226-107">High-Bandwidth 數位內容保護 (HDCP) </span><span class="sxs-lookup"><span data-stu-id="9f226-107">High-Bandwidth Digital Content Protection (HDCP)</span></span>
-   <span data-ttu-id="9f226-108">複製世代管理系統—類比 (CGMS-A) </span><span class="sxs-lookup"><span data-stu-id="9f226-108">Copy Generation Management System — Analog (CGMS-A)</span></span>
-   <span data-ttu-id="9f226-109">類比禁止複製 (ACP) </span><span class="sxs-lookup"><span data-stu-id="9f226-109">Analog Copy Protection (ACP)</span></span>

<span data-ttu-id="9f226-110">如果圖形介面卡支援其中一種機制，應用程式可以使用 COPP 來設定保護層級。</span><span class="sxs-lookup"><span data-stu-id="9f226-110">If the graphics adapter supports one of these mechanisms, the application can use COPP to set the protection level.</span></span>

<span data-ttu-id="9f226-111">COPP 會定義用來建立與圖形驅動程式安全通道的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9f226-111">COPP defines a protocol that is used to establish a secure communications channel with the graphics driver.</span></span> <span data-ttu-id="9f226-112">它會使用 (Mac) 的訊息驗證碼，來確認應用程式與顯示驅動程式之間所傳遞 COPP 命令的完整性。</span><span class="sxs-lookup"><span data-stu-id="9f226-112">It uses Message Authentication Codes (MACs) to verify the integrity of the COPP commands that are passed between the application and the display driver.</span></span> <span data-ttu-id="9f226-113">應用程式會使用 COPP，方法是在 DirectShow 視頻混合轉譯器篩選器的 [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) 介面上呼叫方法， (VMR-7 或 VMR-9) 。</span><span class="sxs-lookup"><span data-stu-id="9f226-113">The application uses COPP by calling methods on the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface of the DirectShow Video Mixing Renderer filter (VMR-7 or VMR-9).</span></span>

<span data-ttu-id="9f226-114">COPP 不會定義可能適用于數位媒體內容的數位版權原則任何內容。</span><span class="sxs-lookup"><span data-stu-id="9f226-114">COPP does not define anything about the digital rights policies that might apply to digital media content.</span></span> <span data-ttu-id="9f226-115">此外，COPP 本身不會執行任何輸出保護系統。</span><span class="sxs-lookup"><span data-stu-id="9f226-115">Also, COPP itself does not implement any output protection systems.</span></span> <span data-ttu-id="9f226-116">COPP 通訊協定只是提供一種方法，可讓您使用介面卡所提供的保護系統，在圖形介面卡上設定和查詢保護層級。</span><span class="sxs-lookup"><span data-stu-id="9f226-116">The COPP protocol simply provides a way to set and query protection levels on the graphics adapter, using the protection systems provided by the adapter.</span></span>

<span data-ttu-id="9f226-117">本節假設您已熟悉下列技術：</span><span class="sxs-lookup"><span data-stu-id="9f226-117">This section assumes that you are familiar with the following technologies:</span></span>

-   <span data-ttu-id="9f226-118">DirectShow</span><span class="sxs-lookup"><span data-stu-id="9f226-118">DirectShow</span></span>
-   <span data-ttu-id="9f226-119">Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="9f226-119">Windows Media Format SDK</span></span>
-   <span data-ttu-id="9f226-120">XML</span><span class="sxs-lookup"><span data-stu-id="9f226-120">XML</span></span>
-   <span data-ttu-id="9f226-121">公開金鑰密碼編譯和對稱式密碼編譯</span><span class="sxs-lookup"><span data-stu-id="9f226-121">Public-key cryptography and symmetric cryptography</span></span>

<span data-ttu-id="9f226-122">本節中的程式碼範例會使用 Microsoft 的 CryptoAPI 來執行密碼編譯作業。</span><span class="sxs-lookup"><span data-stu-id="9f226-122">The code examples in this section use Microsoft's CryptoAPI to perform cryptographic operations.</span></span> <span data-ttu-id="9f226-123">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="9f226-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="9f226-124">COPP 總覽</span><span class="sxs-lookup"><span data-stu-id="9f226-124">Overview of COPP</span></span>](overview-of-copp.md)
-   [<span data-ttu-id="9f226-125">取得驅動程式的憑證鏈</span><span class="sxs-lookup"><span data-stu-id="9f226-125">Obtaining the Driver's Certificate Chain</span></span>](obtaining-the-drivers-certificate-chain.md)
-   [<span data-ttu-id="9f226-126">驗證憑證鏈</span><span class="sxs-lookup"><span data-stu-id="9f226-126">Validating the Certificate Chain</span></span>](validating-the-certificate-chain.md)
-   [<span data-ttu-id="9f226-127">憑證撤銷清單</span><span class="sxs-lookup"><span data-stu-id="9f226-127">Certificate Revocation Lists</span></span>](certificate-revocation-lists.md)
-   [<span data-ttu-id="9f226-128">匯入驅動程式的公開金鑰</span><span class="sxs-lookup"><span data-stu-id="9f226-128">Importing the Driver's Public Key</span></span>](importing-the-drivers-public-key.md)
-   [<span data-ttu-id="9f226-129">起始 COPP 會話</span><span class="sxs-lookup"><span data-stu-id="9f226-129">Initiating a COPP Session</span></span>](initiating-a-copp-session.md)
-   [<span data-ttu-id="9f226-130">傳送 COPP 狀態要求</span><span class="sxs-lookup"><span data-stu-id="9f226-130">Sending COPP Status Requests</span></span>](sending-copp-status-requests.md)
-   [<span data-ttu-id="9f226-131">傳送 COPP 命令</span><span class="sxs-lookup"><span data-stu-id="9f226-131">Sending COPP Commands</span></span>](sending-copp-commands.md)
-   [<span data-ttu-id="9f226-132">測試圖形驅動程式是否支援 COPP</span><span class="sxs-lookup"><span data-stu-id="9f226-132">Testing Whether a Graphics Driver Supports COPP</span></span>](testing-whether-a-graphics-driver-supports-copp.md)
-   [<span data-ttu-id="9f226-133">COPP 查詢參考</span><span class="sxs-lookup"><span data-stu-id="9f226-133">COPP Query Reference</span></span>](copp-query-reference.md)
-   [<span data-ttu-id="9f226-134">COPP 命令參考</span><span class="sxs-lookup"><span data-stu-id="9f226-134">COPP Command Reference</span></span>](copp-command-reference.md)

## <a name="related-topics"></a><span data-ttu-id="9f226-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f226-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f226-136">使用影片混合轉譯器</span><span class="sxs-lookup"><span data-stu-id="9f226-136">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



