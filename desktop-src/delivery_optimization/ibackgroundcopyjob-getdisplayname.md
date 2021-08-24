---
title: 'IBackgroundCopyJob GetDisplayName 方法 (>deliveryoptimization .h) '
description: 捕獲作業的顯示名稱。 一般而言，您會使用顯示名稱來識別使用者介面中的作業。
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName 方法
- GetDisplayName 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetDisplayName 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a50d2bdc1c492725b79368774f07755c7b629d73209a7d53f865cc738eb7025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755538"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a>IBackgroundCopyJob：： GetDisplayName 方法

捕獲作業的顯示名稱。 一般而言，您會使用顯示名稱來識別使用者介面中的作業。

## <a name="syntax"></a>語法


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppDisplayName* \[擴展\]
</dt> <dd>

以 Null 終止的字串，其中包含識別作業的顯示名稱。 有一個以上的作業可以有相同的顯示名稱。 完成時，呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 函式以釋放 *ppDisplayName* 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                                  | 描述                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>     | 已成功取出顯示名稱。<br/>          |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | *PpDisplayName* 參數不可為 **Null**。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

