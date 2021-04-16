---
description: 建立空的掃描設定檔，並將它與掃描器或其他 Windows 映像取得 (WIA) 2.0 專案產生關聯。
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'IScanProfileMgr：： CreateProfile 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469233"
---
# <a name="iscanprofilemgrcreateprofile-method"></a>IScanProfileMgr：： CreateProfile 方法

建立空的掃描設定檔，並將它與掃描器或其他 Windows 映像取得 (WIA) 2.0 專案產生關聯。

## <a name="syntax"></a>語法


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrDeviceID* \[在\]
</dt> <dd>

類型： **BSTR**

裝置或 WIA 2.0 專案的識別碼。

</dd> <dt>

*bstrName* \[在\]
</dt> <dd>

類型： **BSTR**

新設定檔的易記名稱。

</dd> <dt>

*guidCategory* \[在\]
</dt> <dd>

類型： **GUID**

裝置或 WIA 2.0 專案類別的 GUID。 這必須是其中一個 WIA \_ IPA \_ 專案 \_ 類別常數。

</dd> <dt>

*ppScanProfile* \[擴展\]
</dt> <dd>

類型： **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

新設定檔指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

**IScanProfileMgr：： CreateProfile** 會將指定的裝置與新的掃描設定檔產生關聯。

**IScanProfileMgr：： CreateProfile** 會自動產生新設定檔的 GUID。 使用 [**GetGUID**](-wia-iscanprofile-getguid.md)取得 GUID。

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

 

 




