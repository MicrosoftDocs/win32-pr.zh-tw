---
description: 針對 patch 套件所列出的每項產品，都有資格接收修補程式，安裝程式物件的 ApplyPatch 方法會叫用安裝，並將 PATCH 屬性設定為 patch 封裝的路徑。
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: ApplyPatch 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc1b7509ddb4c61fa84a4547dcd47f2c7637b913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982617"
---
# <a name="installerapplypatch-method"></a>ApplyPatch 方法

針對 patch 套件所列出的每項產品，都有資格接收修補程式，[**安裝程式**](installer-object.md)物件的 **ApplyPatch** 方法會叫用安裝，並將 [**patch**](patch.md)屬性設定為 patch 封裝的路徑。

## <a name="syntax"></a>語法


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*PatchPackage* 
</dt> <dd>

指定修補封裝的路徑。

</dd> <dt>

*InstallPackage* 
</dt> <dd>

如果 *InstallType* 設定為 msiInstallTypeNetworkImage，則 *InstallPackage* 會指定要修補的產品路徑。 如果 *InstallType* 設定為 msiInstallTypeDefault，且 *InstallPackage* 設定為0，則安裝程式會將修補程式套用至修補套件中所列的每個合格產品。

如果 *InstallType* 是 msiInstallTypeSingleInstance，則安裝程式會將修補程式套用至 *InstallPackage* 所指定的產品。 在此情況下，會忽略 patch 套件中所列的其他合格產品，且 *InstallPackage* 參數會包含以 null 終止的字串，代表要修補之實例的產品代碼。 這種類型的安裝需要 Windows Server 2003 或更新版本所隨附的 Windows Installer 版本，或是 Windows Installer XP SP1 或更新版本。

</dd> <dt>

*InstallType* 
</dt> <dd>

此參數會指定要修補的安裝類型。 如果省略 *InstallPackage* ，則會忽略 *InstallType* 參數。



| 值                                                                                                                                                                                                                                            | 意義                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <dt>**msiInstallTypeNetworkImage**</dt> </dl> | 表示系統管理安裝。 在此情況下， *InstallPackage* 必須設定為封裝路徑。 MsiInstallTypeNetworkImage 的1值指定系統管理安裝。<br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <dt>**msiInstallTypeDefault**</dt> </dl>                     | 搜尋系統中的產品以進行修補。 在此情況下， *InstallPackage* 必須是空字串。<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <dt>**msiInstallSingleInstance**</dt> </dl>         | 修補 *InstallPackage* 所指定的產品。 *InstallPackage* 是要修補之實例的產品代碼。 這種類型的安裝需要 Windows Server 2003 或更新版本所隨附的 Windows Installer 版本，或是 Windows Installer XP SP1 或更新版本。 如需詳細資訊，請參閱 [安裝多個產品實例和修補程式](installing-multiple-instances-of-products-and-patches.md)。<br/> |



 

</dd> <dt>

*CommandLine* 
</dt> <dd>

指定要在命令列上設定的屬性設定。 請參閱備註一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

因為轉換、來源和修補程式的清單分隔符號是分號，所以不應該將這個字元用於檔案名或路徑。

套用 [小型更新](small-updates.md)或 [次要升級](minor-upgrades.md)修補程式時，需要 [**重新安裝**](reinstall.md)屬性。 如果沒有這個屬性，就會在系統上註冊修補程式，但無法更新檔案。

**Windows Installer 2.0：** 套用 [小型更新](small-updates.md)或 [次要升級](minor-upgrades.md)修補程式時，您必須在命令列上設定 [**重新安裝**](reinstall.md)屬性。 若修補程式未使用 [自訂動作類型 51](custom-action-type-51.md)自動設定 **重新安裝** 和 [**REINSTALLMODE**](reinstallmode.md)屬性，則必須使用 *命令列* 參數明確設定 **重新安裝** 屬性。 設定 [ **重新安裝** ] 屬性以列出受修補程式影響的功能，或使用 [重新安裝 = 全部] 的實際預設設定。 **REINSTALLMODE** 屬性的預設值為 "omus reinstall"。

**Windows Installer 3.0 和更新版本：** 從 Windows Installer 版本3.0 開始，安裝 [**程式屬性是**](reinstall.md) 由安裝程式所設定，不需要在命令列上設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[關於屬性](about-properties.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




