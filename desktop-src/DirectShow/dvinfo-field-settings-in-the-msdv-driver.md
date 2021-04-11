---
description: MSDV 驅動程式中的 DVINFO 欄位設定
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: MSDV 驅動程式中的 DVINFO 欄位設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4205a680833b0e2f8c6be2dc4cb65faa60515867
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688011"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a><span data-ttu-id="40826-103">MSDV 驅動程式中的 DVINFO 欄位設定</span><span class="sxs-lookup"><span data-stu-id="40826-103">DVINFO Field Settings in the MSDV Driver</span></span>

<span data-ttu-id="40826-104">本節說明 MSDV 驅動程式如何填入 [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) 結構。</span><span class="sxs-lookup"><span data-stu-id="40826-104">This section describes how the MSDV driver fills in the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) structure.</span></span>

<span data-ttu-id="40826-105">`DVINFO`結構會定義 MSDV 與其他篩選之間的 pin 連接格式區塊。</span><span class="sxs-lookup"><span data-stu-id="40826-105">The `DVINFO` structure defines the format block for pin connections between MSDV and other filters.</span></span> <span data-ttu-id="40826-106">根據預設，DV 分隔器篩選器會在從 DV 裝置進行捕捉時使用，而 DV Mux 篩選器則會在傳送至裝置時使用。</span><span class="sxs-lookup"><span data-stu-id="40826-106">By default, the DV Splitter filter is used when capturing from a DV device, and the DV Mux filter is used when transmitting to the device.</span></span> <span data-ttu-id="40826-107">不過，應用程式可能會提供自己的自訂篩選，因此瞭解 MSDV 如何填入格式區塊會很有用 `DVINFO` 。</span><span class="sxs-lookup"><span data-stu-id="40826-107">However, applications may provide their own custom filters, so it is useful to understand how MSDV populates the `DVINFO` format block.</span></span>

<span data-ttu-id="40826-108">`DVINFO`結構包含下列資訊：</span><span class="sxs-lookup"><span data-stu-id="40826-108">The `DVINFO` structure contains the following information:</span></span>

-   <span data-ttu-id="40826-109">針對第一個和第二個音訊區塊，兩個音訊輔助 (AAUX) 來源套件。</span><span class="sxs-lookup"><span data-stu-id="40826-109">Two audio auxiliary (AAUX) source packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="40826-110">第一個和第二個音訊區塊的兩個 AAUX 原始檔控制套件。</span><span class="sxs-lookup"><span data-stu-id="40826-110">Two AAUX source control packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="40826-111">影片輔助 (VAUX) 來源套件。</span><span class="sxs-lookup"><span data-stu-id="40826-111">A video auxiliary (VAUX) source pack.</span></span>
-   <span data-ttu-id="40826-112">VAUX 原始檔控制套件。</span><span class="sxs-lookup"><span data-stu-id="40826-112">A VAUX source control pack.</span></span>

<span data-ttu-id="40826-113">DV 串流中的每個畫面格都包含 AAUX 和 VAUX 套件。</span><span class="sxs-lookup"><span data-stu-id="40826-113">Every frame in a DV stream contains AAUX and VAUX packs.</span></span> <span data-ttu-id="40826-114">但是， `DVINFO` 格式區塊是靜態的，而且只會用來建立 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="40826-114">However, the `DVINFO` format block is static, and is only used to establish the pin connection.</span></span> <span data-ttu-id="40826-115">當 MSDV 驅動程式連接時，不會檢查資料流程中的任何 AAUX 或 VAUX 元件。</span><span class="sxs-lookup"><span data-stu-id="40826-115">When the MSDV driver connects, it does not examine any of the AAUX or VAUX packs in the stream.</span></span> <span data-ttu-id="40826-116">相反地，它會根據 DV 裝置的下列特性，使用一組預設值：</span><span class="sxs-lookup"><span data-stu-id="40826-116">Instead, it uses a set of default values, based on the following characteristics of the DV device:</span></span>

-   <span data-ttu-id="40826-117">裝置是否支援取用者格式 (DVCR) 或專業格式 (DVCPRO) </span><span class="sxs-lookup"><span data-stu-id="40826-117">Whether the device supports a consumer format (DVCR) or professional format (DVCPRO)</span></span>
-   <span data-ttu-id="40826-118">信號類型</span><span class="sxs-lookup"><span data-stu-id="40826-118">The signal type</span></span>
-   <span data-ttu-id="40826-119">格式是否為 NTSC 或 PAL。</span><span class="sxs-lookup"><span data-stu-id="40826-119">Whether the format is NTSC or PAL.</span></span> <span data-ttu-id="40826-120"> (如果裝置未報告此資訊，MSDV 預設為 NTSC 設定) </span><span class="sxs-lookup"><span data-stu-id="40826-120">(If the device does not report this information, MSDV defaults to the NTSC settings)</span></span>

<span data-ttu-id="40826-121">串流開始之後，使用者模式篩選器（例如 DV 分隔器）的責任就是檢查每個 DV 框架的實際內容。</span><span class="sxs-lookup"><span data-stu-id="40826-121">Once streaming begins, it is the responsibility of the user-mode filters, such as the DV Splitter, to examine the actual contents of each DV frame.</span></span> <span data-ttu-id="40826-122">因為資訊可以從框架變更為框架，所以篩選可能需要執行動態格式變更。</span><span class="sxs-lookup"><span data-stu-id="40826-122">Because the information can change from frame to frame, the filter may need to perform a dynamic format change.</span></span> <span data-ttu-id="40826-123">例如，如果音訊速率變更，則篩選可能需要重新協商音訊類型。</span><span class="sxs-lookup"><span data-stu-id="40826-123">For example, if the audio rate changes, the filter might need to renegotiate the audio type.</span></span>

