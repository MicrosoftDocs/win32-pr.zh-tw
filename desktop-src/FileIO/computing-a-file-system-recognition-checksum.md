---
description: 檔 \_ 系統辨識 \_ \_ 結構結構（由 Windows 在內部定義，且由檔案系統辨識 (FRS) ）包含必須正確計算的總和檢查碼值，以便讓 FRS 正常地與指定的無法辨識檔案系統搭配使用。
ms.assetid: 8f76784f-7d03-4874-ae7f-e8bdc42638c3
title: 計算檔案系統識別總和檢查碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce146fda589668d39f1f7ff4158384986fb719f2bbbee6ce0584ad9f1e540b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329178"
---
# <a name="computing-a-file-system-recognition-checksum"></a>計算檔案系統識別總和檢查碼

[**檔 \_ 系統辨識 \_ \_ 結構**](file-system-recognition-structure.md)結構（由 Windows 在內部定義，且由 [檔案系統](file-system-recognition.md)辨識 (FRS) ）包含必須正確計算的總和檢查碼值，以便讓 FRS 正常地與指定的無法辨識檔案系統搭配使用。 下列範例會完成此計算。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案系統識別](file-system-recognition.md)
</dt> <dt>

[**檔 \_ 系統 \_ 識別 \_ 結構**](file-system-recognition-structure.md)
</dt> </dl>

 

 



