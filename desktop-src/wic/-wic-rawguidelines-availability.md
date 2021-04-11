---
description: 編解碼器可用性和平臺支援
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: 編解碼器可用性和平臺支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc485c5f8db9ff7883263cd614578705eccd3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194119"
---
# <a name="codec-availability-and-platform-support"></a><span data-ttu-id="2ab14-103">編解碼器可用性和平臺支援</span><span class="sxs-lookup"><span data-stu-id="2ab14-103">Codec Availability and Platform Support</span></span>

<span data-ttu-id="2ab14-104">Microsoft 建議相機廠商在使用新攝影機的軟體發佈中， (WIC) 編解碼器，並將更新的編解碼器安裝在 Windows 7、Windows Vista 和 Windows XP 的預設廠商軟體上，以更新 Windows 影像處理元件。</span><span class="sxs-lookup"><span data-stu-id="2ab14-104">Microsoft recommends that camera vendors include updated RAW Windows Imaging Component (WIC) codecs in the software distribution with new cameras and that the updated codec be installed with the default vendor software installation Windows 7, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2ab14-105">攝影機廠商也應提供最新的 WIC 編解碼器，以從其支援網站下載。</span><span class="sxs-lookup"><span data-stu-id="2ab14-105">Camera vendors should also provide the latest WIC codec as a download from their support sites.</span></span>

## <a name="codec-discovery"></a><span data-ttu-id="2ab14-106">編解碼器探索</span><span class="sxs-lookup"><span data-stu-id="2ab14-106">Codec Discovery</span></span>

<span data-ttu-id="2ab14-107">Microsoft 正在進行下列動作，以協助將使用者指向廠商的網站，以取得編解碼器下載：</span><span class="sxs-lookup"><span data-stu-id="2ab14-107">Microsoft is doing the following to help point users to vendors' Web sites for codec downloads:</span></span>

-   <span data-ttu-id="2ab14-108">在 Windows 檔案總管中，如果使用者按兩下無法辨識的檔案 (預設情況下，當原始檔案在電腦上，但尚未) 安裝編解碼器時，對話方塊會回報檔案無法辨識，並詢問使用者是否想要尋找可理解檔案的程式。</span><span class="sxs-lookup"><span data-stu-id="2ab14-108">In Windows Explorer, if a user double-clicks a file that is not recognized (the default case when a RAW file is on the computer, but the codec is not installed yet), a dialog box reports that the file is not recognized and asks whether the user wants to find a program that understands the file.</span></span> <span data-ttu-id="2ab14-109">Microsoft 會維護現有的重新導向服務，將使用者轉寄給廠商的網站，而這些網站可提供程式來瞭解檔案。</span><span class="sxs-lookup"><span data-stu-id="2ab14-109">Microsoft maintains an existing redirection service to forward users to vendors' Web sites that can supply the program to understand the file.</span></span> <span data-ttu-id="2ab14-110">這項功能存在於 Windows XP 和 Windows Vista 中。</span><span class="sxs-lookup"><span data-stu-id="2ab14-110">This facility exists in Windows XP and in Windows Vista.</span></span>
-   <span data-ttu-id="2ab14-111">Windows 影像中心、Windows Live 影像中心和 Windows 7 相片檢視器會將一組副檔名辨識為原始檔案。</span><span class="sxs-lookup"><span data-stu-id="2ab14-111">The Windows Photo Gallery, Windows Live Photo Gallery, and the Windows 7 Photo Viewer recognize a set of file extensions as RAW files.</span></span> <span data-ttu-id="2ab14-112">如果該集合中的檔案位於任何這些應用程式所查看的資料夾中，而且尚未安裝該檔案的編解碼器，則會出現一個對話方塊，如前面段落中所述。</span><span class="sxs-lookup"><span data-stu-id="2ab14-112">If files from that set are found in folders that any of these applications are looking at, and a codec for the file is not already installed, then a dialog box appears, as described in the preceding paragraph.</span></span>

<span data-ttu-id="2ab14-113">如需有關編解碼器探索的詳細資訊，請參閱編解碼器可用性和平臺支援。</span><span class="sxs-lookup"><span data-stu-id="2ab14-113">For more information about codec discovery, see Codec Availability and Platform Support.</span></span>

## <a name="windows-xp-platform-support"></a><span data-ttu-id="2ab14-114">Windows XP 平臺支援</span><span class="sxs-lookup"><span data-stu-id="2ab14-114">Windows XP Platform Support</span></span>

<span data-ttu-id="2ab14-115">Microsoft 已發行具有 WIC 的 Windows XP SP3，以及適用于 Windows XP SP2 的獨立 WIC 安裝程式。</span><span class="sxs-lookup"><span data-stu-id="2ab14-115">Microsoft has released Windows XP SP3 with WIC, and a standalone WIC installer for Windows XP SP2.</span></span> <span data-ttu-id="2ab14-116">這些會使用 WIC 編解碼器來啟用在這些平臺上的縮圖和預覽支援。</span><span class="sxs-lookup"><span data-stu-id="2ab14-116">These use WIC codecs to enable support for thumbnails and previews on those platforms.</span></span> <span data-ttu-id="2ab14-117">因此，在 Windows 7、Windows Vista 和 Windows XP 上支援和測試編解碼器下載和安裝是很重要的。</span><span class="sxs-lookup"><span data-stu-id="2ab14-117">Therefore, it is important that codec download and installation be supported and tested on the Windows 7, Windows Vista, and Windows XP.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ab14-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ab14-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2ab14-119">**概念**</span><span class="sxs-lookup"><span data-stu-id="2ab14-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2ab14-120">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="2ab14-120">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="2ab14-121">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="2ab14-121">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="2ab14-122">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="2ab14-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



