---
description: InstallProperty 屬性是此產品之實例的屬性值。 這個屬性會呼叫 MsiGetProductInfoEx 函式，其中包含 ProductCode、UserSid 和 Product 物件的內容，以及所要求的屬性做為參數。
ms.assetid: 945c11fe-39da-43b7-a19f-e6364d5e715c
title: InstallProperty 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.InstallProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12949997363fce8073c15f7ca6b7312c211fa0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990546"
---
# <a name="productinstallproperty-method"></a>InstallProperty 方法

**InstallProperty** 屬性是此產品之實例的屬性值。

這個屬性會呼叫 [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)函式，其中包含 *ProductCode*、 *UserSid* 和 [**Product**](product-object.md)物件的 *內容*，以及所要求的屬性做為參數。

## <a name="syntax"></a>語法


```JScript
Product.InstallProperty(
  property
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*property* 
</dt> <dd>

指定要抓取的屬性。 下列清單中的屬性只能從已經安裝的應用程式取出。 請注意， [必要](required-properties.md) 屬性保證可供使用，但只有在已設定該屬性的情況下，才能使用其他屬性。 如需有關如何設定每個屬性的詳細資訊，請參閱安裝程式 [屬性](properties.md) 的指示連結。



| 已安裝屬性                                                                                                                                                                                                               | 意義                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INSTALLPROPERTY_PRODUCTSTATE"></span><span id="installproperty_productstate"></span><dl> <dt>**INSTALLPROPERTY \_ PRODUCTSTATE**</dt> </dl>                         | 已安裝的產品狀態（以字串形式傳回為 "1"），且已安裝 "5"。<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_HELPLINK"></span><span id="installproperty_helplink"></span><dl> <dt>**INSTALLPROPERTY \_ HELPLINK**</dt> </dl>                                     | 支援連結。 如需詳細資訊，請參閱 [**ARPHELPLINK**](arphelplink.md) 屬性。<br/>                                                                                                                                                                                                                                                                             |
| <span id="INSTALLPROPERTY_HELPTELEPHONE"></span><span id="installproperty_helptelephone"></span><dl> <dt>**INSTALLPROPERTY \_ HELPTELEPHONE**</dt> </dl>                      | 支援電話。 如需詳細資訊，請參閱 [**ARPHELPTELEPHONE**](arphelptelephone.md) 屬性。<br/>                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_INSTALLDATE"></span><span id="installproperty_installdate"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLDATE**</dt> </dl>                            | 此產品上次收到服務的時間。 每次在產品中套用或移除修補程式，或使用/v [命令列選項](command-line-options.md) 來修復產品時，就會取代這個屬性的值。 如果產品未收到維修或修補程式，此內容會包含此產品在這部電腦上的安裝時間。<br/> |
| <span id="INSTALLPROPERTY_INSTALLEDPRODUCTNAME"></span><span id="installproperty_installedproductname"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLEDPRODUCTNAME**</dt> </dl> | 已安裝的產品名稱。 如需詳細資訊，請參閱 [**ProductName**](productname.md) 屬性。<br/>                                                                                                                                                                                                                                                                   |
| <span id="INSTALLPROPERTY_INSTALLLOCATION"></span><span id="installproperty_installlocation"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLLOCATION**</dt> </dl>                | 安裝位置。 如需詳細資訊，請參閱 [**ARPINSTALLLOCATION**](arpinstalllocation.md) 屬性。<br/>                                                                                                                                                                                                                                                      |
| <span id="INSTALLPROPERTY_INSTALLSOURCE"></span><span id="installproperty_installsource"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLSOURCE**</dt> </dl>                      | 安裝來源。 如需詳細資訊，請參閱 [**SourceDir**](sourcedir.md) 屬性。<br/>                                                                                                                                                                                                                                                                          |
| <span id="INSTALLPROPERTY_LOCALPACKAGE"></span><span id="installproperty_localpackage"></span><dl> <dt>**INSTALLPROPERTY \_ LOCALPACKAGE**</dt> </dl>                         | 本機快取的封裝。<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="INSTALLPROPERTY_PUBLISHER"></span><span id="installproperty_publisher"></span><dl> <dt>**INSTALLPROPERTY \_ 發行者**</dt> </dl>                                  | 簽發者。 如需詳細資訊，請參閱 [**製造商**](manufacturer.md) 屬性。<br/>                                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_URLINFOABOUT"></span><span id="installproperty_urlinfoabout"></span><dl> <dt>**INSTALLPROPERTY \_ URLINFOABOUT**</dt> </dl>                         | URL 資訊。 如需詳細資訊，請參閱 [**ARPURLINFOABOUT**](arpurlinfoabout.md) 屬性。<br/>                                                                                                                                                                                                                                                                  |
| <span id="INSTALLPROPERTY_URLUPDATEINFO"></span><span id="installproperty_urlupdateinfo"></span><dl> <dt>**INSTALLPROPERTY \_ URLUPDATEINFO**</dt> </dl>                      | URL 更新資訊。 如需詳細資訊，請參閱 [**ARPURLUPDATEINFO**](arpurlupdateinfo.md) 屬性。<br/>                                                                                                                                                                                                                                                         |
| <span id="INSTALLPROPERTY_VERSIONMINOR"></span><span id="installproperty_versionminor"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONMINOR**</dt> </dl>                         | 衍生自 [**ProductVersion**](productversion.md) 屬性的次要產品版本。<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONMAJOR"></span><span id="installproperty_versionmajor"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONMAJOR**</dt> </dl>                         | 從 [**ProductVersion**](productversion.md) 屬性衍生的主要產品版本。<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONSTRING"></span><span id="installproperty_versionstring"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONSTRING**</dt> </dl>                      | 產品版本。 如需詳細資訊，請參閱 [**ProductVersion**](productversion.md) 屬性。<br/>                                                                                                                                                                                                                                                                    |



 

若要從已安裝的應用程式取出產品識別碼、註冊的擁有者或已註冊的公司，請將 *屬性* 設定為下列其中一個文字字串值。



| 值      | 描述                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| ProductID  | 產品識別碼。 如需詳細資訊，請參閱 [**ProductID**](productid.md) 屬性。 |
| RegCompany | 註冊使用此產品的公司。                                                    |
| RegOwner   | 註冊使用此產品的擁有者。                                                      |



 

若要取得產品的實例類型，請將 *屬性* 設定為下列值。 此屬性適用于已公告或已安裝的產品。



| 值        | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InstanceType | 遺漏值或0值表示正常的產品安裝。 值為1時，表示使用多個實例轉換和 [**MSINEWINSTANCE**](msinewinstance.md) 屬性安裝的產品。 適用于執行 Windows Server 2003 或 Windows XP 含 SP1 的安裝程式。 如需詳細資訊，請參閱 [安裝多個產品和修補程式實例](installing-multiple-instances-of-products-and-patches.md)。 |



 

下列清單中的屬性也可以從已公告的應用程式中取出。 無法針對目前使用者帳戶以外的使用者帳戶，針對每個使用者非受控內容所安裝的產品實例，取得這些屬性。



| 宣告的屬性                 | Description                                                                                                                                                                                                                                                                                          |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| INSTALLPROPERTY \_ 轉換           | 轉換。                                                                                                                                                                                                                                                                                          |
| INSTALLPROPERTY \_ 語言             | 產品語言。                                                                                                                                                                                                                                                                                    |
| INSTALLPROPERTY \_ PRODUCTNAME          | 人類可讀取–產品名稱。 如需詳細資訊，請參閱 [**ProductName**](productname.md) 屬性。                                                                                                                                                                                              |
| INSTALLPROPERTY \_ ASSIGNMENTTYPE       | 等於零 (0) 如果產品已針對每位使用者公告或安裝。 等於 1 (1) 如果為所有使用者通告或安裝每一電腦的產品。<br/>                                                                                                                                  |
| INSTALLPROPERTY \_ PACKAGECODE          | 此產品安裝來源套件的識別碼。 如需詳細資訊，請參閱 [套件代碼](package-codes.md)。                                                                                                                                                                                      |
| INSTALLPROPERTY \_ 版本              | 衍生自 [**ProductVersion**](productversion.md) 屬性的產品版本。                                                                                                                                                                                                                  |
| INSTALLPROPERTY \_ PRODUCTICON          | 封裝的主要圖示。 如需詳細資訊，請參閱 [**ARPPRODUCTICON**](arpproducticon.md) 屬性。                                                                                                                                                                                       |
| INSTALLPROPERTY \_ PACKAGENAME          | 原始安裝封裝的名稱。                                                                                                                                                                                                                                                           |
| INSTALLPROPERTY \_ 授權的 \_ LUA \_ 應用程式 | 值為1時，表示可由非系統管理員使用的 [使用者帳戶控制 (UAC) 修補](user-account-control--uac--patching.md)的產品。 遺漏值或值0表示未啟用最低許可權修補。 適用于 Windows Installer 3.0 和更新版本。 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果呼叫成功，屬性會將值包含為字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**產品**](product-object.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




