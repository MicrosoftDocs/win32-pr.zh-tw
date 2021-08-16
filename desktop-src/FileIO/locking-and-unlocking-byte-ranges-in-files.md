---
description: 使用 LockFileEx 和 UnlockFileEx 函數來顯示位元組範圍鎖定和解除鎖定的範例程式碼。
ms.assetid: 9d54fe11-b1ad-4723-a42a-00bc6dc64072
title: 鎖定和解除鎖定檔案中的位元組範圍
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ccd18fc8a5e2f143cb58717f72abbc135421ee802ff93b651dad0916ed8a953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951157"
---
# <a name="locking-and-unlocking-byte-ranges-in-files"></a>鎖定和解除鎖定檔案中的位元組範圍

雖然系統允許一個以上的應用程式開啟檔案並寫入檔案，但應用程式不能寫到彼此的工作。 應用程式可以暫時鎖定檔案中的位元組範圍，以避免這個問題。

[**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile)和 [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)函數會鎖定檔案中指定的位元組範圍。 範圍可能會延伸超過檔的目前結尾。 檔案的鎖定部分會使用指定的檔案控制代碼，讓鎖定進程的執行緒獨佔存取指定的位元組範圍。 嘗試存取另一個進程鎖定的位元組範圍一律會失敗。 如果鎖定進程嘗試透過第二個檔案控制代碼來存取鎖定的位元組範圍，則嘗試會失敗。

> [!Note]  
> 位元組範圍鎖定不支援記憶體對應檔案。

 

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)函式可讓應用程式指定兩種鎖定類型的其中一種。 *獨佔鎖定* 會拒絕所有其他進程讀取和寫入檔案指定位元組範圍的存取權。 *共用鎖定* 會拒絕所有進程對指定位元組範圍的寫入權限，包括先鎖定位元組範圍的進程。 這可以用來在檔案中建立唯讀位元組範圍。

應用程式會使用 [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) 或 [**UnlockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfileex) 函式將位元組範圍解除鎖定，而且應該在關閉檔案之前解除鎖定所有鎖定的區域。

如需使用 [**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile)的範例，請參閱 [將一個檔案附加至另一個](appending-one-file-to-another-file.md)檔案。

下列範例示範如何使用 [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)。 第一個範例是簡單的示範，可建立檔案、將一些資料寫入其中，然後鎖定中間的區段。

**注意**  此範例不會在鎖定檔案之後變更資料。


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved

#include <windows.h>
#include <stdio.h>
#include <stdlib.h>

#define NUMWRITES 10
#define TESTSTRLEN 11

const char TestData[NUMWRITES][TESTSTRLEN] = 
{ 
    "TestData0\n",
    "TestData1\n",
    "TestData2\n",
    "TestData3\n",
    "TestData4\n",
    "TestData5\n",
    "TestData6\n",
    "TestData7\n",
    "TestData8\n",
    "TestData9\n"
};

