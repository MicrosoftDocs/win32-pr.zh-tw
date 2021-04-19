---
description: SfcGetFiles 函數所使用的結構。
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: 'PPROTECT_FILE_ENTRY 結構 (Sfcfiles .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000127"
---
# <a name="pprotect_file_entry-structure"></a>PPROTECT \_ 檔案 \_ 專案結構

\[此結構可在 [需求] 區段中指定的作業系統中使用。 此結構的支援已在 Windows Vista 和 Windows Server 2008 中移除。 請改用 [WRP](wfp-functions.md) 函式中所列的支援函數。\]

[**SfcGetFiles**](sfcgetfiles.md)函數所使用的結構。

## <a name="syntax"></a>語法


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a>成員

<dl> <dt>

**SourceFileName**
</dt> <dd>

字串值的指標，其中包含原始程式檔的檔案名。 如果未在安裝時重新命名檔案，則這會是 **Null** 。

</dd> <dt>

**FileName**
</dt> <dd>

字串值的指標，其中包含目的地檔案名以及檔案的完整路徑。

</dd> <dt>

**InfName**
</dt> <dd>

字串值的指標，其中包含提供版面配置資訊的 INF 檔案名。 使用預設版面配置時，此參數可能是 **Null** 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                 |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Sfcfiles。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SfcGetFiles**](sfcgetfiles.md)
</dt> </dl>

 

 




