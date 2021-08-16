---
description: 抓取所指定檔案物件的基本屬性。
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: NtQueryAttributesFile 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: e6b1ecdc7cc7f0a5c18afc3eeb613c3f9cd9a38aa22a876ad156c3d1c6b1bc97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826804"
---
# <a name="ntqueryattributesfile-function"></a>NtQueryAttributesFile 函式

\[您可以從 Windows 中變更或移除此函式，而不需另行通知。\]

抓取所指定檔案物件的基本屬性。

## <a name="syntax"></a>語法


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ObjectAttributes* \[在\]
</dt> <dd>

[物件 \_ 屬性](https://msdn.microsoft.com/library/aa491657.aspx)結構的指標，此結構會提供要用於檔案物件的屬性。

</dd> <dt>

*FileInformation* \[擴展\]
</dt> <dd>

[File \_ 基本 \_ 資訊](https://msdn.microsoft.com/library/aa491634.aspx)結構的指標，用來接收傳回的檔案屬性資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 NTSTATUS 或錯誤碼。

在 WDK 中可用的 Ntstatus 標頭檔中，會列出 NTSTATUS 錯誤碼的表單和重要性，並會在 WDK 檔中說明。

## <a name="remarks"></a>備註

此函數沒有相關聯的標頭檔。 相關聯的匯入程式庫（Ntdll.dll）可在 WDK 中使用。 您也可以使用 [**LoadLibrary**](-loadlibrary.md) 和 [**GetProcAddress**](-getprocaddress-.md) 函數，動態連結至 Ntdll.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




