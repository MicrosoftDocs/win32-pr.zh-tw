---
description: 包含磁片區開機磁區中儲存的磁片上檔案系統辨識資訊 (邏輯磁片磁區零) 。
ms.assetid: d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac
title: FILE_SYSTEM_RECOGNITION_STRUCTURE 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_SYSTEM_RECOGNITION_STRUCTURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c542b2b9ee1cd1696c7c95797c7df20aa02180cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026509"
---
# <a name="file_system_recognition_structure-structure"></a>檔 \_ 系統 \_ 識別 \_ 結構結構

包含磁片區開機磁區中儲存的磁片上檔案系統辨識資訊 (邏輯磁片磁區零) 。

這是在公用標頭中無法使用的內部定義資料結構，在此提供給想要利用檔案系統識別的檔案系統開發人員使用。 如需詳細資訊，請參閱 [檔案系統識別](file-system-recognition.md)。

## <a name="syntax"></a>語法


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE;
```



## <a name="members"></a>成員

<dl> <dt>

**Jmp**
</dt> <dd>

JMP 指令。 總和 **檢查** 碼資料成員所包含的值中不會包含此資料成員。

</dd> <dt>

**FsName**
</dt> <dd>

檔案系統名稱。 這是8個 ASCII 字元的序列，代表磁片區所格式化之檔案系統的 nonlocalizable 人類可讀取名稱。

此字串與具有一般 BIOS 參數區塊 (BPB) 結構的磁片上的 OEM 檔案系統名稱相同。

</dd> <dt>

**MustBeZero**
</dt> <dd>

包含所有零的保留空間。

此資料成員會與 BPB 中的下列資料成員正常地重迭：

-   **BytesPerSector**
-   **SectorsPerCluster**
-   **ReservedSectorCount**

因為這些資料成員會設定為零，所以這應該就足以讓較早的 Os 結束，因為這不是有效的 BPB，因此可辨識磁片區。

</dd> <dt>

**識別碼**
</dt> <dd>

結構識別碼。 必須包含以位元組由大到小的位元組順序排列的值0x53525346。

在結構中的這個位置，資料會對齊16個位元組。

</dd> <dt>

**長度**
</dt> <dd>

此結構中從開頭到結尾的位元組數目，包括 **Jmp** 資料成員。

</dd> <dt>

**校驗**
</dt> <dd>

從 **FsName** 資料成員開始算起的位元組的雙位元組總和檢查碼，並且在此結構的最後一個位元組結尾，但不包括 **Jmp** 和總和 **檢查** 碼的資料成員。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[計算檔案系統識別總和檢查碼](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[檔案系統識別](file-system-recognition.md)
</dt> <dt>

[**檔 \_ 系統 \_ 識別 \_ 資訊**](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[**FSCTL \_ 查詢 \_ 檔 \_ 系統 \_ 識別**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

