---
description: 將字串轉換成 GUID。
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: GUIDFromString 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: a29a2138f4bcc7435a0d7864f65dd60ab16519c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849201"
---
# <a name="guidfromstring-function"></a>GUIDFromString 函式

\[**GUIDFromString** 可透過 Windows XP Service Pack 2 (SP2) 或 windows Vista 取得。 它可能會在後續版本中變更或無法使用。 應用程式應該使用 [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) 或 [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) 來取代此函式。\]

將字串轉換成 GUID。

## <a name="syntax"></a>語法


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*psz* \[在\]
</dt> <dd>

類型： **LPCTSTR**

要轉換之以 null 結束的字串指標。 字串的格式應該如下：

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

*pguid* \[擴展\]
</dt> <dd>

類型： **LPGUID**

當此方法傳回時，用來接收 GUID 之緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **BOOL**

如果已成功建立 GUID，則 **為 TRUE** ;否則 **為 FALSE**。

## <a name="remarks"></a>備註

這個函式不是在標頭中宣告，也不是由 .dll 檔中的名稱所匯出。 它必須從 Shell32.dll 載入為 **GUIDFromStringA** 的序數703，以及 **GUIDFromStringW** 的序數704。

您也可以從 Shlwapi.dll 將其存取為 **GUIDFromStringA** 的序數269，以及 **GUIDFromStringW** 的序數270。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **GUIDFromStringW** (Unicode) 和 **GUIDFromStringA** (ANSI) <br/>                |



 

 
