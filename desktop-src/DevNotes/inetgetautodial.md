---
description: InetGetAutodial 函式會從登錄傳回自動撥號設定。
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: InetGetAutodial 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 15267cd00940f0386c8a5d9c0c54b070f2cff509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995415"
---
# <a name="inetgetautodial-function"></a>InetGetAutodial 函式

\[這項功能不受支援，而且可能會在未來的 Windows 版本中變更或無法使用。 \]

**InetGetAutodial** 函式會從登錄傳回自動撥號設定。

## <a name="syntax"></a>語法


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpfEnable* \[擴展\]
</dt> <dd>

指出是否已啟用自動撥號。 傳回 **TRUE** 時，表示已啟用自動撥號。

</dd> <dt>

*lpszEntryName* \[擴展\]
</dt> <dd>

傳回時，包含為自動撥號設定的電話簿專案名稱。

</dd> <dt>

*cbEntryNameSize* \[在\]
</dt> <dd>

來電者為電話簿專案名稱所配置的緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數可以傳回其中一個值。



| 傳回碼                                                                                                | Description                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 成功**</dt> </dl>              | 呼叫成功。<br/>                                                                                                                       |
| <dl> <dt>**錯誤 \_ 的 \_ 引數錯誤**</dt> </dl>       | *lpfEnable* 或 *lpszEntryName* 包含 **Null** 指標，或 *cbEntryNameSize* 的值為零。<br/>                                         |
| <dl> <dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt> </dl>  | 記憶體不足，無法配置內部緩衝區。<br/>                                                                                    |
| <dl> <dt>**\_緩衝區不足的錯誤 \_**</dt> </dl> | *cbEntryNameSize* 並不表示 *lpszEntryName* 所指向的緩衝區夠大，無法接收電話簿專案的名稱。<br/> |



 

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Inetcfg.dll</dt> </dl> |



 

 
