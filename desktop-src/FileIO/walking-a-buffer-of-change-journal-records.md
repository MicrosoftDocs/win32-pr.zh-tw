---
description: 如何傳回符合指定準則的變更日誌記錄。
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: 流覽變更日誌記錄的緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9242d671cedfb5c9ef2b5fa836e29c455d09a9e1287b1ed035712f49c6c7d627
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830148"
---
# <a name="walking-a-buffer-of-change-journal-records"></a>流覽變更日誌記錄的緩衝區

傳回更新序號的控制項碼 (USN) 變更日誌記錄、 [**FSCTL \_ 讀取 \_ Usn \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) 和 [**FSCTL \_ 列舉 \_ usn \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)，會在輸出緩衝區中傳回類似的資料。 兩者都會傳回 USN，後面接著零或多個變更日誌記錄，每個記錄都在 [**usn \_ 記錄 \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) 或 [**usn \_ 記錄 \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) 結構中。

USN 作業的目標磁片區必須是 ReFS 或 NTFS 3.0 或更新版本。 若要取得 NTFS 版本的磁片區，請使用系統管理員存取權限開啟命令提示字元，然後執行下列命令：

**FSUtil.exe FSInfo NTFSInfo** *X ** * *：*

其中 *X* 是磁片區的磁碟機號。

下列清單會識別取得變更日誌記錄的方式：

-   使用 [**FSCTL \_ 列舉 \_ USN \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) 來取得兩個 usn 之間所有變更日誌記錄的列舉)  (。
-   使用 [**FSCTL \_ READ \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) 更具選擇性，例如選取變更的特定原因或在檔案關閉時傳回。

> [!Note]  
> 這兩項作業只會傳回符合指定準則之變更日誌記錄的子集。

 

以輸出緩衝區中的第一個專案傳回的 USN 是要抓取之下一個記錄號碼的 USN。 使用此值可繼續從結尾界限讀取記錄。

[**USN \_ 記錄 \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)或 [**usn \_ 記錄 \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3)的 **FileName** 成員包含要套用問題記錄的檔案名。 檔案名的長度會有所不同，因此 **usn \_ 記錄 \_ V2** 和 **usn \_ 記錄 \_ V3** 是可變長度的結構。 其第一個成員 **RecordLength** 是結構的長度 (包括檔案名) （以位元組為單位）。

當您使用「 [**usn \_ 記錄 \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) 」和「 [**usn \_ 記錄 \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) 」結構的 **FileName** 成員時，請勿假設檔案名包含尾端的 ' \\ 0 ' 分隔符號。 若要判斷檔案名的長度，請使用 **FileNameLength** 成員。

下列範例會呼叫 [**FSCTL \_ READ \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) ，並引導作業傳回的變更日誌記錄緩衝區。


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



[**Usn \_ 記錄 \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)或 [**usn \_ 記錄 \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3)結構所指定之任何記錄的大小（以位元組為單位）最多是 `((MaxComponentLength - 1) * Width) + Size` *MaxComponentLength* 是記錄檔名稱的最大長度（以字元為單位）。 寬度是寬字元的大小，而 *大小* 是結構的大小。

若要取得最大長度，請呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函數，並檢查 *lpMaximumComponentLength* 參數所指向的值。 從 *MaxComponentLength* 減去一個，以確定 [**Usn \_ 記錄**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) 和 [**usn \_ 記錄 \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) 的定義包含一個字元的檔案名。

在 C 程式設計語言中，最大可能的記錄大小如下所示：

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
