---
description: 取得裝置的掃描設定檔數目。
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: 'IScanProfileMgr：： GetNumProfilesforDeviceID 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: c2af1e4bc73afee090d947e6bcca0060521cb15cf2faff06be8c9a893534ea4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119264388"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a>IScanProfileMgr：： GetNumProfilesforDeviceID 方法

取得裝置的掃描設定檔數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrDeviceID* \[在\]
</dt> <dd>

類型： **BSTR**

裝置的識別碼。

</dd> <dt>

*pulNumProfiles* \[擴展\]
</dt> <dd>

類型： **ULONG \***

裝置可用設定檔數目的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Scanprofilemgr。h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[掃描設定檔架構](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




