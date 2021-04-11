---
title: 將檔案新增至作業
description: 作業包含一或多個您想要傳送的檔案。
ms.assetid: fb6e7219-b6ca-4f72-b7a3-60d65e8f3892
keywords:
- 傳送工作 BITS，新增檔案
- 檔案傳輸位，新增
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: ecb46a535fee117750b8b46066d798a4525aa44c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933382"
---
# <a name="adding-files-to-a-job"></a><span data-ttu-id="80dd2-105">將檔案新增至作業</span><span class="sxs-lookup"><span data-stu-id="80dd2-105">Adding Files to a Job</span></span>

<span data-ttu-id="80dd2-106">作業包含一或多個您想要傳送的檔案。</span><span class="sxs-lookup"><span data-stu-id="80dd2-106">A job contains one or more files that you want to transfer.</span></span> <span data-ttu-id="80dd2-107">您可以使用下列其中一種方法，將檔案新增至作業：</span><span class="sxs-lookup"><span data-stu-id="80dd2-107">Use one of the following methods to add files to a job:</span></span>

<dl> <dt>

<span data-ttu-id="80dd2-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**IBackgroundCopyJob：： AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span><span class="sxs-lookup"><span data-stu-id="80dd2-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span></span>
</dt> <dd>

<span data-ttu-id="80dd2-109">將單一檔案新增至作業。</span><span class="sxs-lookup"><span data-stu-id="80dd2-109">Adds a single file to a job.</span></span>

</dd> <dt>

<span data-ttu-id="80dd2-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span><span class="sxs-lookup"><span data-stu-id="80dd2-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span></span>
</dt> <dd>

<span data-ttu-id="80dd2-111">將一或多個檔案新增至作業。</span><span class="sxs-lookup"><span data-stu-id="80dd2-111">Adds one or more files to a job.</span></span> <span data-ttu-id="80dd2-112">如果您要加入多個檔案，呼叫這個方法比在迴圈中呼叫 **AddFile** 方法更有效率。</span><span class="sxs-lookup"><span data-stu-id="80dd2-112">If you are adding multiple files, it is more efficient to call this method than to call the **AddFile** method in a loop.</span></span>

</dd> <dt>

<span data-ttu-id="80dd2-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span><span class="sxs-lookup"><span data-stu-id="80dd2-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span></span>
</dt> <dd>

<span data-ttu-id="80dd2-114">將單一檔案新增至作業。</span><span class="sxs-lookup"><span data-stu-id="80dd2-114">Adds a single file to a job.</span></span> <span data-ttu-id="80dd2-115">如果您想要從檔案下載資料範圍，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="80dd2-115">Use this method if you want to download ranges of data from a file.</span></span> <span data-ttu-id="80dd2-116">您只能將此方法用於下載作業。</span><span class="sxs-lookup"><span data-stu-id="80dd2-116">You can use this method only for download jobs.</span></span>

</dd> </dl>

<span data-ttu-id="80dd2-117">當您將檔案新增至作業時，您會指定檔案的遠端名稱和本機名稱。</span><span class="sxs-lookup"><span data-stu-id="80dd2-117">When you add a file to a job, you specify the remote name and the local name of the file.</span></span> <span data-ttu-id="80dd2-118">如需本機和遠端檔案名格式的詳細資訊，請參閱 BG 檔案 [**\_ \_ 資訊**](/windows/desktop/api/Bits/ns-bits-bg_file_info) 結構。</span><span class="sxs-lookup"><span data-stu-id="80dd2-118">For details on the format of the local and remote file names, see the [**BG\_FILE\_INFO**](/windows/desktop/api/Bits/ns-bits-bg_file_info) structure.</span></span>

