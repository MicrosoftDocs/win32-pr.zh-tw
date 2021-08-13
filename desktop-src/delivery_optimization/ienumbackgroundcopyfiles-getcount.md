---
title: 'IEnumBackgroundCopyFiles GetCount 方法 (>deliveryoptimization .h) '
description: 捕獲列舉中的檔案數目計數。
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- GetCount 方法
- GetCount 方法，IEnumBackgroundCopyFiles 介面
- IEnumBackgroundCopyFiles 介面，GetCount 方法
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f67ee932079a7c67619fe769cbe5d1b6705261655853f1adccb14bf5d12eecf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409908"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a>IEnumBackgroundCopyFiles：： GetCount 方法

捕獲列舉中的檔案數目計數。

## <a name="syntax"></a>語法


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCount* \[擴展\]
</dt> <dd>

列舉中的檔案數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles 定義為 CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





