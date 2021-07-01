---
title: 映射主控 API
description: 映射主控 API
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fabf41d1c82420709b39bb5db03c2ac3e851d2
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119674"
---
# <a name="image-mastering-api"></a><span data-ttu-id="30ff7-103">映射主控 API</span><span class="sxs-lookup"><span data-stu-id="30ff7-103">Image Mastering API</span></span>

## <a name="purpose"></a><span data-ttu-id="30ff7-104">目的</span><span class="sxs-lookup"><span data-stu-id="30ff7-104">Purpose</span></span>

<span data-ttu-id="30ff7-105">Microsoft Windows 映像主控 API 可讓應用程式將映射預備和燒錄至 CD、DVD 和藍光光學儲存體媒體。</span><span class="sxs-lookup"><span data-stu-id="30ff7-105">The Microsoft Windows image mastering API enables applications to stage and burn images to CD, DVD, and Blu-ray optical storage media.</span></span> <span data-ttu-id="30ff7-106">以相同方式配置影像的其他類似光碟的媒體也可以使用此 API。</span><span class="sxs-lookup"><span data-stu-id="30ff7-106">Other disc-like media that lay images in the same manner can also use this API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="30ff7-107">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="30ff7-107">Developer audience</span></span>

<span data-ttu-id="30ff7-108">IMAPI.EXE 是針對 C/c + + 和 Visual Basic 開發人員所設計，以及使用 VBScript 撰寫腳本的程式開發人員。</span><span class="sxs-lookup"><span data-stu-id="30ff7-108">IMAPI is designed for C/C++ and Visual Basic developers and those writing scripts using VBScript.</span></span>

