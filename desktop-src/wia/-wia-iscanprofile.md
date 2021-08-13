---
description: IScanProfile 介面代表單一掃描設定檔，可讓應用程式設定和取得設定檔的屬性。
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: IScanProfile 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 1de80ac23ffa3e2687e2e6d0449f7a273067d5899204c479f9b62e8571190d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450828"
---
# <a name="iscanprofile-interface"></a>IScanProfile 介面

**IScanProfile** 介面代表單一掃描設定檔，可讓應用程式設定和取得設定檔的屬性。

## <a name="members"></a>成員

**IScanProfile** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IScanProfile** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IScanProfile** 介面具有這些方法。



| 方法                                                     | 描述                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAllPropIDs**](-wia-iscanprofile-getallpropids.md)   | 取得設定檔中的所有可用屬性識別碼。<br/>                                                                                            |
| [**GetDeviceID**](-wia-iscanprofile-getdeviceid.md)       | 傳回裝置的識別碼。<br/>                                                                                                            |
| [**GetGUID**](-wia-iscanprofile-getguid.md)               | 傳回設定檔的 GUID。<br/>                                                                                                         |
| [**GetItem**](-wia-iscanprofile-getitem.md)               | 取得與設定檔相關聯之 WIA 2.0 專案類別目錄的 GUID。<br/>                                                   |
| [**GetName**](-wia-iscanprofile-getname.md)               | 取得設定檔的易記名稱。<br/>                                                                                                   |
| [**GetNumPropIDS**](-wia-iscanprofile-getnumpropids.md)   | 取得設定檔中的屬性識別碼數目。<br/>                                                                                            |
| [**GetProperty**](-wia-iscanprofile-getproperty.md)       | 取得掃描設定檔的元素中指定之子屬性的值 `<Properties>` 。<br/>                                            |
| [**IsDefault**](-wia-iscanprofile-isdefault.md)           | 取得值，這個值會指出設定檔是否為相關聯之 [**IWiaItem2**](-wia-iwiaitem2.md) 裝置的預設掃描設定檔。<br/> |
| [**RemoveProperty**](-wia-iscanprofile-removeproperty.md) | 在掃描設定檔的元素中移除指定的子屬性清單 `<Properties>` 。<br/>                                            |
| [**儲存**](-wia-iscanprofile-save.md)                     | 將設定檔的變更儲存至磁片。<br/>                                                                                                      |
| [**SetItem**](-wia-iscanprofile-setitem.md)               | 設定與設定檔相關聯之 WIA 2.0 專案類別目錄的 GUID。<br/>                                                       |
| [**SetName**](-wia-iscanprofile-setname.md)               | 設定設定檔的易記名稱。<br/>                                                                                                   |
| [**SetProperty**](-wia-iscanprofile-setproperty.md)       | 在掃描設定檔的元素中，設定指定之子屬性的值 `<Properties>` 。<br/>                                            |



 

## <a name="remarks"></a>備註

任何 [**IWiaItem2**](-wia-iwiaitem2.md) 裝置都可以有掃描設定檔。 不過，  [WIA \_ 類別目錄 \_ 已完成檔案] 和 [wia 類別根目錄] 類型的 IWiaItem2 專案 \_ \_ \_ 不能有設定檔。

如果使用 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) 方法儲存掃描設定檔，它會儲存為 XML 檔案，位於% USERPROFILE% 的 \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles。

若要建立 **IScanProfile** 物件的實例，請使用 [**IScanProfileMgr：： CreateProfile**](-wia-iscanprofilemgr-createprofile.md) 方法。 若要取得已儲存至磁片的掃描設定檔的參考，請使用 [**IScanProfileMgr：： OpenProfile**](-wia-iscanprofilemgr-openprofile.md) 方法。

所有掃描設定檔都有下列元素： `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` 、和 `<Properties>` 。 裝置的預設設定檔也有一個 `<Default>` 元素。

`<ProfileGUID>` `<DeviceID>` 建立設定檔之後，就無法變更和元素。 在 `<ProfileName>` `<WiaItem>` 建立設定檔之後，可以變更元素和元素的值。 您 `<Default>` 可以新增或刪除元素。 您可以使用 [**IScanProfile：： SetName**](-wia-iscanprofile-setname.md)、 [**IScanProfile：： SetItem**](-wia-iscanprofile-setitem.md)和 [**IScanProfileMgr：： SetDefault**](-wia-iscanprofilemgr-setdefault.md) 方法以程式設計方式完成此動作。 使用者也可以透過 [**IScanProfileUI：： ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) 方法變更這些屬性。

`<Properties>`元素包含 `<Property>` 子系。 使用這些專案，將任何 WIA 2.0 專案或裝置屬性新增至設定檔。 您也可以開發自己的映射獲取 `<Property>` 子系。 這可延伸掃描設定檔架構。  (如需延伸架構的詳細資訊，請參閱 [定義自訂屬性](-wia-defining-custom-properties.md)、 [**IScanProfile：： GetProperty**](-wia-iscanprofile-getproperty.md)和 [**IScanProfile：： SetProperty**](-wia-iscanprofile-setproperty.md)。 ) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                        |
| Idl<br/>                      | <dl> <dt>Scanprofiles .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[掃描設定檔架構](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
