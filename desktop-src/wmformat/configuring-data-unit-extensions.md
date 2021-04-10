---
title: 設定資料單位延伸模組
description: 設定資料單位延伸模組
ms.assetid: 5dc0a596-68ae-409a-9abc-15ca507d6ec7
keywords:
- 資料流程，設定資料單位延伸模組
- 資料流程，資料單位延伸
- 資料單位延伸模組，設定
- 設定檔，資料單位延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7e6794b95128d180bc3922f9bf03a15a2749df
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "103681544"
---
# <a name="configuring-data-unit-extensions"></a><span data-ttu-id="203ce-107">設定資料單位延伸模組</span><span class="sxs-lookup"><span data-stu-id="203ce-107">Configuring Data Unit Extensions</span></span>

<span data-ttu-id="203ce-108">寫入至 ASF 檔案的範例可包含媒體範例本身以外的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="203ce-108">Samples written to ASF files can contain additional information apart from the media samples themselves.</span></span> <span data-ttu-id="203ce-109">這項資訊包含在使用資料單位延伸模組中。</span><span class="sxs-lookup"><span data-stu-id="203ce-109">This information is included using data unit extensions.</span></span> <span data-ttu-id="203ce-110">如需資料單位延伸的詳細資訊，請參閱 [資料單位延伸](data-unit-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="203ce-110">For more information about data unit extensions, see [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="203ce-111">若要使用資料單位延伸模組，您必須設定設定檔中的串流以接受這些延伸模組。</span><span class="sxs-lookup"><span data-stu-id="203ce-111">To use data unit extensions, you must configure the stream in the profile to accept them.</span></span> <span data-ttu-id="203ce-112">若要設定資料流程的資料單位延伸，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="203ce-112">To configure a data unit extension for a stream, perform the following steps.</span></span>

1.  <span data-ttu-id="203ce-113">藉由呼叫 [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)的 **QueryInterface** 方法，取得 [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="203ce-113">Obtain a pointer to the [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) interface by calling the **QueryInterface** method of [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span></span>
2.  <span data-ttu-id="203ce-114">呼叫 [**IWMStreamConfig2：： AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) 來註冊資料流程的資料單位延伸模組類型。</span><span class="sxs-lookup"><span data-stu-id="203ce-114">Call [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) to register a type of data unit extension for the stream.</span></span>

<span data-ttu-id="203ce-115">您可以藉由呼叫 [**IWMStreamConfig2：： GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) 來取得已註冊之資料單位延伸模組類型的數目，來檢查目前為數據流註冊的所有資料單位延伸模組類型。</span><span class="sxs-lookup"><span data-stu-id="203ce-115">You can examine all of the data unit extension types currently registered for a stream by calling [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) to retrieve the number of registered data unit extension types.</span></span> <span data-ttu-id="203ce-116">然後，您可以使用 [**IWMStreamConfig2：： GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) 的呼叫，逐一執行所有類型的迴圈。</span><span class="sxs-lookup"><span data-stu-id="203ce-116">Then you can loop through all of the types using calls to [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) for each.</span></span>

<span data-ttu-id="203ce-117">設定資料流程時，會為數據單位延伸模組指派大小。</span><span class="sxs-lookup"><span data-stu-id="203ce-117">Data unit extensions are assigned a size when configured for a stream.</span></span> <span data-ttu-id="203ce-118">許多資料單位延伸系統都使用固定大小的資料， (通常是結構) 。</span><span class="sxs-lookup"><span data-stu-id="203ce-118">Many data unit extension systems use data that is a constant size (usually a structure).</span></span> <span data-ttu-id="203ce-119">不過，您也可以藉由將大小設定為0xFFFF，將資料單位延伸模組設定為變數大小。</span><span class="sxs-lookup"><span data-stu-id="203ce-119">However, you can also configure your data unit extensions to be of variable size by setting the size to 0xFFFF.</span></span> <span data-ttu-id="203ce-120">在編碼時間指派的每個資料單位延伸可以是1個位元組到65534個位元組之間的任何大小。</span><span class="sxs-lookup"><span data-stu-id="203ce-120">Each data unit extension assigned at encoding time can then be of any size between 1 byte and 65534 bytes.</span></span> <span data-ttu-id="203ce-121">大小可變大小的資料單位延伸也稱為動態資料單位延伸模組。</span><span class="sxs-lookup"><span data-stu-id="203ce-121">Variably sized data unit extensions are also called dynamic data unit extensions.</span></span>

<span data-ttu-id="203ce-122">使用動態資料單位延伸的優點是您可以視需要附加擴充功能資料。</span><span class="sxs-lookup"><span data-stu-id="203ce-122">The advantage of using dynamic data unit extensions is that you can attach extension data as needed.</span></span> <span data-ttu-id="203ce-123">如果您定義具有設定大小的資料單位延伸，則資料流程的每個範例都必須包含該大小的延伸資料，即使您沒有一些範例的資料。</span><span class="sxs-lookup"><span data-stu-id="203ce-123">If you define a data unit extension with a set size, every sample for the stream must contain extension data of that size, even if you have no data for some samples.</span></span> <span data-ttu-id="203ce-124">使用動態資料單位延伸模組時，您可以省略一些範例中的資料單位延伸模組，以節省空間並減少頻寬需求。</span><span class="sxs-lookup"><span data-stu-id="203ce-124">With dynamic data unit extensions, you can omit data unit extensions from some samples, which saves space and reduces bandwidth requirements.</span></span> <span data-ttu-id="203ce-125">但是，如果資料單位延伸是變數大小，讀取物件就無法針對靜態大小驗證接收的延伸資料。</span><span class="sxs-lookup"><span data-stu-id="203ce-125">However, if data unit extensions are of variable size, the reading object cannot verify the received extension data against a static size.</span></span> <span data-ttu-id="203ce-126">您必須確認您收到的延伸模組資料是有效的，而不是位資料流程的惡意失真。</span><span class="sxs-lookup"><span data-stu-id="203ce-126">You must verify that the extension data that you receive is valid, and not malicious distortion of the bit stream.</span></span>

<span data-ttu-id="203ce-127">您必須使用 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 方法，在範例上設定個別的資料單位延伸。</span><span class="sxs-lookup"><span data-stu-id="203ce-127">Individual data unit extensions must be set on samples by using the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="203ce-128">如需詳細資訊，請參閱 [設定資料單位延伸](setting-data-unit-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="203ce-128">For more information, see [Setting Data Unit Extensions](setting-data-unit-extensions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="203ce-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="203ce-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="203ce-130">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="203ce-130">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