int main(int argc, char *argv[])
{
    BOOL fSuccess = FALSE;

    // Create the file, open for both read and write.
    HANDLE hFile = CreateFile(TEXT("datafile.txt"),
                       GENERIC_READ | GENERIC_WRITE,
                       0,          // open with exclusive access
                       NULL,       // no security attributes
                       CREATE_NEW, // creating a new temp file
                       0,          // not overlapped index/O
                       NULL);
    
    if (hFile == INVALID_HANDLE_VALUE) 
    {
        // Handle the error.
        printf("CreateFile failed (%d)\n", GetLastError());
        return (1);
    }

    // Write some data to the file.
    DWORD dwNumBytesWritten = 0;

    for (int i=0; i<NUMWRITES; i++)
    {
        fSuccess = WriteFile(hFile,
                             TestData[i],
                             TESTSTRLEN,
                             &dwNumBytesWritten,
                             NULL);  // sync operation.
        if (!fSuccess) 
        {
           // Handle the error.
           printf("WriteFile failed (%d)\n", GetLastError());
           return (2);
        }
    } 

    FlushFileBuffers(hFile);

    // Lock the 4th write-section.  
    // First, set up the Overlapped structure with the file offset 
    // required by LockFileEx, three lines in to the file.
    OVERLAPPED sOverlapped;
    sOverlapped.Offset = TESTSTRLEN * 3;
    sOverlapped.OffsetHigh = 0;

    // Actually lock the file.  Specify exclusive access, and fail 
    // immediately if the lock cannot be obtained.
    fSuccess = LockFileEx(hFile,         // exclusive access, 
                          LOCKFILE_EXCLUSIVE_LOCK | 
                          LOCKFILE_FAIL_IMMEDIATELY,
                          0,             // reserved, must be zero
                          TESTSTRLEN,    // number of bytes to lock
                          0,
                          &sOverlapped); // contains the file offset
    if (!fSuccess) 
    {
       // Handle the error.
       printf ("LockFileEx failed (%d)\n", GetLastError());
       return (3);
    }
    else printf("LockFileEx succeeded\n");

    /////////////////////////////////////////////////////////////////
    // Add code that does something interesting to locked section,  /
    // which should be line 4                                       /
    /////////////////////////////////////////////////////////////////

    // Unlock the file.
    fSuccess = UnlockFileEx(hFile, 
                            0,             // reserved, must be zero
                            TESTSTRLEN,    // num. of bytes to unlock
                            0,
                            &sOverlapped); // contains the file offset
    if (!fSuccess) 
    {
       // Handle the error.
       printf ("UnlockFileEx failed (%d)\n", GetLastError());
       return (4);
    }
    else printf("UnlockFileEx succeeded\n");

    // Clean up handles, memory, and the created file.
    fSuccess = CloseHandle(hFile);
    if (!fSuccess) 
    {
       // Handle the error.
       printf ("CloseHandle failed (%d)\n", GetLastError());
       return (5);
    }

    fSuccess = DeleteFile(TEXT("datafile.txt"));
    if (!fSuccess) 
    {
        // Handle the error.
       printf ("DeleteFile failed (%d)\n", GetLastError());
       return (6);
    }
    return (0);
}
```



下列範例是位元組範圍鎖定的 advanced 示範，使用多個執行緒和簡單資料庫在單一資料檔案上執行隨機作業。 如需詳細資訊，請參閱內嵌程式碼批註以及範例程式碼後面的章節。


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved

#define UNICODE
#define _CRT_RAND_S
#include <stdlib.h>
#include <windows.h>

#include <stdio.h>

#include <malloc.h>
#include <conio.h>
#include <process.h>
#include <winioctl.h>

#define RECORD_SIZE 0x300
#define NUM_RECORDS 0x1000
#define NUM_THREADS 8

#define NUM_FILEOPS 500

#define BITMAP_SIZE ((NUM_RECORDS) / 8)
#define DATA_SIZE   ((RECORD_SIZE) - sizeof(RECORD_HEADER))

#define MSG_PRINTF(S,...) wprintf(L"[THREAD_ID %d] " S, \
    GetCurrentThreadId(), \
    __VA_ARGS__)

#if defined BRLS_DEBUG

#define DBG_PRINTF(S,...) wprintf(L"[THREAD_ID %d] " S, \
    GetCurrentThreadId(), \
    __VA_ARGS__)

#else

#define DBG_PRINTF(...)
#define PrintBitmap(...)

#endif


#define MASTER_RECORD_TYPE_CODE 'rtsM'
#define DATA_RECORD_TYPE_CODE   'ataD'


//
//  Record type definitions.
//
typedef struct _RECORD_HEADER {
    ULONG TypeCode;     // Either MASTER_RECORD_TYPE_CODE or DATA_RECORD_TYPE_CODE.
    ULONG SeqNumber;    // Starts at 1 and is incremented every time contents are modified.
} RECORD_HEADER;

typedef struct _MASTER_RECORD {
    RECORD_HEADER Header;
    BYTE Bitmap[BITMAP_SIZE];  // A bitmap indicating which records are allocated.
} MASTER_RECORD;

typedef struct _DATA_RECORD {
    RECORD_HEADER Header;
    BYTE Data[DATA_SIZE];       // Record raw data.
} DATA_RECORD;


//
//  Types of I/O for IoRecord.
//
typedef enum {
    IoRead,
    IoWrite,
    IoLock,
    IoUnlock
} IO_TYPE;


//
//  Types of operations for OperateOnRecord.
//
typedef enum {
    CreateRecord = 0,
    DeleteRecord,
    ModifyRecord,
    MaxOprRecord
} OPERATION;


//
//  Parameter block for I/Os passed to IoRecord.
//
typedef struct _IO_PARAM {
    IO_TYPE Type;
    union _IO_PARAM_PARAMS {
        struct {
            PVOID Data;
            ULONG RecSize;
        } IoInfo;
        struct {
            BOOL Exclusive;
        } LockInfo ;
    } Params;
} IO_PARAM, *PIO_PARAM;

void ErrorExitThread()
//
//  This function is called immediately after an unrecoverable error is logged.
//
{
    MSG_PRINTF(L"An error has been logged, calling ExitThread.\n");
    ExitThread(1);
}

BOOL IoRecord(HANDLE hFile, ULONG RecNumber, PIO_PARAM pIoParam)
//
//  This function performs I/O (read, write, lock or unlock) in a record, according
//  to the parameters passed in the IO_PARAM block.
//
//  Arguments:
//      hFile       - Handle to the file containing the records.
//      RecNumber   - Number of the record to be operated on.
//      pIoParam    - Pointer to IO_PARAM structure.
//
//  Return value:
//      TRUE if the I/O succeeded, FALSE if not.
//
{
    OVERLAPPED Overlapped;
    BOOL Result;
    ULARGE_INTEGER RecOffset;
    DWORD NumBytes;

    //  Initialize Overlapped.
    SecureZeroMemory(&Overlapped, sizeof(OVERLAPPED));
    Overlapped.hEvent = CreateEvent(NULL,
        FALSE,
        FALSE,
        NULL);

    if (NULL == Overlapped.hEvent) 
    {
        MSG_PRINTF(L"CreateEvent for Overlapped.hEvent failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    //  Calculate record position.
    RecOffset.QuadPart = RecNumber * RECORD_SIZE;

    Overlapped.Offset     = RecOffset.LowPart;
    Overlapped.OffsetHigh = RecOffset.HighPart;

    //  Issue the operation.
    switch (pIoParam->Type) 
    {
    case IoLock:
        Result = LockFileEx(hFile,
            pIoParam->Params.LockInfo.Exclusive ? LOCKFILE_EXCLUSIVE_LOCK : 0,
            0,
            RECORD_SIZE,
            0,
            &Overlapped);
        break;
    case IoUnlock:
        Result = UnlockFileEx(hFile,
            0,
            RECORD_SIZE,
            0,
            &Overlapped);
        break;
    case IoRead:
        Result = ReadFile(hFile,
            pIoParam->Params.IoInfo.Data,
            pIoParam->Params.IoInfo.RecSize,
            NULL,
            &Overlapped);
        break;
    case IoWrite:
        Result = WriteFile(hFile,
            pIoParam->Params.IoInfo.Data,
            pIoParam->Params.IoInfo.RecSize,
            NULL,
            &Overlapped);
        break;
    default:
        Result = FALSE;
        break;
    }

    if (!Result) 
    {
        if (GetLastError() == ERROR_IO_PENDING) 
        {
            //  Wait until the operation finishes.
            if (GetOverlappedResult(hFile,
                &Overlapped,
                &NumBytes,
                TRUE) == FALSE) 
            {
                MSG_PRINTF(L"GetOverlappedResult for Overlapped.hEvent failed with error 0x%08x.\n", 
                    GetLastError());
                ErrorExitThread();
            }
            Result = TRUE;
        } else {
            MSG_PRINTF(L"IoRecord failed with error 0x%08x. Failure passed to caller.\n", 
                GetLastError());
        }
    }
    CloseHandle(Overlapped.hEvent);
    return Result;
}


//
//  The following functions are wrappers around IoRecord, they just set the correct
//  parameters in the IO_PARAM block to correspond to the requested operation and
//  pass that to IoRecord.
//
BOOL ReadRecord(HANDLE hFile, ULONG RecNumber, PVOID Record, ULONG RecSize)
{
    IO_PARAM IoParam;

    IoParam.Type                  = IoRead;
    IoParam.Params.IoInfo.Data    = Record;
    IoParam.Params.IoInfo.RecSize = RecSize;

    return IoRecord(hFile, RecNumber, &IoParam);
}


BOOL WriteRecord(HANDLE hFile, ULONG RecNumber, PVOID Record, ULONG RecSize)
{
    IO_PARAM IoParam;

    IoParam.Type                  = IoWrite;
    IoParam.Params.IoInfo.Data    = Record;
    IoParam.Params.IoInfo.RecSize = RecSize;

    return IoRecord(hFile, RecNumber, &IoParam);
}


BOOL LockRecord(HANDLE hFile, ULONG RecNumber, BOOL Exclusive)
{
    IO_PARAM IoParam;

    IoParam.Type                      = IoLock;
    IoParam.Params.LockInfo.Exclusive = Exclusive;

    return IoRecord(hFile, RecNumber, &IoParam);
}


BOOL UnlockRecord(HANDLE hFile, ULONG RecNumber)
{
    IO_PARAM IoParam;

    IoParam.Type = IoUnlock;

    return IoRecord(hFile, RecNumber, &IoParam);
}


ULONG ReserveFirstFreeRecord(BYTE* Bitmap)
//
//  This function iterates through the bitmap and reserves the first free record
//  it can find in the bitmap.
//
//  Arguments:
//      Bitmap  - Pointer to the bitmap.
//
//  Return value:
//      Either zero, if there are no free records, or the position of the record
//      that was just reserved.
//          
{
    int i;
    BYTE Bit = 1;

    for (i = 0; i < NUM_RECORDS; i++) 
    {
        if (Bitmap[i / 8] & Bit) 
        {
            Bit <<= 1;
            if (Bit == 0) { Bit = 1; }
        } else {
            Bitmap[i / 8] |= Bit;
            return i;
        }
    }

    return 0;
}


BOOL TestBit(BYTE* Bitmap, ULONG Bit)
//
//  This function tests if a given bit is set in the bitmap.
//
//  Arguments:
//      Bitmap  - Pointer to the bitmap.
//      Bit     - Position of the bit in the bitmap.
//
//  Return value:
//      TRUE if the bit is set, FALSE otherwise.
//
{
    ULONG Byte = Bit / 8;

    Bit = Bit % 8;

    return (BOOL)(Bitmap[Byte] & (1 << Bit));
}


void ClearBit(BYTE* Bitmap, ULONG Bit)
//
//  This function clears a given bit in the bitmap.
//
//  Arguments:
//      Bitmap  - Pointer to the bitmap.
//      Bit     - Position of the bit in the bitmap.
//
{
    ULONG Byte = Bit / 8;

    Bit = Bit % 8;

    Bitmap[Byte] &= ~(1 << Bit);
}


#ifdef BRLS_DEBUG
void PrintBitmap(BYTE* Bitmap)
//
//   This function prints the whole bitmap, for debugging purposes.
//
//   Arguments:
//      Bitmap  - Pointer to the bitmap.
//
{
    int i;

    for (i = 0; i < BITMAP_SIZE; i++) 
    {
        wprintf(L"%1x", Bitmap[i]);
    }

    wprintf(L"\n");
}
#endif


void InitRecord(RECORD_HEADER* Record, BOOL Master, ULONG SeqNumber)
//
//  This function initializes a in-memory record structure with the correct
//  type code and sequence number. In case of the Master Record, the bitmap
//  is initialized too.
//
//  Arguments:
//      Record      - Pointer to the record structure.
//      Master      - TRUE if this is a Master Record, FALSE otherwise.
//      SeqNumber   - Initial sequence number.
//
{
    ULONG RecSize   = Master ? sizeof(MASTER_RECORD)   : sizeof(DATA_RECORD);
    ULONG TypeCode  = Master ? MASTER_RECORD_TYPE_CODE : DATA_RECORD_TYPE_CODE;

    SecureZeroMemory(Record, RecSize);

    Record->TypeCode  = TypeCode;
    Record->SeqNumber = Master ? 0 : SeqNumber;

    if (Master) 
    {
        ((MASTER_RECORD*)Record)->Bitmap[0] = 1;
    }
}


DATA_RECORD* PrepareRecord(ULONG SeqNumber)
//
//  This function allocates a new in-memory record structure and initializes it
//  as a brand new data record.
//
//  Arguments:
//      SeqNumber   - Sequence number with which to initialize the record.
//
//  Return value:
//      Pointer to the record structure.
//
{
    DATA_RECORD* Record = NULL;

    Record = (DATA_RECORD*) malloc(sizeof(DATA_RECORD));

    if (Record == NULL) 
    {
        MSG_PRINTF(L"Critical error: malloc for CreateRecord failed.\n");
        ErrorExitThread();
    }

    InitRecord((RECORD_HEADER*)Record, FALSE, SeqNumber);

    return Record;
}


void WriteData(DATA_RECORD* Record)
//
//  This function fills a in-memory data record structure with random data.
//  Errors do not interrupt execution.
//
//  Arguments:
//      Record  - Pointer to the record structure.
//
{
    PUINT iData;
    int i;
    errno_t err;

    iData = (PUINT)Record->Data;

    for (i = 0; i < DATA_SIZE; i += sizeof(ULONG), iData++) 
    {
        err = rand_s(iData);
        if (err != 0) 
        {
            MSG_PRINTF(L"rand_s for WriteData failed with error 0x%08x, continuing execution.\n", 
                err);
        }
    }
}


BOOL OperateOnRecord(HANDLE hFile, PULONG RecNumber, OPERATION Operation)
//
//  This function executes a high-level operation in a record (create, modify or delete).
//
//  Arguments:
//      hFile       - Handle to the file containing the record to be operated on.
//      RecNumber   - Pointer to a ULONG that either will receive the number of the
//                    record created by this operation or just contains the number
//                    of the record that will be modified or deleted.
//      Operation   - Operation to be performed (CreateRecord, ModifyRecord or
//                    DeleteRecord).
//
//  Return value:
//      TRUE if the operation succeeded, FALSE otherwise.
//
{
    BOOL Result;
    BOOL Exists;
    BOOL ExclusiveLock;
    MASTER_RECORD MasterRecord;
    DATA_RECORD*  Record;

    //  Fail operations on Master Record.
    if ((Operation != CreateRecord) && (*RecNumber == 0)) 
    {
        MSG_PRINTF(L"Cannot operate on Master Record.\n");
        return FALSE;
    }

    //  Lock Master Record. If we're just modifying a record, we can get a
    //  shared lock.
    ExclusiveLock = (Operation != ModifyRecord);

    Result = LockRecord(hFile, 0, ExclusiveLock);
    if (!Result) 
    {
        MSG_PRINTF(L"LockRecord (MasterRecord) for OperateOnRecord failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    //  Read in Master Record.
    Result = ReadRecord(hFile, 0, (PVOID)&MasterRecord, sizeof(MASTER_RECORD));
    if (!Result) 
    {
        MSG_PRINTF(L"ReadRecord (MasterRecord) for OperateOnRecord failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    if (MasterRecord.Header.TypeCode != MASTER_RECORD_TYPE_CODE) 
    {
        MSG_PRINTF(L"Master Record corruption error: wrong typecode!\n");
        ErrorExitThread();
    }

    DBG_PRINTF(L"MasterRecord bitmap (before): ");
    PrintBitmap(MasterRecord.Bitmap);

    if (Operation != CreateRecord) 
    {
        //  Test the bit in the bitmap corresponding to this record.
        Exists = TestBit(MasterRecord.Bitmap, *RecNumber);

        //  Clear the bit if we are deleting the record.
        if ((Operation == DeleteRecord) && Exists) 
        {
            ClearBit(MasterRecord.Bitmap, *RecNumber);
        }

    } else {

        //  Reserve the first free record.
        *RecNumber = ReserveFirstFreeRecord(MasterRecord.Bitmap);

        if (*RecNumber != 0) 
        {
            Exists = TRUE;
        } else {
            Exists = FALSE;
            MSG_PRINTF(L"File is full!\n");
        }
    }

    DBG_PRINTF(L"MasterRecord bitmap (after): ");
    PrintBitmap(MasterRecord.Bitmap);

    if ((Operation != ModifyRecord) && Exists) 
    {
        //  Update the Master Record's sequence number.
        MasterRecord.Header.SeqNumber++;

        //  Write Master Record down.
        Result = WriteRecord(hFile, 0, (PVOID)&MasterRecord, sizeof(MASTER_RECORD));
        if (!Result) 
        {
            MSG_PRINTF(L"WriteRecord (MasterRecord) for CreateRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }
    }

    //  Unlock Master Record.
    Result = UnlockRecord(hFile, 0);
    if (!Result) 
    {
        MSG_PRINTF(L"UnlockRecord (MasterRecord) for OperateOnRecord failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    if (!Exists) 
    {
        if (*RecNumber != 0) 
        {
            MSG_PRINTF(L"Record %d not present!\n", *RecNumber);
        }
        return FALSE;
    }

    //  For record deletion, processing is done and skip to write.
    //  Otherwise, there is more to do.
    if (Operation != DeleteRecord) 
    {
        //  Prepare a new record in memory.
        Record = PrepareRecord(1);

        //  Lock the record exclusively.
        Result = LockRecord(hFile, *RecNumber, TRUE);
        if (!Result) 
        {
            MSG_PRINTF(L"LockRecord for ModifyRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }

        if (Operation == ModifyRecord) 
        {
            //  Read the record in from the file if we're modifying it.
            Result = ReadRecord(hFile, *RecNumber, Record, RECORD_SIZE);
            if (!Result) 
            {
                MSG_PRINTF(L"ReadRecord for ModifyRecord failed with error 0x%08x.\n", 
                    GetLastError());
                ErrorExitThread();
            }

            //  Update record sequence number.
            Record->Header.SeqNumber++;
        }

        //  Write to the in-memory record.
        WriteData(Record);

        //  Write the record to the file.
        Result = WriteRecord(hFile, *RecNumber, Record, RECORD_SIZE);
        if (!Result) 
        {
            MSG_PRINTF(L"WriteRecord for ModifyRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }

        //  Unlock the record.
        Result = UnlockRecord(hFile, *RecNumber);
        if (!Result) 
        {
            MSG_PRINTF(L"UnlockRecord for ModifyRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }

        //  Free the record structure.
        free(Record);
    }

    return TRUE;
}


ULONG RandomOption(ULONG NumOpts)
//
//  This function returns a random number between 0 and (NumOpts - 1).
//  It basically is a random option select.
//
//  Arguments:
//      NumOpts - Number of options to choose from.
//
//  Return value:
//      A random option (random ULONG x | 0 <= x < NumOpts).
//
{
    UINT Random;
    errno_t err;

    err = rand_s(&Random);
    if (err != 0) 
    {
        MSG_PRINTF(L"rand_s for RandomOption failed with error 0x%08x\n", 
            err);
    }

    return Random % NumOpts;
}


DWORD WINAPI WorkerThread(PVOID data)
//
//  This is the tight loop executed by each of the threads operating in the file.
//  Each thread has its own handle to the same file. After obtaining that handle,
//  they go into a tight loop in which a record number and a record operation are
//  chosen at random and that operation is then performed in that record.
//
//  Arguments:
//      Data    - PVOID to a string containing the file name (so it can be opened).
//
//  Return value:
//      It should not return.
//
{
    HANDLE hFile;
    LPCWSTR FileName = (LPCWSTR)data;
    ULONG RecNumber;
    OPERATION Operation;
    BOOL Result;

    UINT i;

    hFile = CreateFile(FileName,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_EXISTING,
        FILE_ATTRIBUTE_NORMAL | FILE_FLAG_OVERLAPPED,
        NULL);

    if (hFile == INVALID_HANDLE_VALUE) 
    {
        MSG_PRINTF(L"CreateFile failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    //  Main loop for doing the random operations.
    for (i = 0; i < NUM_FILEOPS; i++) 
    {
        RecNumber = RandomOption(NUM_RECORDS);
        Operation = (OPERATION)RandomOption(MaxOprRecord);

        //  Output message as to what action is being attempted.
        switch (Operation) 
        {
        case CreateRecord:
            MSG_PRINTF(L"attempting record creation.\n");
            break;
        case ModifyRecord:
            MSG_PRINTF(L"attempting modification of record %d.\n", RecNumber);
            break;
        case DeleteRecord:
            MSG_PRINTF(L"attempting deletion of record %d.\n", RecNumber);
            break;
        }

        //  Perform the actual operation and handle the result, 
        //  then loop again until done.
        Result = OperateOnRecord(hFile, &RecNumber, Operation);

        if (Result) 
        {
            switch (Operation) 
            {
            case CreateRecord:
                MSG_PRINTF(L"created record %d.\n", RecNumber);
                break;

            case ModifyRecord:
                MSG_PRINTF(L"modified record %d.\n", RecNumber);
                break;

            case DeleteRecord:
                MSG_PRINTF(L"deleted record %d.\n", RecNumber);
                break;
            }
        }
    }

    CloseHandle(hFile);
    MSG_PRINTF(L"%d file operations complete. Exiting thread.\n", i);

    return 0;
}


BOOL InitNewFile(LPCWSTR FileName)
//
//  This function initializes a file with records. If the file already exists, it
//  just returns, assuming it has a valid Master Record on it. If it does not 
//  exist, a brand new file is created and initialized with a clean Master Record.
//
//  Arguments:
//      FileName    - Name of the file to be initialized.
//
//  Return value:
//      TRUE if the initialization succeeded, FALSE otherwise.
//      
{
    HANDLE hFile;
    MASTER_RECORD MasterRecord;
    DWORD BytesWritten;
    DWORD Result;

    //
    //  Create the file or open existing.
    //
    hFile = CreateFile(FileName,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_ALWAYS,
        FILE_ATTRIBUTE_NORMAL,
        NULL);

    if (INVALID_HANDLE_VALUE == hFile) 
    {
        MSG_PRINTF(L"CreateFile failed with error 0x%08x.\n", 
            GetLastError());
        return FALSE;
    } 
    else if (ERROR_ALREADY_EXISTS == GetLastError()) 
    {
        //  This is ok, simply assume it's a valid file.
        //  Note that this does not actually test that the file
        //  is valid for this application. That error is caught later.
        CloseHandle(hFile);
        return TRUE;
    } //  The implied "else" is that the handle is a good one.


    InitRecord((RECORD_HEADER*)&MasterRecord, TRUE, 0);

    Result = WriteFile(hFile,
        &MasterRecord,
        sizeof(MASTER_RECORD),
        &BytesWritten,
        NULL);

    if (!Result) 
    {
        MSG_PRINTF(L"WriteFile failed with error 0x%08x.\n", 
            GetLastError());
    }

    CloseHandle(hFile);

    return Result;
}


int __cdecl wmain(int argc, LPCWSTR argv[])
//
//  Main function. Reads file name from command line argument, initializes the file
//  and starts the worker threads, waiting for them to return.
//
{
    HANDLE gThread[NUM_THREADS];

    DWORD IdThread;
    DWORD ResultCode;
    LPCWSTR FileName = NULL;

    if (argc != 2) {
        wprintf(L"Invalid number of arguments!\n");
        wprintf(L"Usage: %ws file_name\n", argv[0]);
        return -1;
    }

    FileName = argv[1];

    if (!InitNewFile(FileName))
    {
        wprintf(L"Unable to initialize the data file %ws.\n", FileName);
    }

    wprintf(L"Main thread creating %d worker threads for processing.\n", 
        NUM_THREADS);
    for (int i = 0; i < NUM_THREADS; i++) 
    {
        gThread[i] = CreateThread(NULL,
            0,
            (LPTHREAD_START_ROUTINE)WorkerThread,
            (PVOID)FileName,
            0,
            &IdThread);
    }

    wprintf(L"Main thread waiting for worker threads to exit...\n");

    ResultCode = WaitForMultipleObjects(
        NUM_THREADS,
        gThread,
        TRUE,
        INFINITE);

    wprintf(L"WaitForMultipleObjects returned 0x%08x, execution complete.\n",
        ResultCode);

    // Do some clean-up.
    for (int i = 0; i < NUM_THREADS; i++) 
    {
        CloseHandle(gThread[i]);
    }

    return 0;
}
```



