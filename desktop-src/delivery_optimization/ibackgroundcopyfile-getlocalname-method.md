---
title: 'IBackgroundCopyFile GetLocalName 方法 (>deliveryoptimization .h) '
description: 抓取檔案的本機名稱。
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- GetLocalName 方法
- GetLocalName 方法，IBackgroundCopyFile 介面
- IBackgroundCopyFile 介面，GetLocalName 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetLocalName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d8c3f3e6a722c7d98fffd5904b398a9573b7a809225e35ae89b5910eb965f5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953598"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a>IBackgroundCopyFile：： GetLocalName 方法

抓取檔案的本機名稱。

## <a name="syntax"></a>語法


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppName* \[擴展\]
</dt> <dd>

以 Null 終止的字串，其中包含用戶端上的檔案名。 名稱是完整的。 完成時，呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 函式以釋放 *ppName* 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile 定義為01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile::GetRemoteName**](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

