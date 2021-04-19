---
description: 除了透過 >ivssbackupcomponents 介面透過其複本的裝置物件來存取之外，要求者也可以將陰影複製提供給其他進程使用，做為掛接的唯讀裝置。
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: 公開及呈現陰影複製的磁片區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985701"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a><span data-ttu-id="f4304-103">公開及呈現陰影複製的磁片區</span><span class="sxs-lookup"><span data-stu-id="f4304-103">Exposing and Surfacing Shadow Copied Volumes</span></span>

<span data-ttu-id="f4304-104">除了透過 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面透過其複本的 [*裝置物件*](vssgloss-d.md)來存取之外，要求者也可以將陰影複製提供給其他進程使用，做為掛接的唯讀裝置。</span><span class="sxs-lookup"><span data-stu-id="f4304-104">In addition to being accessed through the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface by means of its copy's [*device object*](vssgloss-d.md), a requester can make a shadow copy available to other processes as a mounted read-only device.</span></span>

<span data-ttu-id="f4304-105">此程式稱為 [*公開陰影複製*](vssgloss-e.md)，並使用 [**>ivssbackupcomponents：： ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) 方法執行。</span><span class="sxs-lookup"><span data-stu-id="f4304-105">This process is known as [*exposing a shadow copy*](vssgloss-e.md), and is performed using the [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) method.</span></span>

<span data-ttu-id="f4304-106">陰影複製可以公開為本機磁片區—指派磁碟機號或與掛接的資料夾相關聯，或作為檔案共用。</span><span class="sxs-lookup"><span data-stu-id="f4304-106">A shadow copy can be exposed as a local volume—assigned a drive letter or associated with a mounted folder—or as a file share.</span></span>

<span data-ttu-id="f4304-107">為了說明這一點，請考慮在掛接于 F：的系統 exposedSys 上的磁片區所組成的陰影複製， \\ 其根目錄為 dirOne 和 dirTwo 目錄，以及檔案 >fileone.txt。</span><span class="sxs-lookup"><span data-stu-id="f4304-107">To illustrate, consider a shadow copy made of a volume on the system exposedSys mounted at F:\\ on whose root are the directories dirOne and dirTwo, and the file FileOne.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="f4304-108">在本機公開陰影複製</span><span class="sxs-lookup"><span data-stu-id="f4304-108">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="f4304-109">掛接為本機磁片區時，陰影複製的根目錄一律會顯示在掛接點 (磁碟機號或掛接的資料夾) ，而且所有陰影複製的檔案都是可見的。</span><span class="sxs-lookup"><span data-stu-id="f4304-109">When mounted as a local volume, the shadow copy's root is always visible at the mount point (drive letter or mounted folder) and all the shadow-copied files are visible.</span></span>

<span data-ttu-id="f4304-110">如果陰影複製是透過掛接的資料夾 C： ShadowOfF 在本機公開的 \\ ，您會發現磁片上的所有檔案都掛接于 F： \\ 于 C： ShadowOfF 下提供的陰影複製時 \\ 。</span><span class="sxs-lookup"><span data-stu-id="f4304-110">If the shadow copy was locally exposed through the mounted folder C:\\ShadowOfF, you would find all files present on disk mounted at F:\\ at the time of the shadow copy available under C:\\ShadowOfF.</span></span> <span data-ttu-id="f4304-111">檢查 C： \\ ShadowOfF 會顯示兩個目錄（dirOne 和 dirTwo），以及 c： ShadowOfF 下的一個檔案（>fileone.txt） \\ 。</span><span class="sxs-lookup"><span data-stu-id="f4304-111">Examining C:\\ShadowOfF would reveal two directories, dirOne and dirTwo, and one file, fileOne, under C:\\ShadowOfF.</span></span>

<span data-ttu-id="f4304-112">在本機公開陰影複製的呼叫可能是：</span><span class="sxs-lookup"><span data-stu-id="f4304-112">A call to locally expose the shadow copy might be:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  PWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
         snapID,                           // VSS_ID SnapshotId,
         NULL,                             // VSS_PWSZ wszPathFromRoot
         VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY, // LONG lAttributes
         L"C:\ShadowOfF",                  // VSS_PWSZ wszExpose
         LPWSTR &wszExposed,               // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="f4304-113">如果已成功在本機公開陰影複製， *wszExposed* 應該包含寬字元字串 "C： \\ ShadowOfF"。</span><span class="sxs-lookup"><span data-stu-id="f4304-113">If the shadow copy was successfully exposed locally, *wszExposed* should contain the wide character string "C:\\ShadowOfF."</span></span>

<span data-ttu-id="f4304-114">您稍後可以藉由呼叫 [**IVssBackupComponentsEx2：： UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot)，將陰影複製未公開。</span><span class="sxs-lookup"><span data-stu-id="f4304-114">The shadow copy can later be unexposed by calling [**IVssBackupComponentsEx2::UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).</span></span>

