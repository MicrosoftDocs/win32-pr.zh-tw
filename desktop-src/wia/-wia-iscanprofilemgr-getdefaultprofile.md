---
description: 取得預設掃描設定檔。
ms.assetid: 0e5ca06a-78ca-4d24-8dda-26babc3124b5
title: 'IScanProfileMgr：： GetDefaultProfile 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetDefaultProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a496a2e606e389f8b2e1dfd7808d56e4360108a27ef66fbc0937ef1040514e44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549758"
---
# <a name="iscanprofilemgrgetdefaultprofile-method"></a>IScanProfileMgr：： GetDefaultProfile 方法

取得預設掃描設定檔。

## <a name="syntax"></a>語法


```C++
HRESULT GetDefaultProfile(
  [in]  BSTR         bstrDeviceID,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrDeviceID* \[在\]
</dt> <dd>

類型： **BSTR**

裝置的識別碼。

</dd> <dt>

*ppScanProfile* \[擴展\]
</dt> <dd>

類型： **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

裝置預設設定檔指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

預設設定檔有一個 `<Default>` 元素。

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

 

 




