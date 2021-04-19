---
description: 安裝程式物件的 ProvideQualifiedComponent 方法會傳回完整的元件路徑，並執行任何必要的安裝。 如有必要，這個方法會提示輸入來源並遞增功能的使用計數。
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: ProvideQualifiedComponent 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 73c830610b49976e3625dd333c57f39e43d4be14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977560"
---
# <a name="installerprovidequalifiedcomponent-method"></a>ProvideQualifiedComponent 方法

[**安裝程式**](installer-object.md)物件的 **ProvideQualifiedComponent** 方法會傳回完整的元件路徑，並執行任何必要的安裝。 如有必要，這個方法會提示輸入來源並遞增功能的使用計數。

## <a name="syntax"></a>語法


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*類別* 
</dt> <dd>

指定所要求元件的元件識別碼。 這可能不是元件本身的 GUID，而是提供正確功能的伺服器，如同 [PublishComponent 資料表](publishcomponent-table.md)的 [元件] 資料行。

</dd> <dt>

*Qualifier* 
</dt> <dd>

從 [PublishComponent 資料表](publishcomponent-table.md)) 指定 (的廣告元件清單中的辨識符號。

</dd> <dt>

*InstallMode* 
</dt> <dd>

定義安裝模式。 此參數可以是下表所示的其中一個值。



| InstallMode                                                                                                                                                                                                                                                                                                                                                         | 意義                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                 | 提供元件，並執行任何必要的安裝。<br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>– 1</dt> </dl>                                                                            | 只有在功能存在時才會提供元件;否則會傳回空字串。 這個模式會確認元件的金鑰檔是否存在。<br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>– 2</dt> </dl>                                                                | 只有在功能存在時才會提供元件;否則會傳回空字串。 此模式只會檢查元件是否已註冊，但不會驗證元件的金鑰檔是否存在。<br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>– 3</dt> </dl>                                    | 只有在具有 *MsiInstallStateLocal* InstallState 參數的功能存在時，才會提供元件路徑。 這會檢查元件的註冊，但不會驗證元件的金鑰檔是否存在。<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**msiReinstallMode 旗標**</dt> <dt></dt>的組合 </dl> | 使用 *ReinstallMode* 參數的這個參數，呼叫 [**ReinstallFeature**](installer-reinstallfeature.md)來重新安裝此功能，然後提供元件。<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




