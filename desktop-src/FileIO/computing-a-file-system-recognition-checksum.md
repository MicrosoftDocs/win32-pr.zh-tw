---
description: 檔 \_ 系統辨識 \_ \_ 結構結構（由 Windows 在內部定義，且由檔案系統辨識 (FRS) ）包含必須正確計算的總和檢查碼值，以便讓 FRS 正常地與指定的無法辨識檔案系統搭配使用。
ms.assetid: 8f76784f-7d03-4874-ae7f-e8bdc42638c3
title: 計算檔案系統識別總和檢查碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cac3975d4e1845dd1ff4aa218526e942fda152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945430"
---
# <a name="computing-a-file-system-recognition-checksum"></a><span data-ttu-id="e73c0-103">計算檔案系統識別總和檢查碼</span><span class="sxs-lookup"><span data-stu-id="e73c0-103">Computing a File System Recognition Checksum</span></span>

<span data-ttu-id="e73c0-104">[**檔 \_ 系統辨識 \_ \_ 結構**](file-system-recognition-structure.md)結構（由 Windows 在內部定義，且由 [檔案系統](file-system-recognition.md)辨識 (FRS) ）包含必須正確計算的總和檢查碼值，以便讓 FRS 正常地與指定的無法辨識檔案系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="e73c0-104">The [**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**](file-system-recognition-structure.md) structure, defined internally by Windows and used by [file system recognition](file-system-recognition.md) (FRS), contains a checksum value that must be properly computed for FRS to work properly with a specified unrecognized file system.</span></span> <span data-ttu-id="e73c0-105">下列範例會完成此計算。</span><span class="sxs-lookup"><span data-stu-id="e73c0-105">The following example accomplishes this computation.</span></span>


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE, *PFILE_SYSTEM_RECOGNITION_STRUCTURE;

USHORT ComputeFileSystemInformationChecksum (
    __in PFILE_SYSTEM_RECOGNITION_STRUCTURE Fsrs
    )

/*++

Routine Description:

    This routine computes the file record checksum.

Arguments:

    Fsrs - Pointer to the record.

Return Value:

    The checksum result.

--*/

{
    USHORT Checksum = 0;
    USHORT i;
    PUCHAR Buffer = (PUCHAR)Fsrs;
    USHORT StartOffset;

    //
    //  Skip the jump instruction
    //

    StartOffset = FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, FsName);
    
    for (i = StartOffset; i < Fsrs->Length; i++) {

        //
        //  Skip the checksum field itself, which is a USHORT.
        //

        if ((i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)) ||
            (i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)+1)) {

            continue;
        }

        Checksum = ((Checksum & 1) ? 0x8000 : 0) + (Checksum >> 1) + Buffer[i];
    }

    return Checksum;
}
```



## <a name="related-topics"></a><span data-ttu-id="e73c0-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="e73c0-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e73c0-107">檔案系統識別</span><span class="sxs-lookup"><span data-stu-id="e73c0-107">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="e73c0-108">**檔 \_ 系統 \_ 識別 \_ 結構**</span><span class="sxs-lookup"><span data-stu-id="e73c0-108">**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**</span></span>](file-system-recognition-structure.md)
</dt> </dl>

 

 