<span data-ttu-id="40826-124">如果您捕捉型別1的 DV 檔案，此 `DVINFO` 結構會以資料流程格式寫入檔案中， ( ' strf ' ) 區塊。</span><span class="sxs-lookup"><span data-stu-id="40826-124">If you capture a type-1 DV file, the `DVINFO` structure is written into the file as the stream format ('strf') chunk.</span></span> <span data-ttu-id="40826-125">這項資料會直接取自 MSDV 所提供的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="40826-125">This data is taken directly from the format block provided by MSDV.</span></span> <span data-ttu-id="40826-126">如所述，資料流程的實際內容可能會不同。</span><span class="sxs-lookup"><span data-stu-id="40826-126">As noted, the actual content of the stream might be different.</span></span> <span data-ttu-id="40826-127">應用程式必須負責檢查每個畫面中的 AAUX 和 VAUX 套件。</span><span class="sxs-lookup"><span data-stu-id="40826-127">It is the application's responsibility to examine the AAUX and VAUX packs in each frame.</span></span>

<span data-ttu-id="40826-128">在下列主題中，您可以找到列出 MSDV 所使用之所有欄位的資料表。</span><span class="sxs-lookup"><span data-stu-id="40826-128">In the following topics, you can find tables listing all of the fields used by MSDV.</span></span>

-   [<span data-ttu-id="40826-129">AAUX 來源 (作為) 套件</span><span class="sxs-lookup"><span data-stu-id="40826-129">AAUX Source (AS) Pack</span></span>](aaux-source--as--pack.md)
-   [<span data-ttu-id="40826-130">AAUX 原始檔控制 (ASC) 套件</span><span class="sxs-lookup"><span data-stu-id="40826-130">AAUX Source Control (ASC) Pack</span></span>](aaux-source-control--asc--pack.md)
-   [<span data-ttu-id="40826-131">VAUX 來源 (VS) 套件</span><span class="sxs-lookup"><span data-stu-id="40826-131">VAUX Source (VS) Pack</span></span>](vaux-source--vs--pack.md)
-   [<span data-ttu-id="40826-132">VAUX 原始檔控制 (VSC) 套件</span><span class="sxs-lookup"><span data-stu-id="40826-132">VAUX Source Control (VSC) Pack</span></span>](vaux-source-control--vsc--pack.md)

<span data-ttu-id="40826-133">閱讀這些資料表時，請參閱下列規格：</span><span class="sxs-lookup"><span data-stu-id="40826-133">When reading these tables, please consult the following specifications:</span></span>

-   <span data-ttu-id="40826-134">IEC 61834</span><span class="sxs-lookup"><span data-stu-id="40826-134">IEC 61834</span></span>
-   <span data-ttu-id="40826-135">SMPTE 314M</span><span class="sxs-lookup"><span data-stu-id="40826-135">SMPTE 314M</span></span>
-   <span data-ttu-id="40826-136">SMPTE 370</span><span class="sxs-lookup"><span data-stu-id="40826-136">SMPTE 370</span></span>

<span data-ttu-id="40826-137">在每個資料表中，第一個資料行提供欄位碼，後面接著以括弧括住的 (位數) 。</span><span class="sxs-lookup"><span data-stu-id="40826-137">In each table, the first column gives the field code, followed by the number of bits (in parentheses).</span></span> <span data-ttu-id="40826-138">其餘的資料行則提供域值。</span><span class="sxs-lookup"><span data-stu-id="40826-138">The remaining columns give the field values.</span></span> <span data-ttu-id="40826-139">許多 AAUX 和 VAUX 欄位與 pin 連接無關，在這種情況下，MSDV 會設定虛擬值。</span><span class="sxs-lookup"><span data-stu-id="40826-139">Many of the AAUX and VAUX fields are not relevant for the pin connection, in which case MSDV sets a dummy value.</span></span> <span data-ttu-id="40826-140">整個套件的數值會列在每個資料表的底部。</span><span class="sxs-lookup"><span data-stu-id="40826-140">The numeric value of the entire pack is listed at the bottom of each table.</span></span>

<span data-ttu-id="40826-141">每個資料表之後的附注會提供有關所選欄位的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="40826-141">The notes after each table give more information about selected fields.</span></span> <span data-ttu-id="40826-142">如需完整的說明，請參閱規格。</span><span class="sxs-lookup"><span data-stu-id="40826-142">For complete descriptions, refer to the specifications.</span></span> <span data-ttu-id="40826-143">此外，在 SMPTE 314M/SMPTE 370 中，某些欄位的意義與 IEC 61834 中的意義不同。</span><span class="sxs-lookup"><span data-stu-id="40826-143">Also, some fields do not have the same meaning in SMPTE 314M/SMPTE 370 as they do in IEC 61834.</span></span>

> [!Note]  
> <span data-ttu-id="40826-144">DirectShow 目前不支援 DVCPRO 格式。</span><span class="sxs-lookup"><span data-stu-id="40826-144">Currently, DirectShow does not support DVCPRO formats.</span></span> <span data-ttu-id="40826-145">針對 DVCPRO 格式所列出的值會定義為供日後使用。</span><span class="sxs-lookup"><span data-stu-id="40826-145">The values listed for the DVCPRO formats are defined for future use.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="40826-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="40826-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40826-147">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="40826-147">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="40826-148">AVI 檔案格式的 DV 資料</span><span class="sxs-lookup"><span data-stu-id="40826-148">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[<span data-ttu-id="40826-149">MSDV 驅動程式</span><span class="sxs-lookup"><span data-stu-id="40826-149">MSDV Driver</span></span>](msdv-driver.md)
</dt> </dl>

 

 



