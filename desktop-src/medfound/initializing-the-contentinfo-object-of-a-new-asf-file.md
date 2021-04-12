---
description: 初始化新 ASF 檔案的 ContentInfo 物件
ms.assetid: a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a
title: 初始化新 ASF 檔案的 ContentInfo 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74826942700f4be8028075fcd9466414834eb8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318308"
---
# <a name="initializing-the-contentinfo-object-of-a-new-asf-file"></a><span data-ttu-id="b2475-103">初始化新 ASF 檔案的 ContentInfo 物件</span><span class="sxs-lookup"><span data-stu-id="b2475-103">Initializing the ContentInfo Object of a New ASF File</span></span>

<span data-ttu-id="b2475-104">藉由呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 函式來建立空的 ContentInfo 物件之後，應用程式必須呼叫 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) 以提供編碼設定檔。</span><span class="sxs-lookup"><span data-stu-id="b2475-104">After creating an empty ContentInfo object by calling the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function, the application must call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to provide the encoding profile.</span></span> <span data-ttu-id="b2475-105">如需建立設定檔的詳細資訊，請參閱 [建立 ASF 設定檔](creating-an-asf-profile.md)。</span><span class="sxs-lookup"><span data-stu-id="b2475-105">For information about creating a profile, see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>

<span data-ttu-id="b2475-106">從設定檔讀取資訊之前， **SetProfile** 方法必須藉由檢查資料流程識別碼或媒體類型來驗證指定的設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="b2475-106">Before information can be read from the profile, the **SetProfile** method must validate the specified profile object by checking the stream identifiers or media types.</span></span> <span data-ttu-id="b2475-107">如果設定檔通過驗證，則會產生不同的標頭物件，例如檔案屬性物件、資料流程位元速率屬性物件、資料流程屬性物件，以及相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="b2475-107">If the profile passes the validation, various header objects are generated, such as the File Properties Object, the Stream Bitrate Properties Object, the Stream Properties Object, and the Mutual Exclusion Object.</span></span>

<span data-ttu-id="b2475-108">**SetProfile** 會計算並設定某些屬性的建議值，例如預先設定的值。</span><span class="sxs-lookup"><span data-stu-id="b2475-108">**SetProfile** computes and sets recommended values for certain properties, such as the preroll value.</span></span> <span data-ttu-id="b2475-109">如果尚未設定此值，建議的預先計算值（以毫秒為單位）取決於設定檔中針對資料流程所指定之有漏洞 bucket 的最大緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="b2475-109">If this is not already set, the recommended preroll value in milliseconds depends on the maximum buffer window of the leaky bucket specified for the streams in the profile.</span></span> <span data-ttu-id="b2475-110">同樣地，也會設定最小和最大的資料封包大小。</span><span class="sxs-lookup"><span data-stu-id="b2475-110">Similarly, the minimum and maximum data packet sizes are also set.</span></span> <span data-ttu-id="b2475-111">建議的值可能會覆寫透過屬性在設定檔上設定的封包大小。</span><span class="sxs-lookup"><span data-stu-id="b2475-111">The recommended values might override the packet sizes that are set on the profile through attributes.</span></span>

<span data-ttu-id="b2475-112">因為檔案正在建立中，所以檔案會分類為廣播類型，並以檔案屬性物件的 [旗標] 欄位表示。</span><span class="sxs-lookup"><span data-stu-id="b2475-112">Because the file is in the process of being created, the file is categorized as a broadcast type, which is denoted by the Flags field of the File Properties Object.</span></span> <span data-ttu-id="b2475-113">某些未知值（例如資料封包數、播放持續時間和傳送持續時間）會設定為零。</span><span class="sxs-lookup"><span data-stu-id="b2475-113">Certain unknown values such as the number of data packets, play duration, and send duration are set to zero.</span></span> <span data-ttu-id="b2475-114">這些值是由 **MF \_ PD \_ ASF \_ xxx** 屬性工作表示，而且必須在檔案建立完成之後，由應用程式更新。</span><span class="sxs-lookup"><span data-stu-id="b2475-114">These values are represented by **MF\_PD\_ASF\_xxx** attributes and must be updated by the application after file creation is complete.</span></span>

<span data-ttu-id="b2475-115">指定的設定檔物件會取代任何與 ContentInfo 物件相關聯的現有設定檔、移除參考的標頭物件，以及重設通用檔案屬性，例如預先處理和資料封包大小。</span><span class="sxs-lookup"><span data-stu-id="b2475-115">The specified profile object replaces any existing profile associated with the ContentInfo object, removes the referenced header objects, and resets global file properties such as preroll and data packet size.</span></span>

<span data-ttu-id="b2475-116">**SetProfile** 方法也會建立代表 ASF 資料物件的資料物件。</span><span class="sxs-lookup"><span data-stu-id="b2475-116">The **SetProfile** method also creates the data object that represents the ASF Data Object.</span></span> <span data-ttu-id="b2475-117">如果您重複使用 ContentInfo 物件，其中包含任何資料封包的相關資訊，則 **SetProfile** 會失敗，並傳回 MF \_ E \_ 已 \_ 初始化的錯誤，指出它已與現有的 ASF 資料物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="b2475-117">If you reuse a ContentInfo object that includes information about any data packets, **SetProfile** fails and returns the MF\_E\_ALREADY\_INITIALIZED error indicating that it is already associated with an existing ASF Data Object.</span></span> <span data-ttu-id="b2475-118">根據預設，對於新的 ContentInfo 物件，資料封包計數會設定為零，而且資料物件大小會設定為50個位元組。</span><span class="sxs-lookup"><span data-stu-id="b2475-118">By default, for a new ContentInfo object, the data packet count is set to zero and the data object size is set to 50 bytes.</span></span> <span data-ttu-id="b2475-119">如果您使用多工器來產生資料封包，則多工器會更新 ContentInfo 物件，以反映新的值，例如資料封包計數。</span><span class="sxs-lookup"><span data-stu-id="b2475-119">If you use the multiplexer to generate data packets, the multiplexer updates the ContentInfo object to reflect new values such as the data packet count.</span></span> <span data-ttu-id="b2475-120">如需有關產生資料封包的詳細資訊，請參閱 [產生新的 ASF 資料封包](generating-new-asf-data-packets.md)。</span><span class="sxs-lookup"><span data-stu-id="b2475-120">For more information about data packet generation, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

<span data-ttu-id="b2475-121">將所有的標頭物件加入到最後一個 ASF 標頭物件之後，就可以藉由呼叫 [**IMFASFContentInfo：： GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize)來取出總標頭大小。</span><span class="sxs-lookup"><span data-stu-id="b2475-121">After all the Header Objects are added to the final ASF Header Object, the total header size can be retrieved by calling [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize).</span></span> <span data-ttu-id="b2475-122">此大小包含初始資料物件大小。</span><span class="sxs-lookup"><span data-stu-id="b2475-122">This size includes the initial data object size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2475-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2475-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2475-124">在 ContentInfo 物件中設定屬性</span><span class="sxs-lookup"><span data-stu-id="b2475-124">Setting Properties in the ContentInfo Object</span></span>](setting-properties-in-the-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="b2475-125">為新檔案撰寫 ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="b2475-125">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



