---
description: 如何傳回符合指定準則的變更日誌記錄。
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: 流覽變更日誌記錄的緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9384316e38c23951849006efc259268a7bdf33df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986999"
---
# <a name="walking-a-buffer-of-change-journal-records"></a><span data-ttu-id="b594d-103">流覽變更日誌記錄的緩衝區</span><span class="sxs-lookup"><span data-stu-id="b594d-103">Walking a Buffer of Change Journal Records</span></span>

<span data-ttu-id="b594d-104">傳回更新序號的控制項碼 (USN) 變更日誌記錄、 [**FSCTL \_ 讀取 \_ Usn \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) 和 [**FSCTL \_ 列舉 \_ usn \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)，會在輸出緩衝區中傳回類似的資料。</span><span class="sxs-lookup"><span data-stu-id="b594d-104">The control codes that return update sequence number (USN) change journal records, [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), return similar data in the output buffer.</span></span> <span data-ttu-id="b594d-105">兩者都會傳回 USN，後面接著零或多個變更日誌記錄，每個記錄都在 [**usn \_ 記錄 \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) 或 [**usn \_ 記錄 \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) 結構中。</span><span class="sxs-lookup"><span data-stu-id="b594d-105">Both return a USN followed by zero or more change journal records, each in a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure.</span></span>

<span data-ttu-id="b594d-106">USN 作業的目標磁片區必須是 ReFS 或 NTFS 3.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b594d-106">The target volume for USN operations must be ReFS or NTFS 3.0 or later.</span></span> <span data-ttu-id="b594d-107">若要取得 NTFS 版本的磁片區，請使用系統管理員存取權限開啟命令提示字元，然後執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="b594d-107">To obtain the NTFS version of a volume, open a command prompt with Administrator access rights and execute the following command:</span></span>

<span data-ttu-id="b594d-108">**FSUtil.exe FSInfo NTFSInfo** \*X \*\* \* *：*</span><span class="sxs-lookup"><span data-stu-id="b594d-108">**FSUtil.exe FSInfo NTFSInfo** *X\*\*\*:*\*</span></span>

<span data-ttu-id="b594d-109">其中 *X* 是磁片區的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="b594d-109">where *X* is the drive letter of the volume.</span></span>

<span data-ttu-id="b594d-110">下列清單會識別取得變更日誌記錄的方式：</span><span class="sxs-lookup"><span data-stu-id="b594d-110">The following list identifies ways to get change journal records:</span></span>

