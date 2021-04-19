---
description: 開啟現有的目錄物件。
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: NtOpenDirectoryObject 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ceea03c36e0617e2f48887275e7867e3589c87ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995643"
---
# <a name="ntopendirectoryobject-function"></a>NtOpenDirectoryObject 函式

\[這項功能可能會在未來變更或無法使用。\]

開啟現有的目錄物件。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI NtOpenDirectoryObject(
  _Out_ PHANDLE            DirectoryHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DirectoryHandle* \[擴展\]
</dt> <dd>

新開啟的目錄物件的控制碼。

</dd> <dt>

*DesiredAccess* \[在\]
</dt> <dd>

[**存取 \_ 遮罩**](../secauthz/access-mask.md)，指定要求的目錄物件存取權。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                                                                                                                      | 意義                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <dt>**目錄 \_查詢**</dt> <dt>0x0001</dt> </dl>                                            | 查詢目錄物件的存取權。<br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <dt>**目錄 \_遍歷**</dt> <dt>0x0002</dt> </dl>                                   | 目錄物件的名稱查閱存取。<br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <dt>**目錄 \_建立 \_ 物件**</dt> <dt>0x0004</dt> </dl>                   | 目錄物件的名稱建立存取權。<br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <dt>**目錄 \_建立 \_ 子目錄**</dt> <dt>0x0008</dt> </dl> | 目錄物件的子目錄建立存取權。<br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <dt>**目錄 \_需要所有 \_ 存取**</dt><dt>標準 \_ 許可權 \_ \| 0xF</dt> </dl> | 上述擁有權限加上 **\_ \_ 所需的標準許可權**。<br/> |



 

</dd> <dt>

*ObjectAttributes* \[在\]
</dt> <dd>

目錄物件的屬性。 若要初始化 **物件 \_ 屬性** 結構，請使用 **InitializeObjectAttributes** 宏。 如需詳細資訊，請參閱 WDK 檔中的這些專案的說明文件。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回狀態 \_ 成功或錯誤狀態。 可能的狀態碼包括下列各項。



| 傳回碼                                                                                                       | Description                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**狀態 \_ 不足的 \_ 資源**</dt> </dl>    | 無法配置此函數所需的暫存緩衝區。<br/>                                                                                                                                                                                                                           |
| <dl> <dt>**狀態 \_ 不正確 \_ 參數**</dt> </dl>         | 指定的 ObjectAttributes 參數為 **Null** 指標，而不是 **物件 \_ 屬性** 結構的有效指標，或 **物件 \_ 屬性** 結構中指定的部分成員無效。<br/>                                                                          |
| <dl> <dt>**狀態 \_ 物件 \_ 名稱 \_ 無效**</dt> </dl>      | *ObjectAttributes* 參數包含 **物件 \_ 屬性** 結構中的 **ObjectName** 成員，因為在 **物件 \_ 名稱 \_ 路徑 \_ 分隔符號** 之後找到空字串，所以無效。<br/>                                                                        |
| <dl> <dt>**\_ \_ \_ \_ 找不到狀態物件名稱**</dt> </dl>   | *ObjectAttributes* 參數包含 **物件 \_ 屬性** 結構中找不到的 **ObjectName** 成員。<br/>                                                                                                                                                           |
| <dl> <dt>**\_ \_ \_ \_ 找不到狀態物件路徑**</dt> </dl>   | *ObjectAttributes* 參數在 **物件 \_ 屬性** 結構中包含的 **ObjectName** 成員具有找不到的物件路徑。 <br/>                                                                                                                                      |
| <dl> <dt>**狀態 \_物件 \_ 路徑 \_ 語法不 \_ 正確**</dt> </dl> | *ObjectAttributes* 參數未包含 **RootDirectory** 成員，但是 **物件 \_ 屬性** 結構中的 **ObjectName** 成員是空字串，或未包含 **物件 \_ 名稱 \_ 路徑 \_ 分隔符號**。 這表示物件路徑的語法不正確。<br/> |



 

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NtQueryDirectoryObject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