此範例是一個 Windows 主控台應用程式，它會執行多個平行存取檔案，並使用簡單的資料庫（由固定大小的數筆記錄組成），以位元組範圍鎖定進行協調。 請注意，實際的並行取決於主機系統上有多少處理器核心。

所有記錄都有前兩個共通的欄位：類型代碼和序號。 型別程式碼是兩個程式碼的其中一個： "Mstr" 程式碼是指 **主要 \_ 記錄** 類型，而「資料」程式碼則是指 **資料 \_ 記錄** 類型。 只能有一個 **主要 \_ 記錄** 和零或多個 **資料 \_ 記錄** s。 在此範例中，資料記錄中包含的資料會隨機產生。 第二個欄位（序號）會在每次修改記錄時遞增。

開始執行時，如果資料檔案不存在， **InitNewFile** 函式就會建立並初始化該資料檔。 **InitNewFile** 函式會在開頭以空的點陣圖寫入類型 Master 的記錄。 如果檔案已存在，則會開啟;假設在一開始有有效的主要記錄。

成功建立或成功開啟檔案之後，多個背景工作執行緒就會啟動，而且它們都會執行一個迴圈，其中會隨機播放作業和 a 記錄，然後再嘗試執行該記錄。 因為這些作業是隨機的，而不是全部都成功，但不一定是錯誤。 適當的狀態資訊會記錄到主控台。

