---
description: 刪除您的應用程式執行所在系統中使用者可用的所有掃描設定檔。
ms.assetid: 1a79fd0e-1309-4fc4-863f-6dfb20594d91
title: 'IScanProfileMgr：:D eleteAllProfilesForUser 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfilesForUser
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 967a2ca3e2ed313c024f52cec6d8064c702c6caedc122ce7bd4409f3408ec995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209098"
---
# <a name="iscanprofilemgrdeleteallprofilesforuser-method"></a>IScanProfileMgr：:D eleteAllProfilesForUser 方法

刪除您的應用程式執行所在系統中使用者可用的所有掃描設定檔。

## <a name="syntax"></a>語法


```C++
HRESULT DeleteAllProfilesForUser();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

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

 

 




