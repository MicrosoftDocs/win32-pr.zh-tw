---
description: 安裝程式物件的 ProvideComponent 方法會傳回完整的元件路徑，並執行任何必要的安裝。
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: ProvideComponent 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 49e3808fdad44e4bc3cb7312c1b352874eab3b768920f23ac198811d29f6c8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630326"
---
# <a name="installerprovidecomponent-method"></a>ProvideComponent 方法

[**安裝程式**](installer-object.md)物件的 **ProvideComponent** 方法會傳回完整的元件路徑，並執行任何必要的安裝。 如有必要，[**安裝程式**](installer-object.md)物件的 **ProvideComponent** 方法會提示輸入來源並遞增功能的使用計數。

## <a name="syntax"></a>語法


```JScript
Installer.ProvideComponent(
  Product,
  Feature,
  Component,
  InstallMode
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*產品* 
</dt> <dd>

指定產品的產品代碼。

</dd> <dt>

*功能* 
</dt> <dd>

指定包含元件之功能的功能識別碼。

</dd> <dt>

*元件* 
</dt> <dd>

指定元件代碼。

</dd> <dt>

*InstallMode* 
</dt> <dd>

定義安裝模式。 此參數可以是下表所示的其中一個值。



| 名稱                                                                                                                                                                                                                                                                                                                                                               | 意義                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                | 提供元件路徑，視需要執行任何安裝。<br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>– 1</dt> </dl>                                                                           | 只有在功能存在時，才會提供元件路徑;否則，會傳回空字串。 這個模式會確認元件的金鑰檔是否存在。<br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>– 2</dt> </dl>                                                               | 只有在功能存在時，才會提供元件路徑。 否則，會傳回空字串。 此模式會檢查元件的註冊，但不會驗證元件的金鑰檔是否存在。<br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>– 3</dt> </dl>                                   | 只有在具有 *MsiInstallStateLocal* InstallState 參數的功能存在時，才會提供元件路徑。 這會檢查元件的註冊，但不會驗證元件的金鑰檔是否存在。<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**msiReinstallMode 旗標的組合**</dt><dt></dt> </dl> | 使用 *ReinstallMode* 參數的這個參數，呼叫 [**ReinstallFeature**](installer-reinstallfeature.md)來重新安裝此功能，然後提供元件。<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**ProvideComponent** 方法會結合 [**UseFeature**](installer-usefeature.md)、 [**ConfigureFeature**](installer-configurefeature.md)和 [**ComponentPath**](installer-componentpath.md)的功能。 **ProvideComponent** 方法會簡化呼叫序列，但也會增加使用計數，且應該謹慎使用，以避免使用次數不正確。 **ProvideComponent** 方法也提供比一系列個別呼叫先前所述的方法和屬性更少的彈性。

如果應用程式正在從非預期的情況下復原，則應用程式可能已被呼叫 [**UseFeature**](installer-usefeature.md) 並增加了使用計數。 在此情況下，應用程式應呼叫 [**ConfigureFeature**](installer-configurefeature.md) 方法，而不是 **ProvideComponent** 方法，以避免遞增使用計數。

MsiInstallModeExisting 選項不能搭配 msiReinstallMode 旗標一起使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




