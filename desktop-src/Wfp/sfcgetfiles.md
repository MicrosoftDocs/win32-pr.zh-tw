---
description: 列出受保護的檔案。
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: 'SfcGetFiles 函式 (Sfcfiles) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 6b38b761372db656308e778fd96ea48607cf1f21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849860"
---
# <a name="sfcgetfiles-function"></a>SfcGetFiles 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 這項功能的支援已在 Windows Vista 和 Windows Server 2008 中移除。 請改用 [WRP](wfp-functions.md) 函式中所列的支援函數。\]

列出受保護的檔案。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProtFileData* \[擴展\]
</dt> <dd>

[**PPROTECT 檔案 \_ \_ 專案**](pprotect-file-entry.md)結構的指標，其中包含受保護的檔案清單。

</dd> <dt>

*FileCount* \[擴展\]
</dt> <dd>

包含受保護檔案數目之 ULONG 值的位置指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「狀態 \_ 成功」。 如果函式失敗，則會傳回適當的 NTSTATUS 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Sfcfiles。h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Sfcfiles.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PPROTECT \_ 檔案 \_ 專案**](pprotect-file-entry.md)
</dt> </dl>

 

 