<span data-ttu-id="30ff7-109">建議您瞭解 CD、DVD 和藍光技術以及檔案系統。</span><span class="sxs-lookup"><span data-stu-id="30ff7-109">Knowledge of CD, DVD, and Blu-ray technologies and file systems is recommended.</span></span> <span data-ttu-id="30ff7-110">開發人員可能會在 [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go)中熟悉多媒體命令 (MMC) 的最新版本。</span><span class="sxs-lookup"><span data-stu-id="30ff7-110">Developers may benefit from a familiarity with the latest revision of Multimedia Command (MMC) at [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="30ff7-111">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="30ff7-111">Run-time requirements</span></span>

<span data-ttu-id="30ff7-112">從 Windows Vista 和 Windows Server 2008 開始，原本就支援 IMAPI.EXE 2.0。</span><span class="sxs-lookup"><span data-stu-id="30ff7-112">IMAPI 2.0 is supported natively starting with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="30ff7-113">啟用 Windows XP 和 Windows Server 2003 的 IMAPI.EXE 2.0 功能需要安裝 [KB932716](https://support.microsoft.com/kb/932716) 更新套件。</span><span class="sxs-lookup"><span data-stu-id="30ff7-113">Enabling IMAPI 2.0 functionality for Windows XP and Windows Server 2003 requires the installation of the [KB932716](https://support.microsoft.com/kb/932716) update package.</span></span> <span data-ttu-id="30ff7-114">如果未安裝此封裝，Windows XP 仍會以原生方式支援 [imapi.exe 1.0](imapiv1.md)。</span><span class="sxs-lookup"><span data-stu-id="30ff7-114">If this package is not installed, Windows XP still natively supports [IMAPI 1.0](imapiv1.md).</span></span>

> [!Note]  
> <span data-ttu-id="30ff7-115">適用于儲存體的 Windows Feature Pack 可透過 [Microsoft 下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)取得。</span><span class="sxs-lookup"><span data-stu-id="30ff7-115">The Windows Feature Pack for Storage is available to the public via the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span></span> <span data-ttu-id="30ff7-116">您可以在 [ [新功能](what-s-new.md) ] 區段中找到有關特定 API 變更的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="30ff7-116">Additional information regarding specific API changes can be found in the [What's New](what-s-new.md) section.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="30ff7-117">本節內容</span><span class="sxs-lookup"><span data-stu-id="30ff7-117">In this section</span></span>



| <span data-ttu-id="30ff7-118">主題</span><span class="sxs-lookup"><span data-stu-id="30ff7-118">Topic</span></span>                                             | <span data-ttu-id="30ff7-119">描述</span><span class="sxs-lookup"><span data-stu-id="30ff7-119">Description</span></span>                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="30ff7-120">新功能</span><span class="sxs-lookup"><span data-stu-id="30ff7-120">What's New</span></span>](what-s-new.md)<br/>           | <span data-ttu-id="30ff7-121">詳述映射主控 API 每個重要版本的資訊。</span><span class="sxs-lookup"><span data-stu-id="30ff7-121">Information detailing each significant release of the Image Mastering API.</span></span><br/> |
| [<span data-ttu-id="30ff7-122">關於 IMAPI.EXE</span><span class="sxs-lookup"><span data-stu-id="30ff7-122">About IMAPI</span></span>](about-imapi.md)<br/>         | <span data-ttu-id="30ff7-123">映射主控 API 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="30ff7-123">General information about the Image Mastering API.</span></span><br/>                         |
| [<span data-ttu-id="30ff7-124">使用 IMAPI.EXE</span><span class="sxs-lookup"><span data-stu-id="30ff7-124">Using IMAPI</span></span>](using-imapi.md)<br/>         | <span data-ttu-id="30ff7-125">工作相關的主題，示範如何使用映射主控 API。</span><span class="sxs-lookup"><span data-stu-id="30ff7-125">Task-related topics that demonstrate how to use the Image Mastering API.</span></span><br/>   |
| [<span data-ttu-id="30ff7-126">IMAPI.EXE 參考</span><span class="sxs-lookup"><span data-stu-id="30ff7-126">IMAPI Reference</span></span>](imapi-reference.md)<br/> | <span data-ttu-id="30ff7-127">IMAPI.EXE 介面和其他程式設計項目的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="30ff7-127">Detailed descriptions of IMAPI interfaces and other programming elements.</span></span><br/>  |



 

## <a name="additional-resources"></a><span data-ttu-id="30ff7-128">其他資源</span><span class="sxs-lookup"><span data-stu-id="30ff7-128">Additional resources</span></span>

<span data-ttu-id="30ff7-129">您可以在下列位置找到有關 IMAPI.EXE 和其他相關主題的進一步資訊：</span><span class="sxs-lookup"><span data-stu-id="30ff7-129">Further information regarding IMAPI and other related subjects can be found at the following locations:</span></span>



| <span data-ttu-id="30ff7-130">主題</span><span class="sxs-lookup"><span data-stu-id="30ff7-130">Topic</span></span>                                                                                                 | <span data-ttu-id="30ff7-131">描述</span><span class="sxs-lookup"><span data-stu-id="30ff7-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30ff7-132">Microsoft 光學儲存體 Blog</span><span class="sxs-lookup"><span data-stu-id="30ff7-132">Microsoft Optical Storage Blog</span></span>](/archive/blogs/opticalstorage/)                | <span data-ttu-id="30ff7-133">著重在實際開發案例中，著重于映射主控 API 實作為的主題。</span><span class="sxs-lookup"><span data-stu-id="30ff7-133">Highlights topics that focus on the implementation of the Image Mastering API in real world development scenarios.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="30ff7-134">光學平臺討論論壇</span><span class="sxs-lookup"><span data-stu-id="30ff7-134">Optical Platform Discussion Forum</span></span>](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | <span data-ttu-id="30ff7-135">討論 CDROM.SYS、IMAPIv2 和 Live File System 問題。</span><span class="sxs-lookup"><span data-stu-id="30ff7-135">Discuss CDROM.SYS, IMAPIv2 and Live File System issues.</span></span> <span data-ttu-id="30ff7-136">此論壇著重于系統層級的主題，適用于應用程式開發人員，而非使用者。</span><span class="sxs-lookup"><span data-stu-id="30ff7-136">This forum focuses on system-level topics and is intended for application developers rather than endusers.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="30ff7-137">T10 技術委員會</span><span class="sxs-lookup"><span data-stu-id="30ff7-137">T10 Technical Committee</span></span>](https://www.t10.org/)                       | <span data-ttu-id="30ff7-138">國際委員會的資訊技術標準 (INCITS，發音為「深入解析」 ) 。</span><span class="sxs-lookup"><span data-stu-id="30ff7-138">A Technical Committee of the InterNational Committee on Information Technology Standards (INCITS, pronounced "insights").</span></span> <span data-ttu-id="30ff7-139">INCITS 由的認可，並且會在由美國國家標準局 (ANSI) 的核准規則下運作。</span><span class="sxs-lookup"><span data-stu-id="30ff7-139">INCITS is accredited by, and operates under rules that are approved by, the American National Standards Institute (ANSI).</span></span> <span data-ttu-id="30ff7-140">這些規則的設計是為了確保自願標準是由產業團隊的共識所開發。</span><span class="sxs-lookup"><span data-stu-id="30ff7-140">These rules are designed to ensure that voluntary standards are developed by the consensus of industry groups.</span></span> |
| [<span data-ttu-id="30ff7-141"> (OSTA) 的光學儲存體技術關聯 </span><span class="sxs-lookup"><span data-stu-id="30ff7-141">Optical Storage Technology Association (OSTA)</span></span>](http://www.osta.org/) | <span data-ttu-id="30ff7-142">可透過週期性商業化光學儲存體應用程式會議，來塑造產業的未來 (COSA) 、DVD 相容性、行銷、MPV (MusicPhotoVideo) 、UDF 委員會，以及全新的特殊藍色鐳射委員會。</span><span class="sxs-lookup"><span data-stu-id="30ff7-142">Works to shape the future of the industry through regular meetings of Commercial Optical Storage Applications (COSA), DVD Compatibility, Marketing, MPV (MusicPhotoVideo), UDF committees, and a new adhoc Blue Laser committee.</span></span> <span data-ttu-id="30ff7-143">全球有興趣的公司受邀加入組織，並參與其委員會和計畫。</span><span class="sxs-lookup"><span data-stu-id="30ff7-143">Interested companies worldwide are invited to join the organization and participate in its committees and programs.</span></span>               |



 

 

