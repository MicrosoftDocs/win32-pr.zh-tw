---
description: 重新列舉系統中的所有掃描設定檔。
ms.assetid: f5e49645-e81a-4750-8ea5-f0c698a61752
title: 'IScanProfileMgr：： Refresh 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.Refresh
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 5bb343d310be3aa352c4777275c231f6264d6d25fe5ad88cde559995da915aa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208941"
---
# <a name="iscanprofilemgrrefresh-method"></a>IScanProfileMgr：： Refresh 方法

重新列舉系統中的所有掃描設定檔。

## <a name="syntax"></a>語法


```C++
HRESULT Refresh();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當有一個以上的 [**IScanProfileMgr**](-wia-iscanprofilemgr.md) 物件可能同時建立或刪除設定檔時，請使用這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Scanprofilemgr。h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[掃描設定檔架構](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




