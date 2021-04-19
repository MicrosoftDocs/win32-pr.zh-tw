---
description: 將指定的離線登錄 hive 寫入檔案。
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: 'ORSaveHive 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 59df5b191a9bc0cfe98e1681665c5814935aa2c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992805"
---
# <a name="orsavehive-function"></a>ORSaveHive 函式

將指定的離線登錄 hive 寫入檔案。

## <a name="syntax"></a>語法


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*控制碼* \[在\]
</dt> <dd>

離線登錄 hive 要儲存的控制碼。

</dd> <dt>

*lpHivePath* \[在\]
</dt> <dd>

Unicode 字串的指標，指定登錄 hive 檔案的名稱。 這不可以是現有檔案的名稱。

</dd> <dt>

*dwOsMajorVersion* \[在\]
</dt> <dd>

作業系統的主要版本號碼。 這個成員可以是下列其中一個值。



| 值                                                                        | 意義                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>5</dt> </dl> | 如果 *dwOsMinorVersion* 是1，則作業系統是 Windows XP。<br/> 如果 *dwOsMinorVersion* 為2，則作業系統為 windows Server 2003 R2、windows server 2003 或 Windows XP Professional x64 Edition。<br/> |
| <dl> <dt>6</dt> </dl> | 如果 *dwOsMinorVersion* 為0，則作業系統是 windows Server 2008 或 windows Vista。<br/> 如果 *dwOsMinorVersion* 是1，則作業系統是 windows Server 2008 R2 或 windows 7。<br/>                       |



 

</dd> <dt>

*dwOsMinorVersion* \[在\]
</dt> <dd>

作業系統的次要版本號碼。 這個成員可以是下列其中一個值。



| 值                                                                        | 意義                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 如果 *dwOsMajorVersion* 為6，則作業系統是 windows Server 2008 或 windows Vista。<br/>                                                                                                                                          |
| <dl> <dt>1</dt> </dl> | 如果 *dwOsMajorVersion* 是5，則作業系統是 Windows XP。<br/> 如果 *dwOsMajorVersion* 為6，則作業系統是 windows Server 2008 R2 或 windows 7。<br/>                                                                |
| <dl> <dt>2</dt> </dl> | 如果 *dwOsMajorVersion* 是5，則作業系統是 windows Server 2003 R2、windows server 2003 或 Windows XP Professional x64 Edition。 <br/> 如果 *dwOsMajorVersion* 為6， *dwOsMinorVersion* 參數必須是0或1。 <br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。 可能的錯誤代碼包括下列各項：

-   如果呼叫端沒有寫入檔案的必要存取權限，則函式會傳回 \_ 拒絕存取錯誤 \_ 。
-   如果指定的檔案已經存在，則函數會傳回 \_ 錯誤 \_ 。

## <a name="remarks"></a>備註

您必須使用 **ORSaveHive** 函式來儲存對離線登錄 hive 進行的變更。 在呼叫 **ORSaveHive** 將 hive 儲存至檔案之前，不會保留變更。

*DwOsMajorVersion* 和 *dwOsMinorVersion* 參數會一起指定登錄 hive 檔案的目標格式。 下表摘要說明最新的作業系統版本號碼。



| 作業系統                    | 版本號碼 |
|-------------------------------------|----------------|
| Windows Server 2008 R2              | 6.1            |
| Windows 7                           | 6.1            |
| Windows Server 2008                 | 6.0            |
| Windows Vista                       | 6.0            |
| Windows Server 2003 R2              | 5.2            |
| Windows Server 2003                 | 5.2            |
| Windows XP Professional x64 Edition | 5.2            |
| Windows XP                          | 5.1            |



 

使用 [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) 函式取出目前作業系統的相關資訊。

**ORSaveHive** 函式會在將 hive 寫入檔案時鎖定登錄 hive，然後關閉檔案並釋放鎖定。 登錄 hive 會保留在記憶體中，直到透過呼叫 [**ORCloseHive**](orclosehive.md) 函式關閉為止。 您可以在登錄 hive 開啟時進行進一步的變更;不過，若要保留這些變更，必須將 hive 儲存至新的檔案，因為 **ORSaveHive** 函式不會覆寫現有的檔案。

**ORSaveHive** 函式可用於儲存離線登錄 hive 的一部分。 *控制碼* 參數中所指定的索引鍵會成為 hive 的根機碼，其中包含指定的索引鍵及其所有子機碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Offline Registry library 1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 
