---
title: IMAPI.EXE 多會話配置
description: IMAPI.EXE 讓應用程式開發人員能夠建立 ISO 9660 和 UDF 檔案系統映射，並將它們燒錄到 CD、DVD 和 Blu-Ray \ 8482;光學媒體。
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2581672fac78d23a0d2f4e2bc36ee4227adbca1d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "104566163"
---
# <a name="imapi-multisession-layout"></a><span data-ttu-id="2d93a-103">IMAPI.EXE 多會話配置</span><span class="sxs-lookup"><span data-stu-id="2d93a-103">IMAPI Multisession Layout</span></span>

<span data-ttu-id="2d93a-104">IMAPI.EXE 讓應用程式開發人員能夠建立 ISO 9660 和 UDF 檔案系統映射，並將它們燒錄到 CD、DVD 和藍光™光學媒體上。</span><span class="sxs-lookup"><span data-stu-id="2d93a-104">IMAPI provides application developers with the ability to create ISO 9660 and UDF file system images and burn them onto CD, DVD and Blu-Ray™ optical media.</span></span> <span data-ttu-id="2d93a-105">在 Windows 7 中，IMAPI.EXE 提供對 DVD 和藍光™可讀寫媒體上的多會話燒錄的額外支援。</span><span class="sxs-lookup"><span data-stu-id="2d93a-105">With Windows 7, IMAPI provides additional support for multisession burning on DVD and Blu-Ray™ rewritable media.</span></span>

<span data-ttu-id="2d93a-106">下列檔詳細說明 IMAPI.EXE 利用來執行多會話的光碟版面配置。</span><span class="sxs-lookup"><span data-stu-id="2d93a-106">The following documentation details the disc layout that IMAPI utilizes to implement multisession.</span></span> <span data-ttu-id="2d93a-107">這項資訊應該用來確保 IMAPI.EXE 與其他燒錄軟體之間的互通性，以及允許此軟體的開發人員建立與 IMAPI.EXE 相容的多會話光碟映射。</span><span class="sxs-lookup"><span data-stu-id="2d93a-107">This information should be used to ensure interoperability between IMAPI and other burning software as well as allow the developers of this software to create IMAPI-compatible multisession disc images.</span></span>

> [!Note]  
> <span data-ttu-id="2d93a-108">如需詳細說明如何建立多個多會話光碟的範例，請參閱 [建立多會話光碟](creating-a-multisession-disc.md)。</span><span class="sxs-lookup"><span data-stu-id="2d93a-108">For an example detailing the creation of a multisession disc, see [Creating a Multisession Disc](creating-a-multisession-disc.md).</span></span>

 

## <a name="multisession-on-sequential-media"></a><span data-ttu-id="2d93a-109">連續媒體上的多會話</span><span class="sxs-lookup"><span data-stu-id="2d93a-109">Multisession on Sequential Media</span></span>

<span data-ttu-id="2d93a-110">連續媒體上的多會話的 IMAPI.EXE 執行支援與 CD-R、CD-RW、DVD-R、DVD + R 和藍光™媒體搭配使用。</span><span class="sxs-lookup"><span data-stu-id="2d93a-110">The IMAPI implementation of multisession on sequential media is supported for use with CD-R, CD-RW, DVD-R, DVD+R and Blu-Ray™ media.</span></span> <span data-ttu-id="2d93a-111">IMAPI.EXE 會使用一次會話記錄模式進行 CD-RW，因此在此案例中，格式會視為連續的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="2d93a-111">IMAPI uses the Session-At-Once recording mode for CD-RW, and as a result, in this scenario, the format is considered a sequential media type.</span></span>

<span data-ttu-id="2d93a-112">在使用 UDF 的連續媒體的多重會話案例中，IMAPI.EXE 會寫出錨點結構 (UDF 錨點磁片區描述元指標-AVDP) 、磁片區結構 (UDF 磁片區描述項順序-VDS) ，以及檔案系統元資料結構 (UDF 檔案集描述項-FSD) 在每個新會話開始時，如下圖所述：</span><span class="sxs-lookup"><span data-stu-id="2d93a-112">In a scenario involving multisession on sequential media using UDF, IMAPI writes out the anchor structures (UDF Anchor Volume Descriptor Pointer - AVDP), volume structures (UDF Volume Descriptor Sequence - VDS) , and the file system metadata structures (UDF File Set Descriptor - FSD) at the start of every new session as outlined in the following diagram:</span></span>

![顯示具有「匯入/F S 掛接點」的檔案系統元資料結構的圖表，其在實體會話2的「錨點」以紅色箭號表示。](images/multises1.png)

> [!Note]  
> <span data-ttu-id="2d93a-114">此圖說明使用 UDF 2.50 搭配重複中繼資料時的 IMAPI.EXE 光碟版面配置。</span><span class="sxs-lookup"><span data-stu-id="2d93a-114">This figure illustrates the IMAPI disc layout when using UDF 2.50 with redundant metadata.</span></span>

 