可能的作業如下：建立新的記錄、修改現有的記錄，或刪除現有的記錄。 建立作業會查看點陣圖以找出第一個可用記錄，並將該記錄配置為新記錄。 修改作業會讀取點陣圖以查看該記錄是否確實存在，如果有的話，則會修改該記錄。 刪除作業會清除對應于記錄之點陣圖中的位，釋出記錄所佔用的空間供日後配置之用。 此外，這些作業分成兩個部分：存取 MasterRecord、儲存中繼資料的存取，以及資料記錄本身的存取權。

由於它們會將資料寫入資料記錄，因此記錄建立和記錄修改作業是唯一需要資料記錄存取權的作業。 基於這個理由，記錄所涵蓋的區域會在執行作業之前，以獨佔方式鎖定。 建立和刪除作業會修改點陣圖，因此只需要鎖定主要記錄。 不過，記錄修改作業只需要讀取點陣圖，而不是寫入點陣圖，以便驗證檔案是否存在。 針對該作業，主要記錄只需要共用的位元組範圍鎖定。

獨佔位元組範圍鎖定可防止檔案的所有其他控制碼進行讀取和寫入存取，這也是寫入記錄時使用它們的原因。 另一方面，共用的位元組範圍鎖定會防止所有控制碼的寫入存取，包括擁有鎖定的控制碼，但允許所有控制碼的讀取權限。

