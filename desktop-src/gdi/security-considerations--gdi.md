---
description: 本主題提供與 GDI 相關的安全性考慮資訊。 本主題不提供您需要瞭解的安全性問題。 相反地，請使用它作為此技術領域的起點和參考。
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 安全性考慮： GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71644da7d313e2efe0f287002c3e41a3a813a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944691"
---
# <a name="security-considerations-gdi"></a><span data-ttu-id="c4275-105">安全性考慮： GDI</span><span class="sxs-lookup"><span data-stu-id="c4275-105">Security Considerations: GDI</span></span>

<span data-ttu-id="c4275-106">本主題提供與 GDI 相關的安全性考慮資訊。</span><span class="sxs-lookup"><span data-stu-id="c4275-106">This topic provides information about security considerations related to GDI.</span></span> <span data-ttu-id="c4275-107">本主題不提供您需要瞭解的安全性問題。</span><span class="sxs-lookup"><span data-stu-id="c4275-107">This topic does not provide all you need to know about security issues.</span></span> <span data-ttu-id="c4275-108">相反地，請使用它作為此技術領域的起點和參考。</span><span class="sxs-lookup"><span data-stu-id="c4275-108">Instead, use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="c4275-109">GDI 通常有一些安全性考慮，因為它會處理顯示而非輸入。</span><span class="sxs-lookup"><span data-stu-id="c4275-109">GDI generally has few security concerns because it deals with display rather than input.</span></span> <span data-ttu-id="c4275-110">不過，以下是您應該考慮的一些問題。</span><span class="sxs-lookup"><span data-stu-id="c4275-110">However, here are a few issues that you should consider.</span></span>

<span data-ttu-id="c4275-111">點陣圖、中繼檔和字型是複雜的結構，可能會損毀。</span><span class="sxs-lookup"><span data-stu-id="c4275-111">Bitmaps, metafiles, and fonts are complex structures that could become corrupted.</span></span> <span data-ttu-id="c4275-112">最好的作法是嘗試確保這些專案不會被破壞，而不是來自可信任的來源。</span><span class="sxs-lookup"><span data-stu-id="c4275-112">It is good practice to try to ensure that these items are uncorrupted and from a trustworthy source.</span></span>

<span data-ttu-id="c4275-113">應用程式可以為某些列印和幕後處理 Api 指定安全描述項。</span><span class="sxs-lookup"><span data-stu-id="c4275-113">An application can specify the security descriptor for some of the printing and spooling APIs.</span></span> <span data-ttu-id="c4275-114">在設定安全描述項時，您應該要小心。</span><span class="sxs-lookup"><span data-stu-id="c4275-114">You should take care when setting the security descriptor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4275-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4275-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4275-116">Microsoft 安全性中心</span><span class="sxs-lookup"><span data-stu-id="c4275-116">Microsoft Security Central</span></span>](https://www.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="c4275-117">安全性開發人員中心</span><span class="sxs-lookup"><span data-stu-id="c4275-117">Security Developer Center</span></span>](https://technet.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="c4275-118">資訊安全技術中心</span><span class="sxs-lookup"><span data-stu-id="c4275-118">Security TechCenter</span></span>](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 



