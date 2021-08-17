---
title: 'IBackgroundCopyFile GetRemoteName 方法 (>deliveryoptimization .h) '
description: 抓取檔案的遠端名稱。
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- GetRemoteName 方法
- GetRemoteName 方法，IBackgroundCopyFile 介面
- IBackgroundCopyFile 介面，GetRemoteName 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e84827f4c1144c4242f382aff822984b24dd83610c1ebd5d2540ba7c4ca65d2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810328"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a>IBackgroundCopyFile：： GetRemoteName 方法

抓取檔案的遠端名稱。

## <a name="syntax"></a>語法


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppName* \[擴展\]
</dt> <dd>

以 Null 終止的字串，其中包含要傳送之檔案的遠端名稱。 名稱是完整的。 完成時，呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 函式以釋放 *ppName* 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM **HRESULT** 值。

## <a name="remarks"></a>備註

若要變更遠端檔案名，請呼叫 [**IBackgroundCopyFile2：： SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) 方法。

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

[**IBackgroundCopyFile：： GetLocalName**](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