-   <span data-ttu-id="b594d-111">使用 [**FSCTL \_ 列舉 \_ USN \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) 來取得兩個 usn 之間所有變更日誌記錄的列舉)  (。</span><span class="sxs-lookup"><span data-stu-id="b594d-111">Use [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) to get a listing (enumeration) of all change journal records between two USNs.</span></span>
-   <span data-ttu-id="b594d-112">使用 [**FSCTL \_ READ \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) 更具選擇性，例如選取變更的特定原因或在檔案關閉時傳回。</span><span class="sxs-lookup"><span data-stu-id="b594d-112">Use [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) to be more selective, such as selecting specific reasons for changes or returning when a file is closed.</span></span>

> [!Note]  
> <span data-ttu-id="b594d-113">這兩項作業只會傳回符合指定準則之變更日誌記錄的子集。</span><span class="sxs-lookup"><span data-stu-id="b594d-113">Both of these operations return only the subset of change journal records that meet the specified criteria.</span></span>

 

<span data-ttu-id="b594d-114">以輸出緩衝區中的第一個專案傳回的 USN 是要抓取之下一個記錄號碼的 USN。</span><span class="sxs-lookup"><span data-stu-id="b594d-114">The USN returned as the first item in the output buffer is the USN of the next record number to be retrieved.</span></span> <span data-ttu-id="b594d-115">使用此值可繼續從結尾界限讀取記錄。</span><span class="sxs-lookup"><span data-stu-id="b594d-115">Use this value to continue reading records from the end boundary forward.</span></span>

<span data-ttu-id="b594d-116">[**USN \_ 記錄 \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)或 [**usn \_ 記錄 \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3)的 **FileName** 成員包含要套用問題記錄的檔案名。</span><span class="sxs-lookup"><span data-stu-id="b594d-116">The **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contains the name of the file to which the record in question applies.</span></span> <span data-ttu-id="b594d-117">檔案名的長度會有所不同，因此 **usn \_ 記錄 \_ V2** 和 **usn \_ 記錄 \_ V3** 是可變長度的結構。</span><span class="sxs-lookup"><span data-stu-id="b594d-117">The file name varies in length, so **USN\_RECORD\_V2** and **USN\_RECORD\_V3** are variable length structures.</span></span> <span data-ttu-id="b594d-118">其第一個成員 **RecordLength** 是結構的長度 (包括檔案名) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b594d-118">Their first member, **RecordLength**, is the length of the structure (including the file name), in bytes.</span></span>

<span data-ttu-id="b594d-119">當您使用「 [**usn \_ 記錄 \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) 」和「 [**usn \_ 記錄 \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) 」結構的 **FileName** 成員時，請勿假設檔案名包含尾端的 ' \\ 0 ' 分隔符號。</span><span class="sxs-lookup"><span data-stu-id="b594d-119">When you work with the **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structures, do not assume that the file name contains a trailing '\\0' delimiter.</span></span> <span data-ttu-id="b594d-120">若要判斷檔案名的長度，請使用 **FileNameLength** 成員。</span><span class="sxs-lookup"><span data-stu-id="b594d-120">To determine the length of the file name, use the **FileNameLength** member.</span></span>

<span data-ttu-id="b594d-121">下列範例會呼叫 [**FSCTL \_ READ \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) ，並引導作業傳回的變更日誌記錄緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b594d-121">The following example calls [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and walks the buffer of change journal records that the operation returns.</span></span>


```C++
#include <Windows.h>
#include <WinIoCtl.h>
#include <stdio.h>

#define BUF_LEN 4096

void main()
{
   HANDLE hVol;
   CHAR Buffer[BUF_LEN];

   USN_JOURNAL_DATA JournalData;
   READ_USN_JOURNAL_DATA ReadData = {0, 0xFFFFFFFF, FALSE, 0, 0};
   PUSN_RECORD UsnRecord;  

   DWORD dwBytes;
   DWORD dwRetBytes;
   int I;

   hVol = CreateFile( TEXT("\\\\.\\c:"), 
               GENERIC_READ | GENERIC_WRITE, 
               FILE_SHARE_READ | FILE_SHARE_WRITE,
               NULL,
               OPEN_EXISTING,
               0,
               NULL);

   if( hVol == INVALID_HANDLE_VALUE )
   {
      printf("CreateFile failed (%d)\n", GetLastError());
      return;
   }

   if( !DeviceIoControl( hVol, 
          FSCTL_QUERY_USN_JOURNAL, 
          NULL,
          0,
          &JournalData,
          sizeof(JournalData),
          &dwBytes,
          NULL) )
   {
      printf( "Query journal failed (%d)\n", GetLastError());
      return;
   }

   ReadData.UsnJournalID = JournalData.UsnJournalID;

   printf( "Journal ID: %I64x\n", JournalData.UsnJournalID );
   printf( "FirstUsn: %I64x\n\n", JournalData.FirstUsn );

   for(I=0; I<=10; I++)
   {
      memset( Buffer, 0, BUF_LEN );

      if( !DeviceIoControl( hVol, 
            FSCTL_READ_USN_JOURNAL, 
            &ReadData,
            sizeof(ReadData),
            &Buffer,
            BUF_LEN,
            &dwBytes,
            NULL) )
      {
         printf( "Read journal failed (%d)\n", GetLastError());
         return;
      }

      dwRetBytes = dwBytes - sizeof(USN);

      // Find the first record
      UsnRecord = (PUSN_RECORD)(((PUCHAR)Buffer) + sizeof(USN));  

      printf( "****************************************\n");

      // This loop could go on for a long time, given the current buffer size.
      while( dwRetBytes > 0 )
      {
         printf( "USN: %I64x\n", UsnRecord->Usn );
         printf("File name: %.*S\n", 
                  UsnRecord->FileNameLength/2, 
                  UsnRecord->FileName );
         printf( "Reason: %x\n", UsnRecord->Reason );
         printf( "\n" );

         dwRetBytes -= UsnRecord->RecordLength;

         // Find the next record
         UsnRecord = (PUSN_RECORD)(((PCHAR)UsnRecord) + 
                  UsnRecord->RecordLength); 
      }
      // Update starting USN for next call
      ReadData.StartUsn = *(USN *)&Buffer; 
   }

   CloseHandle(hVol);

}
```



<span data-ttu-id="b594d-122">[**Usn \_ 記錄 \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)或 [**usn \_ 記錄 \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3)結構所指定之任何記錄的大小（以位元組為單位）最多是 `((MaxComponentLength - 1) * Width) + Size` *MaxComponentLength* 是記錄檔名稱的最大長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="b594d-122">The size in bytes of any record specified by a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure is at most `((MaxComponentLength - 1) * Width) + Size` where *MaxComponentLength* is the maximum length in characters of the record file name.</span></span> <span data-ttu-id="b594d-123">寬度是寬字元的大小，而 *大小* 是結構的大小。</span><span class="sxs-lookup"><span data-stu-id="b594d-123">The width is the size of a wide character, and the *Size* is the size of the structure.</span></span>

<span data-ttu-id="b594d-124">若要取得最大長度，請呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函數，並檢查 *lpMaximumComponentLength* 參數所指向的值。</span><span class="sxs-lookup"><span data-stu-id="b594d-124">To obtain the maximum length, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the value pointed to by the *lpMaximumComponentLength* parameter.</span></span> <span data-ttu-id="b594d-125">從 *MaxComponentLength* 減去一個，以確定 [**Usn \_ 記錄**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) 和 [**usn \_ 記錄 \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) 的定義包含一個字元的檔案名。</span><span class="sxs-lookup"><span data-stu-id="b594d-125">Subtract one from *MaxComponentLength* to account for the fact that the definition of [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) includes one character of the file name.</span></span>

<span data-ttu-id="b594d-126">在 C 程式設計語言中，最大可能的記錄大小如下所示：</span><span class="sxs-lookup"><span data-stu-id="b594d-126">In the C programming language, the largest possible record size is the following:</span></span>

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
