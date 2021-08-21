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
ms.openlocfilehash: c9070290170febf08e532b071812600fb0ef8755302a4bd1603858659196d0c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053196"
---
# <a name="pprotect_file_entry-structure"></a>PPROTECT \_ 檔案 \_ 專案結構

\[此結構可在 [需求] 區段中指定的作業系統中使用。 Windows Vista 和 Windows Server 2008 已移除對此結構的支援。 請改用 [WRP](wfp-functions.md) 函式中所列的支援函數。\]

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
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                 |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Sfcfiles。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SfcGetFiles**](sfcgetfiles.md)
</dt> </dl>

 

 