<span data-ttu-id="2d93a-115">依序錄製的媒體上儲存的資料是由一些實體會話所組成。</span><span class="sxs-lookup"><span data-stu-id="2d93a-115">The data stored on sequentially recorded media consists of a number of physical sessions.</span></span> <span data-ttu-id="2d93a-116">每個會話都包含一個完整的檔案系統，將使用者資料表示為一組以目錄組織的檔案。</span><span class="sxs-lookup"><span data-stu-id="2d93a-116">Each session contains a complete file system representing user data as a set of files organized in directories.</span></span> <span data-ttu-id="2d93a-117">檔案系統中繼資料包含許多階層式組織的資料結構。</span><span class="sxs-lookup"><span data-stu-id="2d93a-117">The file system metadata consists of a number of hierarchically organized data structures.</span></span> <span data-ttu-id="2d93a-118">階層的頂端會有錨點結構 (AVDP) 位於預先定義的邏輯區塊位址 (LBAs) 。</span><span class="sxs-lookup"><span data-stu-id="2d93a-118">At the top of the hierarchy reside anchor structures (AVDP) located at pre-defined Logical Block Addresses (LBAs).</span></span> <span data-ttu-id="2d93a-119">錨點結構會指定沒有預先定義之位址的下一個層級結構的位置。</span><span class="sxs-lookup"><span data-stu-id="2d93a-119">The anchor structures specify the locations of the next level structures which do not have predefined addresses.</span></span> <span data-ttu-id="2d93a-120">錨點結構之後的下一個階層層級包含磁片區結構 (VDS) 描述磁片區的屬性，並參考檔案系統元資料結構 (FSD) ，進而描述個別的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="2d93a-120">The next level of hierarchy after anchor structures contains the volume structures (VDS) that describe the properties of the volume and referencing the file system metadata structures (FSD), which in turn describe individual files and directories.</span></span>

## <a name="multisession-on-rewritable-media"></a><span data-ttu-id="2d93a-121">可讀寫媒體上的多會話</span><span class="sxs-lookup"><span data-stu-id="2d93a-121">Multisession on Rewritable Media</span></span>

<span data-ttu-id="2d93a-122">上一節所述之順序媒體的方法與可讀寫 (非順序) 媒體不相容。</span><span class="sxs-lookup"><span data-stu-id="2d93a-122">The approach for sequential media outlined in the previous section is incompatible with rewritable (non-sequential) media.</span></span> <span data-ttu-id="2d93a-123">這些媒體格式包括 DVD-ROM、DVD + RW、DVD RAM、藍光™可讀寫，以及其他隨機寫入媒體，例如 Iomega REV 磁片。</span><span class="sxs-lookup"><span data-stu-id="2d93a-123">These media formats include DVD-RW, DVD+RW, DVD-RAM, Blu-Ray™ rewritable and other random writable media, such as Iomega REV disks.</span></span> <span data-ttu-id="2d93a-124">可讀寫媒體不支援對應至邏輯會話的實體會話概念，也就是由主控應用程式所認可的個別增量。</span><span class="sxs-lookup"><span data-stu-id="2d93a-124">Rewritable media does not support the concept of physical sessions corresponding to logical sessions, which are individual increments committed by a mastering application.</span></span> <span data-ttu-id="2d93a-125">只會公開單一實體會話，這是從光碟開頭開始的區域，代表可能包含多個邏輯會話的整個可定址區域。</span><span class="sxs-lookup"><span data-stu-id="2d93a-125">Only a single physical session is exposed, which is an area starting at the beginning of the disc representing the entire addressable area that has the potential to contain multiple logical sessions.</span></span>

> [!Note]  
> <span data-ttu-id="2d93a-126">雖然 CD-RW 是在連續模式下支援實體會話的概念，但 IMAPI.EXE 目前並不支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="2d93a-126">While DVD-RW is an exception in that it supports the concept of a physical session in the Sequential mode, this capability is currently not supported by IMAPI.</span></span>

 

<span data-ttu-id="2d93a-127">為了因應可讀寫格式的實體和邏輯會話之間缺乏一對一的對應，IMAPI.EXE 選擇性地更新 *第一個* 邏輯會話中的錨定結構 (AVDP) ，以指向 *最後一個* 邏輯會話的新磁片區結構 (VDS) 和檔案系統元資料結構 (FSD) ，如下圖所述：</span><span class="sxs-lookup"><span data-stu-id="2d93a-127">To address the lack of one-to-one mapping between physical and logical sessions on rewritable formats, IMAPI selectively updates the anchor structures (AVDP) in the *first* logical session to point to the new volume structures (VDS) and file system metadata structures (FSD) at the beginning of the *last* logical session as outlined in the following diagram:</span></span>

![此圖顯示具有「匯入/F S 掛接點」的檔案系統元資料結構，並在邏輯會話1的「錨點」處以紅色箭號表示。](images/multises2.png)

> [!Note]  
> <span data-ttu-id="2d93a-129">此圖說明使用 UDF 2.50 搭配重複中繼資料時的 IMAPI.EXE 光碟版面配置。</span><span class="sxs-lookup"><span data-stu-id="2d93a-129">This figure illustrates the IMAPI disc layout when using UDF 2.50 with redundant metadata.</span></span>

 

