---
description: 本章節中的主題將討論國際字型的基本功能。
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: 國際字型管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ade599577f97c696d3205e32bfaaca106ddaae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975164"
---
# <a name="international-font-management"></a><span data-ttu-id="cd585-103">國際字型管理</span><span class="sxs-lookup"><span data-stu-id="cd585-103">International Font Management</span></span>

<span data-ttu-id="cd585-104">本章節中的主題將討論國際字型的基本功能。</span><span class="sxs-lookup"><span data-stu-id="cd585-104">The topics in this section address the basic functionality of International Fonts.</span></span> <span data-ttu-id="cd585-105">如需在您的應用程式中使用國際字型技術的指示，請參閱 [國際字型列舉和選取專案](using-international-fonts-and-text.md) ，以及 [使用 ms SHELL Dlg 和 ms shell dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md)。</span><span class="sxs-lookup"><span data-stu-id="cd585-105">For instructions on using the international font technology in your applications, see [International Font Enumeration and Selection](using-international-fonts-and-text.md) and [Using MS Shell Dlg and MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md).</span></span>

## <a name="font-management-infrastructure"></a><span data-ttu-id="cd585-106">字型管理基礎結構</span><span class="sxs-lookup"><span data-stu-id="cd585-106">Font Management Infrastructure</span></span>

<span data-ttu-id="cd585-107">從 Windows 7 開始，字型管理基礎結構支援隱藏不適合用戶字型挑選清單的字型。</span><span class="sxs-lookup"><span data-stu-id="cd585-107">Starting with Windows 7, the font management infrastructure supports the hiding of fonts which are not appropriate for a user's font selection lists.</span></span> <span data-ttu-id="cd585-108">預設系統設定會選擇自動隱藏未針對輸入語言 ()  (鍵盤) 在作業系統系統上啟用的字型。</span><span class="sxs-lookup"><span data-stu-id="cd585-108">The default system settings will choose to auto-hide fonts which are not designed for the input language(s) (keyboards) enabled on the OS system.</span></span> <span data-ttu-id="cd585-109">此外，使用者也可以選擇以手動方式隱藏字型主控台中的字型。</span><span class="sxs-lookup"><span data-stu-id="cd585-109">In addition, users can choose to manually hide fonts in the Fonts Control Panel.</span></span> <span data-ttu-id="cd585-110">這項功能表示使用者不再需要面對不適當字型的長清單，對於使用非拉丁腳本的國際使用者來說特別有用。</span><span class="sxs-lookup"><span data-stu-id="cd585-110">This feature means users need no longer be faced with long lists of inappropriate fonts, and is particularly valuable for international users working in non-Latin scripts.</span></span>

<span data-ttu-id="cd585-111">在 Windows 7 中，沒有任何 Api 可直接查詢隱藏的字型，或將字型設定為隱藏。</span><span class="sxs-lookup"><span data-stu-id="cd585-111">In Windows 7, there are no APIs for directly querying which fonts are hidden, or for setting fonts to be hidden.</span></span> <span data-ttu-id="cd585-112">不過，這並不表示您無法在應用程式中利用此功能。</span><span class="sxs-lookup"><span data-stu-id="cd585-112">However, this does not mean you cannot take advantage of this feature in your application.</span></span> <span data-ttu-id="cd585-113">如果您使用 Windows [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) API (字型通用對話方塊) 若要立即選取字型，您將可免費取得新的行為。</span><span class="sxs-lookup"><span data-stu-id="cd585-113">If you use the Windows [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) API (Font common dialog) to enable font selection today, you will get the new behavior for free.</span></span> <span data-ttu-id="cd585-114">) 在 Windows 7 中引進的新 Windows Scenic 功能區 (字型控制項也支援此行為，並提供另一個原因來「Ribbonize」您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="cd585-114">The new Windows Scenic Ribbon (Font Controls) introduced in Windows 7 also supports this behavior and provides another reason to "Ribbonize" your applications.</span></span> <span data-ttu-id="cd585-115">如需在功能區和 **ChooseFont** 中使用字型控制項來顯示字型，同時篩選出隱藏字型的詳細資訊，請參閱 [國際字型列舉和選取](using-international-fonts-and-text.md)。</span><span class="sxs-lookup"><span data-stu-id="cd585-115">For details of using Font Controls in Ribbon and **ChooseFont** to display fonts while filtering out the hidden fonts, please reference [International Font Enumeration and Selection](using-international-fonts-and-text.md).</span></span>

<span data-ttu-id="cd585-116">請注意，隱藏字型只會影響字型選取的 UI。</span><span class="sxs-lookup"><span data-stu-id="cd585-116">Note that hiding fonts only impacts font selection UI.</span></span> <span data-ttu-id="cd585-117">它不會影響繪圖 Api。</span><span class="sxs-lookup"><span data-stu-id="cd585-117">It does not impact drawing APIs.</span></span> <span data-ttu-id="cd585-118">當您選取字型至裝置內容時，因為隱藏了字型，所以不會影響繪圖。</span><span class="sxs-lookup"><span data-stu-id="cd585-118">When a font is selected into a device context, there is no effect on drawing due to the font being hidden.</span></span> <span data-ttu-id="cd585-119">[**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)函式會繼續列舉設定為隱藏的字型。</span><span class="sxs-lookup"><span data-stu-id="cd585-119">The [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) function continues to enumerate fonts that are set to hidden.</span></span>

## <a name="gdi-font-embedding-and-subsetting"></a><span data-ttu-id="cd585-120">GDI 字型內嵌和子集</span><span class="sxs-lookup"><span data-stu-id="cd585-120">GDI Font Embedding and Subsetting</span></span>

<span data-ttu-id="cd585-121">國際字型技術會利用「內嵌服務」程式庫，讓您可以將 TrueType 和 OpenType 字型組合成檔或檔案。</span><span class="sxs-lookup"><span data-stu-id="cd585-121">International Fonts technology makes use of the Font Embedding Services Library to allow you to bundle TrueType and OpenType fonts into a document or file.</span></span> <span data-ttu-id="cd585-122">在檔案中內嵌字型可保證字型會出現在接收檔案的電腦上。</span><span class="sxs-lookup"><span data-stu-id="cd585-122">Embedding a font in a file guarantees that the font will be present on the computer receiving the file.</span></span> <span data-ttu-id="cd585-123">如需詳細資訊，請參閱 [字型內嵌參考](../gdi/font-embedding-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="cd585-123">For more information, see [Font Embedding Reference](../gdi/font-embedding-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd585-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="cd585-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd585-125">國際字型列舉和選取</span><span class="sxs-lookup"><span data-stu-id="cd585-125">International Font Enumeration and Selection</span></span>](using-international-fonts-and-text.md)
</dt> <dt>

[<span data-ttu-id="cd585-126">使用 MS Shell Dlg 和 MS Shell Dlg 2</span><span class="sxs-lookup"><span data-stu-id="cd585-126">Using MS Shell Dlg and MS Shell Dlg 2</span></span>](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[<span data-ttu-id="cd585-127">字型內嵌參考</span><span class="sxs-lookup"><span data-stu-id="cd585-127">Font Embedding Reference</span></span>](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 
