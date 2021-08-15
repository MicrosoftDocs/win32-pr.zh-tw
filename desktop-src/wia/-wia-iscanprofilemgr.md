---
description: IScanProfileMgr 介面提供建立、開啟、刪除及管理掃描設定檔的方法。
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: 'IScanProfileMgr 介面 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: d2d517143a55c2bd732bb8f9c642697a7d50151ddb72fcffd13d978caef597b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593088"
---
# <a name="iscanprofilemgr-interface"></a>IScanProfileMgr 介面

**IScanProfileMgr** 介面提供建立、開啟、刪除及管理掃描設定檔的方法。

## <a name="members"></a>成員

**IScanProfileMgr** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IScanProfileMgr** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IScanProfileMgr** 介面具有這些方法。



| 方法                                                                              | 描述                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md)                         | 建立空的掃描設定檔，並將它與掃描器或其他 WIA 2.0 專案產生關聯。<br/>                       |
| [**DeleteAllProfiles**](-wia-iscanprofilemgr-deleteallprofiles.md)                 | 刪除與指定裝置相關聯的所有掃描設定檔。<br/>                                         |
| [**DeleteAllProfilesForUser**](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | 刪除您的應用程式執行所在系統中使用者可用的所有掃描設定檔。 <br/> |
| [**DeleteProfile**](-wia-iscanprofilemgr-deleteprofile.md)                         | 刪除指定的掃描設定檔。<br/>                                                                         |
| [**GetDefaultProfile**](-wia-iscanprofilemgr-getdefaultprofile.md)                 | 取得預設掃描設定檔。<br/>                                                                              |
| [**GetNumProfiles**](-wia-iscanprofilemgr-getnumprofiles.md)                       | 取得在您的應用程式執行所在系統中為使用者建立的掃描設定檔數目。<br/> |
| [**GetNumProfilesforDeviceID**](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | 取得裝置的掃描設定檔數目。<br/>                                                            |
| [**>ipartner.getprofiles**](-wia-iscanprofilemgr-getprofiles.md)                             | 取得您的應用程式執行所在系統中使用者可用的所有掃描設定檔。<br/>     |
| [**GetProfilesforDeviceID**](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | 取得與裝置相關聯的所有掃描設定檔。<br/>                                                        |
| [**OpenProfile**](-wia-iscanprofilemgr-openprofile.md)                             | 開啟已儲存至磁片的掃描設定檔做為 XML 檔案。<br/>                                            |
| [**重新整理**](-wia-iscanprofilemgr-refresh.md)                                     | 重新列舉系統中的所有掃描設定檔。<br/>                                                          |
| [**SetDefault**](-wia-iscanprofilemgr-setdefault.md)                               | 將指定的掃描設定檔設定為預設設定檔。<br/>                                                     |



 

## <a name="remarks"></a>備註

若要建立 **IScanProfileMgr** 物件，請使用具有下列參數的 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 方法：

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

如果使用 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) 方法儲存掃描設定檔，它會儲存為 XML 檔案，位於% USERPROFILE% 的 \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Scanprofilemgr。h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[掃描設定檔架構](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
