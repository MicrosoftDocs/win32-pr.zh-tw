---
description: 取得您的應用程式執行所在系統中使用者可用的所有掃描設定檔。
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'IScanProfileMgr：： >ipartner.getprofiles 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 13949fe08dd547ecb5319e18ecc84139ccd310bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693071"
---
# <a name="iscanprofilemgrgetprofiles-method"></a>IScanProfileMgr：： >ipartner.getprofiles 方法

取得您的應用程式執行所在系統中使用者可用的所有掃描設定檔。

## <a name="syntax"></a>語法


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pulNumProfiles* \[in、out\]
</dt> <dd>

類型： **ULONG \** _

傳遞時，為要傳回的最大設定檔數目的指標。 傳回時，為所傳回設定檔數目的指標。

</dd> <dt>

_ppScanProfile * \[ out\]
</dt> <dd>

類型： **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

設定檔指標陣列的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果使用者可用的設定檔總數小於傳遞給 *pulNumProfiles* 的值，則 *pulNumProfiles* 會傳回該總計。 否則，它會傳回與傳遞給它相同的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Scanprofilemgr。h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[掃描設定檔架構](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