<span data-ttu-id="f4304-115">只有持續性陰影複製（也就是以 VSS \_ CTX \_ NAS \_ 復原或 vss CTX 應用程式回復所建立的陰影複製 \_ \_ \_ ）可以在本機公開。</span><span class="sxs-lookup"><span data-stu-id="f4304-115">Only persistent shadow copies—that is, shadow copies created with either VSS\_CTX\_NAS\_ROLLBACK or VSS\_CTX\_APP\_ROLLBACK—can be exposed locally.</span></span>

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a><span data-ttu-id="f4304-116">將陰影複製公開為遠端共用</span><span class="sxs-lookup"><span data-stu-id="f4304-116">Exposing a Shadow Copy as a Remote Share</span></span>

<span data-ttu-id="f4304-117">或者，您也可以選擇將磁片的陰影複製設為 F： \\ 提供作為遠端檔案共用，並只將 dirTwo 下的資料公開為檔案共用 dirTwoOfF。</span><span class="sxs-lookup"><span data-stu-id="f4304-117">Alternatively, you could choose to make the shadow copy of the disk mounted at F:\\ available as a remote file share, and expose only data under dirTwo as the file share dirTwoOfF.</span></span>

<span data-ttu-id="f4304-118">在此情況下，系統可以將 \\ \\ \\ exposedSys \\ dirTwoOfF 對應為網路磁碟機機，以存取 F： dirTwo 下的檔案陰影複製。</span><span class="sxs-lookup"><span data-stu-id="f4304-118">In this case, systems could access the shadow copy of files under F:\\dirTwo by mapping \\\\exposedSys\\dirTwoOfF as a network drive.</span></span>

<span data-ttu-id="f4304-119">執行遠端將陰影複製公開為共用的呼叫可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="f4304-119">A call to implement remote exposing the shadow copy as a share might be the following:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  LPWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
               snapID,                            // VSS_ID SnapshotId,
               L"\dirTwo",                        // VSS_PWSZ wszPathFromRoot
               VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY, // LONG lAttributes
               L"dirTwoOfF",                      // VSS_PWSZ wszExpose
               LPWSTR &wszExposed,                // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="f4304-120">如果已成功從遠端公開陰影複製， *wszExposed* 應該包含寬字元字串 "dirTwoOfF"。</span><span class="sxs-lookup"><span data-stu-id="f4304-120">If the shadow copy was successfully exposed remotely, *wszExposed* should contain the wide character string "dirTwoOfF."</span></span>

<span data-ttu-id="f4304-121">任何目前對應 dirTwoOfF 網路共用的系統都可以中斷連線，就像它可能與任何一般共用中斷連線一樣。</span><span class="sxs-lookup"><span data-stu-id="f4304-121">Any system currently mapping the network share of dirTwoOfF could disconnect from it, just as it might disconnect from any ordinary share.</span></span>

## <a name="surfacing-a-shadow-copy"></a><span data-ttu-id="f4304-122">呈現陰影複製</span><span class="sxs-lookup"><span data-stu-id="f4304-122">Surfacing a Shadow Copy</span></span>

<span data-ttu-id="f4304-123">[*呈現的陰影複製*](vssgloss-s.md)是系統的 Mount Manager 命名空間已知的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="f4304-123">A [*surfaced shadow copy*](vssgloss-s.md) is one in which the shadow copy is known to a system's Mount Manager namespace.</span></span>

<span data-ttu-id="f4304-124">這表示，您可以使用 **FindFirstVolume** 和 **FindNextVolume**，找出這類陰影複製的方式，就像是尋找任何其他可用但尚未載入的磁片區。</span><span class="sxs-lookup"><span data-stu-id="f4304-124">This means that you can locate such shadow copies just as you would locate any other available but not-yet-mounted volume—by using **FindFirstVolume** and **FindNextVolume**, for example.</span></span>

<span data-ttu-id="f4304-125">顯然，公開的陰影複製也會呈現陰影複製。</span><span class="sxs-lookup"><span data-stu-id="f4304-125">Clearly, then, exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="f4304-126">不過，反向並不一定是 true。</span><span class="sxs-lookup"><span data-stu-id="f4304-126">However, the reverse is not necessarily true.</span></span>

<span data-ttu-id="f4304-127">如果已卸載本機公開的陰影複製，或系統選擇中斷遠端公開陰影複製的連接，則不會再公開陰影複製。</span><span class="sxs-lookup"><span data-stu-id="f4304-127">If a locally exposed shadow copy was dismounted, or a system chose to disconnect a remotely exposed shadow copy, that shadow copy would no longer be exposed.</span></span> <span data-ttu-id="f4304-128">不過，只要保存陰影複製，就會顯示磁片區。</span><span class="sxs-lookup"><span data-stu-id="f4304-128">However, as long as the shadow copy persisted, the volumes would be surfaced.</span></span> <span data-ttu-id="f4304-129">這表示它們可以像任何其他唯讀磁片區一樣掛接。</span><span class="sxs-lookup"><span data-stu-id="f4304-129">This means they could be mounted like any other read-only volume.</span></span>

 

 



