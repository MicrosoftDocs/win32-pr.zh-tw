---
title: 設定中繼資料屬性
description: 設定中繼資料屬性
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows Media 格式 SDK，設定中繼資料屬性
- Advanced Systems Format (ASF) ，設定中繼資料屬性
- ASF (Advanced Systems Format) ，設定中繼資料屬性
- 中繼資料，設定屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374526"
---
# <a name="setting-metadata-attributes"></a><span data-ttu-id="a70c4-107">設定中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="a70c4-107">Setting Metadata Attributes</span></span>

<span data-ttu-id="a70c4-108">中繼資料屬性是使用 [**IWMHeaderInfo3：： AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) 方法所設定。</span><span class="sxs-lookup"><span data-stu-id="a70c4-108">Metadata attributes are set by using the [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) method.</span></span>

<span data-ttu-id="a70c4-109">所有屬性都是從檔案的語言清單中指派語言。</span><span class="sxs-lookup"><span data-stu-id="a70c4-109">All attributes are assigned a language from the language list for the file.</span></span> <span data-ttu-id="a70c4-110">您可以使用 [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) 介面來存取語言清單。</span><span class="sxs-lookup"><span data-stu-id="a70c4-110">You can access the language list by using the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface.</span></span> <span data-ttu-id="a70c4-111">若要取得 **IWMLanguageList** 介面的指標，請在您取得 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)之物件的任何介面上呼叫 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="a70c4-111">To get a pointer to an **IWMLanguageList** interface, call **QueryInterface** on any interface of the object from which you have obtained [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).</span></span>

<span data-ttu-id="a70c4-112">您可以使用任何想要的名稱來新增屬性。</span><span class="sxs-lookup"><span data-stu-id="a70c4-112">You can add attributes with any name you like.</span></span> <span data-ttu-id="a70c4-113">不過，使用 Windows Media 格式 SDK 所支援之非標準名稱的屬性名稱，可能會讓使用者難以探索您的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a70c4-113">However, using attribute names that are not standard names supported by the Windows Media Format SDK can make your metadata difficult for users to discover.</span></span> <span data-ttu-id="a70c4-114">大部分的媒體播放應用程式都會檢查標準值。</span><span class="sxs-lookup"><span data-stu-id="a70c4-114">Most media-playing applications will check for standard values.</span></span> <span data-ttu-id="a70c4-115">如需詳細資訊，請參閱 [自訂中繼資料](custom-metadata.md)。</span><span class="sxs-lookup"><span data-stu-id="a70c4-115">For more information, see [Custom Metadata](custom-metadata.md).</span></span>

<span data-ttu-id="a70c4-116">您無法使用 stream number 0xFFFF 來全域加入屬性。</span><span class="sxs-lookup"><span data-stu-id="a70c4-116">You cannot use stream number 0xFFFF to add an attribute globally.</span></span> <span data-ttu-id="a70c4-117">您必須將每個屬性指派給特定的資料流程號碼，或指派給檔案層級屬性的資料流程0。</span><span class="sxs-lookup"><span data-stu-id="a70c4-117">You must assign each attribute to a specific stream number, or stream 0 for file-level attributes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a70c4-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="a70c4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a70c4-119">**使用中繼資料**</span><span class="sxs-lookup"><span data-stu-id="a70c4-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




