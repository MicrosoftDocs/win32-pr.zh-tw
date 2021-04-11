---
description: 刪除指定的掃描設定檔。
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: 'IScanProfileMgr：:D eleteProfile 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f45dfa3ef96fee194348192c2898a44df5f34be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944318"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a>IScanProfileMgr：:D eleteProfile 方法

刪除指定的掃描設定檔。

## <a name="syntax"></a>語法


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pScanProfile* \[在\]
</dt> <dd>

類型： **[**IScanProfile**](-wia-iscanprofile.md) \** _

設定檔的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

**IScanProfileMgr：:D eleteprofile** 會從磁片刪除設定檔，並在記憶體中終結設定檔物件。

當有一個以上的 [**IScanProfileMgr**](-wia-iscanprofilemgr.md)物件可能同時建立或刪除設定檔時，請使用 [**IScanProfileMgr：： Refresh**](-wia-iscanprofilemgr-refresh.md)方法。

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

 

 