<span data-ttu-id="2d93a-130">將新的邏輯會話新增到可讀寫光碟時，IMAPI.EXE 會先分析磁片區中繼資料 (VDS) ，判斷最後一個邏輯會話的結尾。</span><span class="sxs-lookup"><span data-stu-id="2d93a-130">When adding a new logical session to a rewritable disc, IMAPI first determines the end of the last logical session by analyzing the volume metadata (VDS).</span></span> <span data-ttu-id="2d93a-131">然後，IMAPI.EXE 會新增邏輯會話、完成新的錨點 (AVDP) 、磁片區 (VDS) 以及檔案系統元資料結構 (FSD) ，與先前錄製的邏輯會話實際上是連續的。</span><span class="sxs-lookup"><span data-stu-id="2d93a-131">IMAPI then adds the new logical session, complete with new anchor (AVDP), volume (VDS) and file system metadata structures (FSD), physically contiguous with the previously recorded logical session.</span></span> <span data-ttu-id="2d93a-132">最後一個步驟需要更新第一個邏輯會話開頭的錨定結構 (AVDP) ，以指向 *新* 邏輯會話中 (VDS) 的磁片區結構。</span><span class="sxs-lookup"><span data-stu-id="2d93a-132">The final step requires that the anchor structures (AVDP) at the beginning of the first logical session are updated to point to the volume structures (VDS) in the *new* logical session.</span></span> <span data-ttu-id="2d93a-133">操作結果與順序媒體相同。</span><span class="sxs-lookup"><span data-stu-id="2d93a-133">The operational result is the same as with sequential media.</span></span>

## <a name="additional-recommendations"></a><span data-ttu-id="2d93a-134">其他建議</span><span class="sxs-lookup"><span data-stu-id="2d93a-134">Additional Recommendations</span></span>

-   <span data-ttu-id="2d93a-135">**分割區版面配置**</span><span class="sxs-lookup"><span data-stu-id="2d93a-135">**Partition Layout**</span></span>

    <span data-ttu-id="2d93a-136">為了達成 IMAPI.EXE 的相容性，建議協力廠商的燒錄軟體發展人員使用本檔中所述的光碟版面配置。</span><span class="sxs-lookup"><span data-stu-id="2d93a-136">To achieve IMAPI compatiblity, it is recommended that third-party burning software developers use the disc layouts outlined in this documentation.</span></span> <span data-ttu-id="2d93a-137">開發人員應避免配置檔案系統分割區佔用整個光碟，因為這需要記錄應用程式，以便在需要將資料附加到光碟時，找出現有磁碟分割內的可用空間。記錄應用程式通常會利用光碟上的專屬標記來完成這項作業，以指出使用者資料實際佔用多少空間。</span><span class="sxs-lookup"><span data-stu-id="2d93a-137">Developers should avoid layouts with file system partitions occupying the entire disc, as this requires recording applications to locate free space within existing partitions whenever data needs to be appended to the disc. Oftentimes, the recording applications accomplish this by utilizing proprietary markers on the disc to indicate how much space is actually occupied by user data.</span></span> <span data-ttu-id="2d93a-138">這類光碟版面配置與 IMAPI.EXE 不相容，因為無法在建立專屬標記的應用程式之外辨識這些標記。</span><span class="sxs-lookup"><span data-stu-id="2d93a-138">Such disc layouts are incompatible with IMAPI as the proprietary markers are not recognized outside of the application they were created for.</span></span>

-   <span data-ttu-id="2d93a-139">**UDF 磁碟分割類型**</span><span class="sxs-lookup"><span data-stu-id="2d93a-139">**UDF Partition Type**</span></span>

    <span data-ttu-id="2d93a-140">IMAPI.EXE 會在可寫入的媒體上，使用 **唯讀** UDF 磁碟分割類型來執行多會話。</span><span class="sxs-lookup"><span data-stu-id="2d93a-140">IMAPI uses the **Read-Only** UDF partition type in its implementation of multisession on rewritable media.</span></span> <span data-ttu-id="2d93a-141">協力廠商燒錄軟體的開發人員應該使用 **唯讀** UDF 磁碟分割類型，透過 Imapi.exe 達成 Windows 主要燒錄的相容性。</span><span class="sxs-lookup"><span data-stu-id="2d93a-141">Developers of third-party burning software should use the **Read-Only** UDF partition type to achieve compatiblity with Windows mastered burning via IMAPI.</span></span> <span data-ttu-id="2d93a-142">如果使用另一個 UDF 分割類型，例如可重 **寫** ，則 imapi.exe 無法提供主控支援。</span><span class="sxs-lookup"><span data-stu-id="2d93a-142">If another UDF partition type such as **Rewritable** is used, IMAPI cannot provide mastering support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d93a-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d93a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d93a-144">建立多會話光碟</span><span class="sxs-lookup"><span data-stu-id="2d93a-144">Creating a Multisession Disc</span></span>](creating-a-multisession-disc.md)
</dt> <dt>

[<span data-ttu-id="2d93a-145">**IMultisessionRandomWrite**</span><span class="sxs-lookup"><span data-stu-id="2d93a-145">**IMultisessionRandomWrite**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




