---
description: 在指定的模組中，判斷具有指定之類型和名稱之資源的位置。
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: FindResourceWrapW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 8f76d516570725fe6da5e8a21ec5a29699276ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192702"
---
# <a name="findresourcewrapw-function"></a>FindResourceWrapW 函式

\[**FindResourceWrapW** 可用於 Windows XP。 在後續版本中可能無法使用。 您應該改為使用 [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) 。\]

在指定的模組中，判斷具有指定之類型和名稱之資源的位置。

> [!Note]  
> **FindResourceWrapW** 是 **FindResourceW** 函數的包裝函式。 如需進一步的使用注意事項，請參閱 [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) 。

 

## <a name="syntax"></a>語法


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hModule* \[在\]
</dt> <dd>

類型： **HMODULE**

模組的控制碼，可執行檔包含資源。 **Null** 值會指定與作業系統用來建立目前進程的影像檔相關聯的模組控制碼。

</dd> <dt>

*lpName* \[在\]
</dt> <dd>

類型： **LPCWSTR**

資源名稱。 如需詳細資訊，請參閱 [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea)。

</dd> <dt>

*lpType* \[在\]
</dt> <dd>

類型： **LPCWSTR**

指定資源類型之字串的指標。 如需詳細資訊，請參閱 [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRSRC**

如果函式成功，則傳回值是指定資源之資訊區塊的控制碼。 若要取得資源的控制碼，請將此控制碼傳遞給 [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) 函數。

如果函式失敗，則傳回值為 **Null**。 若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。

## <a name="remarks"></a>備註

如果您需要指定特定的當地語系化，請使用 [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) 函式，而不是 **FindResourceWrapW**。

**FindResourceWrapW** 提供在舊版作業系統中使用 Unicode 字串的能力。 慣用的方法是使用 [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。

您必須使用序數66，直接從 Shlwapi.dll 呼叫 **FindResourceWrapW** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>None</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (5.0 版或更新版本) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **FindResourceWrapW** (Unicode) <br/>                                                                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
