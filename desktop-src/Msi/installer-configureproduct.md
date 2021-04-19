---
description: 安裝程式物件的 ConfigureProduct 方法會安裝或卸載產品。
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Installer.ConfigureProduct 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 989855508215b2cd5d04bff7903628513314b9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993685"
---
# <a name="installerconfigureproduct-method"></a>Installer.ConfigureProduct 方法

[**安裝程式**](installer-object.md)物件的 **ConfigureProduct** 方法會安裝或卸載產品。

## <a name="syntax"></a>語法


```JScript
Installer.ConfigureProduct(
  Product,
  InstallLevel,
  InstallState
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*產品* 
</dt> <dd>

指定產品的產品代碼。

</dd> <dt>

*InstallLevel* 
</dt> <dd>

指定產品的預設安裝設定。 如果 InstallState 參數設定為 msiInstallStateDefault 以外的任何其他值，則會忽略 InstallLevel 參數，並安裝所有功能。

此參數必須是 0 (使用撰寫的功能層級進行安裝) 、65535 (安裝所有功能) ，或介於0到65535之間的值，以安裝可用功能的子集。

</dd> <dt>

*InstallState* 
</dt> <dd>

指定功能的安裝狀態。 此參數必須是下列值之一。



| 值                                                                                                                                                                                                                                        | 意義                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <dt>**msiInstallStateAdvertised**</dt> </dl> | 此功能已公告<br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <dt>**msiInstallStateLocal**</dt> </dl>                     | 這項功能會安裝在本機。<br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <dt>**msiInstallStateAbsent**</dt> </dl>                 | 這項功能已卸載。<br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <dt>**msiInstallStateSource**</dt> </dl>                 | 這項功能已安裝成從來源執行。<br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <dt>**msiInstallStateDefault**</dt> </dl>             | 這項功能會安裝到其預設位置。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**ConfigureProduct** 方法會使用目前的設定來顯示使用者介面。 在呼叫 **ConfigureProduct** 方法之前，您可以藉由修改 [**UILevel 屬性 (安裝程式物件)**](installer-uilevel.md)來變更使用者介面設定。

如果 *InstallState* 參數設定為 msiInstallStateDefault 以外的任何其他值，則會忽略 *InstallLevel* 參數，並安裝產品的所有功能。 當 *InstallState* 參數未設定為 msiInstallStateDefault 時，請使用 [**ConfigureFeature**](installer-configurefeature.md)方法來控制個別功能的安裝。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[安裝和設定功能](installer-function-reference.md)
</dt> </dl>

 

 




