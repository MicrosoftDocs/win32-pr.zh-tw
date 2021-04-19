---
description: 抓取離線檔案快取的狀態。
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: CSCQueryDatabaseStatus 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000932"
---
# <a name="cscquerydatabasestatus-function"></a>CSCQueryDatabaseStatus 函式

\[這項功能不受支援，因此不應該使用。\]

抓取離線檔案快取的狀態。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pulStatus* 
</dt> <dd>

狀態。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                                               | 意義                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <dt>**旗 \_ 標DATABASESTATUS \_ 加密**</dt>的 <dt>0x00000002</dt> </dl>                                      | 快取會標示為加密，而且快取中的所有檔案都會加密。<br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <dt>**旗 \_ 標DATABASESTATUS \_ 部分 \_ 加密**</dt>的 <dt>0x00000004</dt> </dl>       | 快取會標示為加密，但快取中的某些檔案並不會加密。<br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <dt>**旗 \_ 標DATABASESTATUS \_ 部分 \_ 未加密**</dt>的 <dt>0x00000004</dt> </dl> | 快取未標示為加密，但尚未解密快取中的所有檔案。<br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <dt>**旗 \_ 標DATABASESTATUS \_ 未加密**</dt>的 <dt>0x00000000</dt> </dl>                                | 快取未標示為加密，而且快取中的所有檔案都已解密。<br/>      |



 

</dd> <dt>

*pulErrors* 
</dt> <dd>

如果發生內部資料庫錯誤，此參數為非零值，否則為0。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSCIsCSCEnabled**](csciscscenabled.md)
</dt> </dl>

 

 
