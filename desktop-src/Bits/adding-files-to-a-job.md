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
# <a name="adding-files-to-a-job"></a>將檔案新增至作業

作業包含一或多個您想要傳送的檔案。 您可以使用下列其中一種方法，將檔案新增至作業：

<dl> <dt>

<span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**IBackgroundCopyJob：： AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
</dt> <dd>

將單一檔案新增至作業。

</dd> <dt>

<span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
</dt> <dd>

將一或多個檔案新增至作業。 如果您要加入多個檔案，呼叫這個方法比在迴圈中呼叫 **AddFile** 方法更有效率。

</dd> <dt>

<span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)
</dt> <dd>

將單一檔案新增至作業。 如果您想要從檔案下載資料範圍，請使用這個方法。 您只能將此方法用於下載作業。

</dd> </dl>

當您將檔案新增至作業時，您會指定檔案的遠端名稱和本機名稱。 如需本機和遠端檔案名格式的詳細資訊，請參閱 BG 檔案 [**\_ \_ 資訊**](/windows/desktop/api/Bits/ns-bits-bg_file_info) 結構。

上傳工作只能包含一個檔案。 [](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) [](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) \_ \_ \_ \_ 如果您嘗試將一個以上的檔案新增至上傳作業，IBackgroundCopyJob：： AddFile 和 IBackgroundCopyJob：： AddFileSet 方法會傳回過多的 BG E。 如果您需要上傳一個以上的檔案，請考慮使用 CAB 或 ZIP 檔案。

針對下載作業，BITS 會將使用者可新增至作業的檔案數目限制為200個檔案，以及將檔案的範圍數目限制為500個範圍。 這些限制不適用於系統管理員或服務。 若要變更這些預設限制，請參閱 [群組原則](group-policies.md)。

作業的擁有者或具有系統管理員許可權的使用者，可以在呼叫 [**IBackgroundCopyJob：： Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法或 [**IBackgroundCopyJob：： Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) 方法之前，隨時將檔案新增至作業。

如果您在將檔案加入至作業之後需要變更檔案的遠端名稱，您可以呼叫 [**IBackgroundCopyJob3：： ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) 方法或 [**IBackgroundCopyFile2：： SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) 方法。 當伺服器無法使用時，請使用 **ReplaceRemotePrefix** 方法來變更遠端名稱的伺服器部分，或讓漫遊使用者連接到最接近的伺服器。 您可以使用 **SetRemoteName** 方法來變更用來傳送檔案的通訊協定，或變更檔案名或路徑。

BITS 會在目的目錄中建立暫存檔案，並使用暫存檔進行檔案傳輸。 若要取得暫存檔案名稱，請呼叫 [**IBackgroundCopyFile3：： GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) 方法。 當您呼叫 [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法時，BITS 會將暫存檔案名稱變更為目的地檔案名。 BITS 不會在 [**建立**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 暫存檔案時指定安全描述項， (檔案從目的地目錄) 繼承 ACL 資訊。 如果傳送的資料是敏感的，應用程式應該在目的地目錄上指定適當的 ACL，以防止未經授權的存取。

若要使用傳送的檔案來維護擁有者和 ACL 資訊，請呼叫 [**IBackgroundCopyJob3：： SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) 方法。

工作的擁有者 (建立作業的使用者，或是 [取得作業擁有權](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership)) 的系統管理員，必須具有伺服器和用戶端上檔案的許可權。 例如，若要下載檔案，使用者必須擁有伺服器的讀取權限，以及對用戶端上本機目錄的寫入權限。

下列範例示範如何將單一檔案新增至作業。 此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標 pJob 是有效的。


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



下列範例顯示如何將多個檔案新增至作業。 此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標 pJob 有效，且本機和遠端名稱來自使用者介面中的清單。


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



 

 