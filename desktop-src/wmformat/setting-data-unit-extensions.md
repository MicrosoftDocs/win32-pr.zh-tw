---
title: 設定資料單位延伸模組
description: 設定資料單位延伸模組
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- Advanced Systems Format (ASF) 、資料單位延伸模組
- ASF (Advanced Systems Format) 、資料單位延伸模組
- 資料單位延伸模組，設定
- 資料流程，資料單位延伸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a05a6e6bcbb9f0101d32eed05f2b6c5c68dc8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104507832"
---
# <a name="setting-data-unit-extensions"></a><span data-ttu-id="a1ee9-107">設定資料單位延伸模組</span><span class="sxs-lookup"><span data-stu-id="a1ee9-107">Setting Data Unit Extensions</span></span>

<span data-ttu-id="a1ee9-108">某些串流會設定為使用資料單位延伸模組，將補充資料與個別範例產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a1ee9-108">Some streams are configured to use data unit extensions to associate supplementary data with individual samples.</span></span> <span data-ttu-id="a1ee9-109">如需擴充範例的詳細資訊，請參閱 [資料單位延伸](data-unit-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="a1ee9-109">For more information about extended samples, see [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="a1ee9-110">大部分的資料單位延伸系統都需要在資料流程中的每個範例上有一個延伸模組。</span><span class="sxs-lookup"><span data-stu-id="a1ee9-110">Most data unit extension systems require an extension on every sample in the stream.</span></span> <span data-ttu-id="a1ee9-111">如果您未提供正確大小的延伸，寫入器將會拒絕範例。</span><span class="sxs-lookup"><span data-stu-id="a1ee9-111">If you do not provide an extension of the correct size, the writer will reject the sample.</span></span>

<span data-ttu-id="a1ee9-112">若要將擴充資料加入至範例，請使用 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 方法。</span><span class="sxs-lookup"><span data-stu-id="a1ee9-112">To add extended data to a sample, use the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="a1ee9-113">您可以使用 [**IWMStreamConfig2：： GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) 和 [**IWMStreamConfig2：： GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) 方法，取得有關資料流程上所設定之資料單位延伸模組的資訊。</span><span class="sxs-lookup"><span data-stu-id="a1ee9-113">You can get information about the data unit extensions configured on a stream by using the [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) and [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1ee9-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="a1ee9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1ee9-115">**設定資料單位延伸模組**</span><span class="sxs-lookup"><span data-stu-id="a1ee9-115">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="a1ee9-116">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="a1ee9-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