為了示範如何使用位元組範圍鎖定和檔案，此範例中的所有 i/o （除了新檔案初始化以外）都是透過非同步檔案控制代碼來完成。 這可以在 switch 語句內的 **IoLock** 和 **IoUnlock** 案例中，于 **IoRecord** 函數中看到。 [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)和 [**UnlockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfileex)函式會搭配重 [**迭的 i/o**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry)模型使用，方法是將重迭的結構傳遞給它們（其具有鎖定範圍開頭的位移），以及除非函式立即傳回，否則會授與在該範圍鎖定之後發出信號的事件。

發出非同步 i/o 要求之後， **IoRecord** 函式中的下一個作業就是以內嵌方式等候作業。 如果需要最大效能，這通常是次佳的案例，在這裡使用是為了簡化。 在實際執行的應用程式中，建議使用 [i/o 完成埠](i-o-completion-ports.md) 或類似的機制，因為它會在 i/o 完成時釋放執行緒以進行其他處理。

此範例會在執行 **NUM \_ FILEOPS** random 作業之後結束。 每個執行緒都會將其終止狀態記錄為錯誤狀況或正常終止。 請注意，並非所有的執行緒都會同時結束，視主機系統擁有的處理器核心數目和 i/o 子系統的速度而定。

 

 



