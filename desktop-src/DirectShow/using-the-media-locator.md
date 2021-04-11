---
description: 使用媒體定位器
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: 使用媒體定位器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce934b06d92c0bec66d9260a485516d3acaf5a9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945595"
---
# <a name="using-the-media-locator"></a><span data-ttu-id="3baaa-103">使用媒體定位器</span><span class="sxs-lookup"><span data-stu-id="3baaa-103">Using the Media Locator</span></span>

<span data-ttu-id="3baaa-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3baaa-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="3baaa-105">媒體定位器是一個協助程式物件，可驗證檔案名，並在本機或網路目錄上搜尋遺失的檔案。</span><span class="sxs-lookup"><span data-stu-id="3baaa-105">The media locator is a helper object that verifies file names and searches for missing files on local or network directories.</span></span> <span data-ttu-id="3baaa-106">媒體偵測器會保留目錄路徑的快取，其中已在過去搜尋中成功找到檔案。</span><span class="sxs-lookup"><span data-stu-id="3baaa-106">The media detector keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="3baaa-107">為了找出檔案，它會在其快取中搜尋目錄。</span><span class="sxs-lookup"><span data-stu-id="3baaa-107">To locate a file, it searches the directories in its cache.</span></span> <span data-ttu-id="3baaa-108">若失敗，媒體偵測器會顯示 [開啟檔案] 對話方塊，讓使用者以手動方式尋找檔案。</span><span class="sxs-lookup"><span data-stu-id="3baaa-108">Failing that, the media detector can display an Open File dialog for the user to locate a file manually.</span></span> <span data-ttu-id="3baaa-109">假設使用者找出檔案，則媒體定位器會將新的目錄新增至其快取。</span><span class="sxs-lookup"><span data-stu-id="3baaa-109">Assuming the user locates the file, the media locator adds the new directory to its cache.</span></span> <span data-ttu-id="3baaa-110">媒體定位器會公開 [**IMediaLocator**](imedialocator.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="3baaa-110">The media locator exposes the [**IMediaLocator**](imedialocator.md) interface.</span></span>

<span data-ttu-id="3baaa-111">一般來說，您的應用程式不會直接建立媒體定位器的實例。</span><span class="sxs-lookup"><span data-stu-id="3baaa-111">Typically, your application does not directly create an instance of the media locator.</span></span> <span data-ttu-id="3baaa-112">相反地，時間軸和轉譯引擎會提供下列方法，以使用媒體偵測器來驗證檔案名。</span><span class="sxs-lookup"><span data-stu-id="3baaa-112">Instead, the timeline and the render engine provide the following methods for validating file names using the media detector.</span></span>

-   <span data-ttu-id="3baaa-113">若要在時間軸中驗證檔案名，請呼叫 [**IAMTimeline：： ValidateSourceNames**](iamtimeline-validatesourcenames.md)。</span><span class="sxs-lookup"><span data-stu-id="3baaa-113">To validate file names in the timeline, call [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md).</span></span> <span data-ttu-id="3baaa-114">（選擇性）此方法也會使用正確的檔案名來更新來源物件。</span><span class="sxs-lookup"><span data-stu-id="3baaa-114">Optionally, this method also updates the source objects with the correct file names.</span></span>
-   <span data-ttu-id="3baaa-115">若要在轉譯專案時驗證檔案名，請呼叫 [**IRenderEngine：： SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)。</span><span class="sxs-lookup"><span data-stu-id="3baaa-115">To validate file names when the project is rendered, call [**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).</span></span>

<span data-ttu-id="3baaa-116">這兩種方法都採用旗標來控制媒體定位器的行為。</span><span class="sxs-lookup"><span data-stu-id="3baaa-116">Both methods take flags that control the behavior of the media locator.</span></span> <span data-ttu-id="3baaa-117">例如，您可以將搜尋限制為本機目錄。</span><span class="sxs-lookup"><span data-stu-id="3baaa-117">For example, you can restrict the search to local directories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3baaa-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="3baaa-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3baaa-119">使用來源</span><span class="sxs-lookup"><span data-stu-id="3baaa-119">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



