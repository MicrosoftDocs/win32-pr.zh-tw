---
title: 若要設定輸入設定
description: 若要設定輸入設定
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- Advanced Systems Format (ASF) ，輸入設定
- ASF (Advanced Systems Format) ，輸入設定
- 設定檔，輸入設定
- 編解碼器，輸入設定
- 資料流程，輸入設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7b2db64a7346cc8b9d46c48f0add79dafcac95
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932941"
---
# <a name="to-set-input-settings"></a><span data-ttu-id="2044e-108">若要設定輸入設定</span><span class="sxs-lookup"><span data-stu-id="2044e-108">To Set Input Settings</span></span>

<span data-ttu-id="2044e-109">輸入媒體和串流媒體的基本屬性是由 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構所定義。</span><span class="sxs-lookup"><span data-stu-id="2044e-109">The basic properties of input media and stream media are defined by the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="2044e-110">針對輸入格式，媒體類型資訊是由您的應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="2044e-110">For input formats, the media type information is set by your application.</span></span> <span data-ttu-id="2044e-111">針對串流格式，媒體類型資訊會在您指派給寫入器的設定檔中設定。</span><span class="sxs-lookup"><span data-stu-id="2044e-111">For stream formats, the media type information is set in the profile you assign to the writer.</span></span> <span data-ttu-id="2044e-112">有些屬性與媒體類型無關，而且必須在寫入開始之前為輸入設定。</span><span class="sxs-lookup"><span data-stu-id="2044e-112">Some properties are independent of media type and must be set for an input before writing begins.</span></span> <span data-ttu-id="2044e-113">這些屬性是獨立于資料流程類型的編解碼器和寫入器功能，而且必須在寫入器中指派設定檔之後，但在寫入開始之前設定。</span><span class="sxs-lookup"><span data-stu-id="2044e-113">These properties are codec and writer features that are independent of stream type, and must be set after the profile is assigned in the writer but before writing begins.</span></span>

<span data-ttu-id="2044e-114">設定輸入設定需要呼叫 [**IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)。</span><span class="sxs-lookup"><span data-stu-id="2044e-114">Setting an input setting requires a call to [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="2044e-115">您也可以使用 [**IWMWriterAdvanced2：： GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)的呼叫來檢查設定的目前值。</span><span class="sxs-lookup"><span data-stu-id="2044e-115">You can also check the current value of a setting with a call to [**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2044e-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="2044e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2044e-117">**將設定檔與寫入器搭配使用**</span><span class="sxs-lookup"><span data-stu-id="2044e-117">**To Use Profiles with the Writer**</span></span>](to-use-profiles-with-the-writer.md)
</dt> <dt>

[<span data-ttu-id="2044e-118">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="2044e-118">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> <dt>

[<span data-ttu-id="2044e-119">**寫入影像資料流程**</span><span class="sxs-lookup"><span data-stu-id="2044e-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