<span data-ttu-id="80dd2-119">上傳工作只能包含一個檔案。</span><span class="sxs-lookup"><span data-stu-id="80dd2-119">An upload job can contain only one file.</span></span> <span data-ttu-id="80dd2-120">[](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) [](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) \_ \_ \_ \_ 如果您嘗試將一個以上的檔案新增至上傳作業，IBackgroundCopyJob：： AddFile 和 IBackgroundCopyJob：： AddFileSet 方法會傳回過多的 BG E。</span><span class="sxs-lookup"><span data-stu-id="80dd2-120">The [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) and [**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) methods return BG\_E\_TOO\_MANY\_FILES if you try to add more than one file to an upload job.</span></span> <span data-ttu-id="80dd2-121">如果您需要上傳一個以上的檔案，請考慮使用 CAB 或 ZIP 檔案。</span><span class="sxs-lookup"><span data-stu-id="80dd2-121">If you need to upload more than one file, consider using a CAB or ZIP file.</span></span>

<span data-ttu-id="80dd2-122">針對下載作業，BITS 會將使用者可新增至作業的檔案數目限制為200個檔案，以及將檔案的範圍數目限制為500個範圍。</span><span class="sxs-lookup"><span data-stu-id="80dd2-122">For download jobs, BITS limits the number of files that a user can add to a job to 200 files and the number of ranges for a file to 500 ranges.</span></span> <span data-ttu-id="80dd2-123">這些限制不適用於系統管理員或服務。</span><span class="sxs-lookup"><span data-stu-id="80dd2-123">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="80dd2-124">若要變更這些預設限制，請參閱 [群組原則](group-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="80dd2-124">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="80dd2-125">作業的擁有者或具有系統管理員許可權的使用者，可以在呼叫 [**IBackgroundCopyJob：： Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法或 [**IBackgroundCopyJob：： Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) 方法之前，隨時將檔案新增至作業。</span><span class="sxs-lookup"><span data-stu-id="80dd2-125">The owner of the job or a user with administrator privileges can add files to the job anytime prior to calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span>

<span data-ttu-id="80dd2-126">如果您在將檔案加入至作業之後需要變更檔案的遠端名稱，您可以呼叫 [**IBackgroundCopyJob3：： ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) 方法或 [**IBackgroundCopyFile2：： SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) 方法。</span><span class="sxs-lookup"><span data-stu-id="80dd2-126">If you need to change the remote name of the file after you add the file to the job, you can call the [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) method or the [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) method.</span></span> <span data-ttu-id="80dd2-127">當伺服器無法使用時，請使用 **ReplaceRemotePrefix** 方法來變更遠端名稱的伺服器部分，或讓漫遊使用者連接到最接近的伺服器。</span><span class="sxs-lookup"><span data-stu-id="80dd2-127">Use the **ReplaceRemotePrefix** method to change the server portion of the remote name when the server is unavailable or to let roaming users connect to the closest server.</span></span> <span data-ttu-id="80dd2-128">您可以使用 **SetRemoteName** 方法來變更用來傳送檔案的通訊協定，或變更檔案名或路徑。</span><span class="sxs-lookup"><span data-stu-id="80dd2-128">Use the **SetRemoteName** method to change the protocol used to transfer the file or to change the file name or path.</span></span>

<span data-ttu-id="80dd2-129">BITS 會在目的目錄中建立暫存檔案，並使用暫存檔進行檔案傳輸。</span><span class="sxs-lookup"><span data-stu-id="80dd2-129">BITS creates a temporary file in the destination directory and uses the temporary file for the file transfer.</span></span> <span data-ttu-id="80dd2-130">若要取得暫存檔案名稱，請呼叫 [**IBackgroundCopyFile3：： GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) 方法。</span><span class="sxs-lookup"><span data-stu-id="80dd2-130">To get the temporary file name, call the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method.</span></span> <span data-ttu-id="80dd2-131">當您呼叫 [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法時，BITS 會將暫存檔案名稱變更為目的地檔案名。</span><span class="sxs-lookup"><span data-stu-id="80dd2-131">BITS changes the temporary file name to the destination file name when you call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="80dd2-132">BITS 不會在 [**建立**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 暫存檔案時指定安全描述項， (檔案從目的地目錄) 繼承 ACL 資訊。</span><span class="sxs-lookup"><span data-stu-id="80dd2-132">BITS does not specify a security descriptor when it [**creates**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) the temporary file (the file inherits the ACL information from the destination directory).</span></span> <span data-ttu-id="80dd2-133">如果傳送的資料是敏感的，應用程式應該在目的地目錄上指定適當的 ACL，以防止未經授權的存取。</span><span class="sxs-lookup"><span data-stu-id="80dd2-133">If the transferred data is sensitive, the application should specify an appropriate ACL on the destination directory to prevent unauthorized access.</span></span>

<span data-ttu-id="80dd2-134">若要使用傳送的檔案來維護擁有者和 ACL 資訊，請呼叫 [**IBackgroundCopyJob3：： SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) 方法。</span><span class="sxs-lookup"><span data-stu-id="80dd2-134">To maintain the owner and ACL information with the transferred file, call the [**IBackgroundCopyJob3::SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) method.</span></span>

<span data-ttu-id="80dd2-135">工作的擁有者 (建立作業的使用者，或是 [取得作業擁有權](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership)) 的系統管理員，必須具有伺服器和用戶端上檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="80dd2-135">The owner of the job (the user who created the job or the administrator who [took ownership](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) of the job) must have permissions to the file on the server as well as the client.</span></span> <span data-ttu-id="80dd2-136">例如，若要下載檔案，使用者必須擁有伺服器的讀取權限，以及對用戶端上本機目錄的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="80dd2-136">For example, to download a file the user must have read permissions on the server and write permissions to the local directory on the client.</span></span>

<span data-ttu-id="80dd2-137">下列範例示範如何將單一檔案新增至作業。</span><span class="sxs-lookup"><span data-stu-id="80dd2-137">The following example shows how to add a single file to the job.</span></span> <span data-ttu-id="80dd2-138">此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標 pJob 是有效的。</span><span class="sxs-lookup"><span data-stu-id="80dd2-138">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;

//Replace parameters with variables that contain valid paths.
hr = pJob->AddFile(L"https://ServerName/Path/File.Ext", L"d:\\Path\\File.Ext");
if (SUCCEEDED(hr))
{
  //Do something.
}
```



<span data-ttu-id="80dd2-139">下列範例顯示如何將多個檔案新增至作業。</span><span class="sxs-lookup"><span data-stu-id="80dd2-139">The following example shows how to add multiple files to the job.</span></span> <span data-ttu-id="80dd2-140">此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標 pJob 有效，且本機和遠端名稱來自使用者介面中的清單。</span><span class="sxs-lookup"><span data-stu-id="80dd2-140">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid and the local and remote names come from a list in the user interface.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_FILE_INFO* paFiles = NULL;
ULONG idx = 0;
ULONG nCount = 0;            //Set to the number of files to add to the job.
LPWSTR pszLocalName = NULL;  //Comes from the list in the user interface.
LPWSTR pszRemoteName = NULL; //Comes from the list in the user interface.

//Set nCount to the number of files to transfer.

//Allocate a block of memory to contain the array of BG_FILE_INFO structures.
//The BG_FILE_INFO structure contains the local and remote names of the 
//file being transferred.
paFiles = (BG_FILE_INFO*) malloc(sizeof(BG_FILE_INFO) * nCount);
if (NULL == paFiles)
{
  //Handle error
}
else
{
  //Add local and remote file name pairs to the memory block. 
  for (idx=0; idx<nCount; idx++)
  {
    //Set pszLocalName to point to an LPWSTR that contains the local name or
    //allocate memory for pszLocalName and copy the local name to pszLocalName.
    (paFiles+idx)->LocalName = pszLocalName;

    //Set pszRemoteName to point to an LPWSTR that contains the remote name or
    //allocate memory for pszRemoteName and copy the remote name to pszRemoteName.
    (paFiles+idx)->RemoteName = pszRemoteName;
  }

  //Add the files to the job.
  hr = pJob->AddFileSet(nCount, paFiles);
  if (SUCCEEDED(hr))
  {
     //Do Something.
  }

  //Free the memory block for the array of BG_FILE_INFO structures. If you allocated
  //memory for the local and remote file names, loop through the array and free the
  //memory for the file names before you free paFiles.
  free(paFiles);
}
```



 

 