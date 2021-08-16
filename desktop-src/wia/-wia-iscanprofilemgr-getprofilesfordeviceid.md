---
description: 取得與裝置相關聯的所有掃描設定檔。
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: 'IScanProfileMgr：： GetProfilesforDeviceID 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 8ca150d02aff2f84becf8b36aca87e2da24b2b83c9ccd85c0cf5a1c5ced0d664
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209054"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a>IScanProfileMgr：： GetProfilesforDeviceID 方法

取得與裝置相關聯的所有掃描設定檔。

## <a name="syntax"></a>語法


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrDeviceID* \[在\]
</dt> <dd>

類型： **BSTR**

裝置的識別碼。

</dd> <dt>

*pulNumProfiles* \[in、out\]
</dt> <dd>

類型： **ULONG \***

傳遞時，為要傳回的最大設定檔數目的指標。 傳回時，為所傳回設定檔數目的指標。

</dd> <dt>

*ppScanProfile* \[擴展\]
</dt> <dd>

類型： **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

設定檔陣列的指標位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果與裝置相關聯的設定檔總數小於傳遞給 *pulNumProfiles* 的值，則 *pulNumProfiles* 會傳回該總計。 否則，它會傳回與傳遞給它相同的值。

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

 

 




