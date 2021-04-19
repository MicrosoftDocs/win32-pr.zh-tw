---
description: Product 物件代表產品的唯一實例，也就是已公告、已安裝或未知。您可以使用 Product 屬性將物件具現化為 &\# 0034;WindowsInstaller： Product (ProductCode，UserSid，CoNtext) &\# 0034;。
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Product 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f8e9071f26da944c2c5ea206b2f70582d731ef59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982978"
---
# <a name="product-object"></a>Product 物件

**Product** 物件代表產品的唯一實例，也就是已公告、已安裝或未知。

您可以使用 **product** 屬性將物件具現化為 "WindowsInstaller"、" (*"、*" *UserSid*"、 *CoNtext*) "。 每一機器內容的 *UserSid* 必須是 Null。 當內容不是每一部電腦時， *UserSid* 可為指定目前使用者的 null。 需要 *ProductCode* 和 *CoNtext* 參數。

## <a name="members"></a>成員

**Product** 物件有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Product** 物件有這些方法。



| 方法                                                                 | 描述                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)       | 將磁片新增至已註冊的磁片集。<br/>                                                              |
| [**SourceListAddSource**](product-sourcelistaddsource.md)             | 將網路或 URL 來源新增至來源清單。<br/>                                                         |
| [**SourceListClearAll**](product-sourcelistclearall.md)               | 清除指定類型來源的完整來源清單。<br/>                                       |
| [**SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)   | 從來源清單中移除已註冊磁片集的磁片。<br/>                                    |
| [**SourceListClearSource**](product-sourcelistclearsource.md)         | 從來源清單中移除網路或 URL 來源。<br/>                                                    |
| [**SourceListForceResolution**](product-sourcelistforceresolution.md) | 清除上次使用的來源。 這會在下一次需要來源時強制來源清單解析。<br/> |



 

### <a name="properties"></a>屬性

**Product** 物件具有這些屬性。



| 屬性                                                      | 描述                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**ComponentState**](product-componentstate.md)<br/>   | 此產品實例之指定元件的狀態。 <br/>                   |
| [**Context**](product-context.md)<br/>                 | 此產品實例的內容，做為 MSIINSTALLCONTEXT 值。 <br/>                 |
| [**FeatureState**](product-featurestate.md)<br/>       | 此產品實例之指定功能的狀態。 <br/>                     |
| [**InstallProperty**](product-installproperty.md)<br/> | 指定之屬性的值。 <br/>                                              |
| [**MediaDisks**](product-mediadisks.md)<br/>           | 列舉此產品實例的所有媒體磁片。<br/>                        |
| [**ProductCode**](product-productcode.md)<br/>         | 傳回產品代碼。 <br/>                                                       |
| [**SourceListInfo**](product-sourcelistinfo.md)<br/>   | 取得和設定來源資訊屬性。 這是讀取或寫入屬性。<br/> |
| [**來源**](product-sources.md)<br/>                 | 列舉此產品實例的所有來源。<br/>                            |
| [**狀態**](product-state.md)<br/>                     | 產品的安裝狀態。<br/>                                               |
| [**UserSid**](product-usersid.md)<br/>                 | 傳回使用者 SID，此為此產品實例可用的帳戶。<br/>    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows Installer 腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




