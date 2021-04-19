---
description: 使用 Windows Media 視訊 9 Advanced Profile
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: 使用 Windows Media 視訊 9 Advanced Profile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106985802"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a><span data-ttu-id="68ce1-103">使用 Windows Media 視訊 9 Advanced Profile</span><span class="sxs-lookup"><span data-stu-id="68ce1-103">Using the Windows Media Video 9 Advanced Profile</span></span>

<span data-ttu-id="68ce1-104">「使用 [影片](workingwithvideo.md) 」一節中所述的基本影片程式也直接套用到 Windows Media 視訊 9 Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="68ce1-104">The basic video procedures described in the [Working with Video](workingwithvideo.md) section also apply directly to the Windows Media Video 9 Advanced Profile.</span></span> <span data-ttu-id="68ce1-105">不需要任何特殊程式。</span><span class="sxs-lookup"><span data-stu-id="68ce1-105">No special procedures are required.</span></span>

<span data-ttu-id="68ce1-106">Windows Media 視訊 9 Advanced Profile 與類別識別碼 CLSID \_ CWMV9EncMediaObject 和 clsid CWMVDecMediaObject 相關聯 \_ 。</span><span class="sxs-lookup"><span data-stu-id="68ce1-106">The Windows Media Video 9 Advanced Profile is associated with the class identifiers CLSID\_CWMV9EncMediaObject and CLSID\_CWMVDecMediaObject.</span></span> <span data-ttu-id="68ce1-107">使用此編解碼器之媒體類型的 FOURCC 值為 "WVC1"。</span><span class="sxs-lookup"><span data-stu-id="68ce1-107">The FOURCC value for media types using this codec is "WVC1".</span></span>

<span data-ttu-id="68ce1-108">Windows Media 視訊 9 Advanced Profile 支援所有常見的編碼模式，以及交錯編碼、混合交錯和漸進編碼、與顯示不同的解析度，以及範圍縮減功能。</span><span class="sxs-lookup"><span data-stu-id="68ce1-108">The Windows Media Video 9 Advanced Profile supports all common encoding modes as well interlaced encoding, mixed interlaced and progressive encoding, resolutions that are different than the display, and range reduction features.</span></span> <span data-ttu-id="68ce1-109">另一項功能是在位資料流程本身儲存序列和框架中繼資料的能力;之前，這必須使用 ASF 和資料單位延伸 API。</span><span class="sxs-lookup"><span data-stu-id="68ce1-109">Another feature is the ability to store sequence and frame metadata in the bit-stream itself; previously this had required use of the ASF and Data Unit Extensions API.</span></span>

<span data-ttu-id="68ce1-110">您可以使用登錄設定來控制 Windows Media 視訊 9 Advanced Profile 的下列屬性，而且沒有對應的 **IPropertyBag** 或 **IPropertyStore** 字串：</span><span class="sxs-lookup"><span data-stu-id="68ce1-110">The following properties of the Windows Media Video 9 Advanced Profile, which can be controlled using registry settings, do not have corresponding **IPropertyBag** or **IPropertyStore** strings:</span></span>

-   <span data-ttu-id="68ce1-111">Dquant 選項。</span><span class="sxs-lookup"><span data-stu-id="68ce1-111">Dquant Option.</span></span>
-   <span data-ttu-id="68ce1-112">Dquant 強度。</span><span class="sxs-lookup"><span data-stu-id="68ce1-112">Dquant Strength.</span></span>
-   <span data-ttu-id="68ce1-113">強制重迭。</span><span class="sxs-lookup"><span data-stu-id="68ce1-113">Force Overlap.</span></span>
-   <span data-ttu-id="68ce1-114">動作向量成本方法。</span><span class="sxs-lookup"><span data-stu-id="68ce1-114">Motion Vector Cost Method.</span></span>

## <a name="achieving-optimal-visual-quality"></a><span data-ttu-id="68ce1-115">達到最佳的視覺品質</span><span class="sxs-lookup"><span data-stu-id="68ce1-115">Achieving Optimal Visual Quality</span></span>

<span data-ttu-id="68ce1-116">針對大部分的影片資料，若要使用 Windows Media 視訊 9 Advanced Profile 達成最佳的視覺品質，您可以將 [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) 屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="68ce1-116">For most video data, to achieve optimal visual quality using the Windows Media Video 9 Advanced Profile, you can set the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property to 1.</span></span>

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a><span data-ttu-id="68ce1-117">關於先前的 Windows Media 視訊 9 Advanced Profile 編解碼器</span><span class="sxs-lookup"><span data-stu-id="68ce1-117">About the Previous Windows Media Video 9 Advanced Profile Codecs</span></span>

<span data-ttu-id="68ce1-118">Windows Media 視訊 9 Advanced Profile 編解碼器的最新版本是以「運動」圖片和電視工程師為基礎， (適用于 VC-1 (SMPTE 421M) Advanced Profile 的) 標準。</span><span class="sxs-lookup"><span data-stu-id="68ce1-118">The current version of the Windows Media Video 9 Advanced Profile codec is based on the Society of Motion Picture and Television Engineers (SMPTE) standard for VC-1 (SMPTE 421M) Advanced Profile.</span></span> <span data-ttu-id="68ce1-119">此編解碼器會取代 Windows 的舊版編解碼器，也稱為 Windows Media 視訊 9 Advanced Profile 編解碼器（由 FOURCC 碼 "WMVA" 識別）。</span><span class="sxs-lookup"><span data-stu-id="68ce1-119">This codec replaces the earlier codec from Windows also called the Windows Media Video 9 Advanced Profile codec which was identified by the FOURCC code "WMVA".</span></span> <span data-ttu-id="68ce1-120">前一版的 VC-1 編解碼器是在 VC-1 advanced profile standard 完成之前執行，不再支援。</span><span class="sxs-lookup"><span data-stu-id="68ce1-120">The previous version of the VC-1 codec was implemented before the VC-1 advanced profile standard was finalized, and is no longer supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68ce1-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="68ce1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68ce1-122">使用影片</span><span class="sxs-lookup"><span data-stu-id="68ce1-122">Working with Video</span></span>](workingwithvideo.md)
</dt> 
<dt>

[<span data-ttu-id="68ce1-123">使用 Windows Media 視訊 9 Advanced Profile 編解碼器的 Advanced 設定</span><span class="sxs-lookup"><span data-stu-id="68ce1-123">Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec</span></span>](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



