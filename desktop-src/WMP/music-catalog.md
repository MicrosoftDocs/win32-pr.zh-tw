---
title: 音樂類別目錄
description: 音樂類別目錄
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Windows Media Player 線上商店、音樂目錄
- 線上商店、音樂目錄
- 輸入1個線上商店、音樂目錄
- Windows Media Player 線上商店，目錄編譯器
- 線上商店，目錄編譯器
- 輸入1個線上商店、目錄編譯器
- 音樂目錄
- 目錄編譯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479a74393ee4d853f591cb6d75eef8be741c9228
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023012"
---
# <a name="music-catalog"></a><span data-ttu-id="c47b4-111">音樂類別目錄</span><span class="sxs-lookup"><span data-stu-id="c47b4-111">Music Catalog</span></span>

<span data-ttu-id="c47b4-112">類型1線上商店會以一組定位鍵分隔值 (TSV) 檔案來建立其音樂目錄。</span><span class="sxs-lookup"><span data-stu-id="c47b4-112">A type 1 online store creates its music catalog as a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="c47b4-113">然後，線上商店會使用 Microsoft 的 [目錄](catalog-compiler-for-type-1-online-stores.md) 編譯器將 TSV 檔案編譯成可 Windows Media Player 下載的壓縮類別目錄。</span><span class="sxs-lookup"><span data-stu-id="c47b4-113">Then the online store uses Microsoft's [catalog compiler](catalog-compiler-for-type-1-online-stores.md) to compile the TSV files into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="c47b4-114">Windows Media Player 可以下載完整的類別目錄檔案或目錄更新檔案。</span><span class="sxs-lookup"><span data-stu-id="c47b4-114">Windows Media Player can download full catalog files or catalog update files.</span></span> <span data-ttu-id="c47b4-115">目錄更新只包含上次目錄更新之後變更的目錄資訊。</span><span class="sxs-lookup"><span data-stu-id="c47b4-115">Catalog updates contain only the catalog information that has changed since the last catalog update.</span></span> <span data-ttu-id="c47b4-116">由內容合作夥伴外掛程式決定是否要下載完整目錄或更新。</span><span class="sxs-lookup"><span data-stu-id="c47b4-116">It is up to the content partner plug-in to determine whether to download a full catalog or an update.</span></span> <span data-ttu-id="c47b4-117">無論是哪一種情況，Windows Media Player 都會在來自外掛程式的通知時，將變更套用至目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="c47b4-117">In either case, Windows Media Player applies the changes to the current catalog upon notification from the plug-in.</span></span>

<span data-ttu-id="c47b4-118">如果線上商店已備妥新的目錄，此外掛程式可以藉由呼叫 [IWMPContentPartnerCallback：： notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) 並傳遞 wmpcnNewCatalogAvailable 作為 *型* 別參數的值，來通知玩家。</span><span class="sxs-lookup"><span data-stu-id="c47b4-118">If the online store has a new catalog prepared, the plug-in can notify the Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) and passing wmpcnNewCatalogAvailable as the value for the *type* parameter.</span></span>

<span data-ttu-id="c47b4-119">當 Windows Media Player 準備好下載目錄或更新時，播放程式會呼叫 [IWMPContentPartner：： GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)。</span><span class="sxs-lookup"><span data-stu-id="c47b4-119">When Windows Media Player is ready to download a catalog or update, the Player calls [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> <span data-ttu-id="c47b4-120">這個方法會將目前目錄的相關資訊提供給外掛程式，例如目錄版本和地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="c47b4-120">This method provides the plug-in with information about the current catalog, such as the catalog version and locale identifier.</span></span> <span data-ttu-id="c47b4-121">外掛程式的回應方式是提供統一資源定位器 (URL) 正確的完整目錄或更新，以及更新的版本號碼和到期日。</span><span class="sxs-lookup"><span data-stu-id="c47b4-121">The plug-in responds by supplying the uniform resource locator (URL) of the correct full catalog or update, as well as an updated version number and expiration date.</span></span> <span data-ttu-id="c47b4-122">Windows Media Player 會根據外掛程式在 **GetCatalogURL** 中提供的資訊，定期要求類別目錄更新。</span><span class="sxs-lookup"><span data-stu-id="c47b4-122">Windows Media Player will periodically request catalog updates based upon the information provided by the plug-in in **GetCatalogURL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c47b4-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="c47b4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c47b4-124">**關於類型1線上商店**</span><span class="sxs-lookup"><span data-stu-id="c47b4-124">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="c47b4-125">**類型1線上商店的目錄編譯器**</span><span class="sxs-lookup"><span data-stu-id="c47b4-125">**Catalog Compiler for Type 1 Online Stores**</span></span>](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="c47b4-126">**IWMPContentPartner 介面**</span><span class="sxs-lookup"><span data-stu-id="c47b4-126">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




