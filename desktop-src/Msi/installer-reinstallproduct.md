---
description: 安裝程式物件的 ReinstallProduct 方法會重新安裝產品，或更正已安裝產品中的安裝問題。
ms.assetid: ff933cce-9f27-4215-9291-dd860d9c4d08
title: ReinstallProduct 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1570f5a0dc607b4a011a5b4276a243c59a64392d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976116"
---
# <a name="installerreinstallproduct-method"></a>ReinstallProduct 方法

[**安裝程式**](installer-object.md)物件的 **ReinstallProduct** 方法會重新安裝產品，或更正已安裝產品中的安裝問題。

## <a name="syntax"></a>語法


```JScript
Installer.ReinstallProduct(
  Product,
  ReinstallMode
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*產品* 
</dt> <dd>

指定產品的產品代碼。

</dd> <dt>

*ReinstallMode* 
</dt> <dd>

指定重新安裝的類型。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                                                                                                                    | 意義                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <dt>**msiReinstallModeFileMissing**</dt> </dl>                     | 只有在遺失檔案時才會重新安裝。<br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <dt>**msiReinstallModeFileOlderVersion**</dt> </dl> | 如果檔案遺失或為較舊的版本，則重新安裝。<br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <dt>**msiReinstallModeFileEqualVersion**</dt> </dl> | 如果檔案遺失或相同或較舊的版本，則重新安裝。<br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <dt>**msiReinstallModeFileExact**</dt> </dl>                             | 如果檔案遺失或不是正確的版本，則重新安裝。<br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <dt>**msiReinstallModeFileVerify**</dt> </dl>                         | 檢查 sum 可執行檔，並在它們遺失或損毀時重新安裝。<br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <dt>**msiReinstallModeFileReplace**</dt> </dl>                     | 無論版本為何，都會重新安裝所有檔案。<br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <dt>**msiReinstallModeUserData**</dt> </dl>                                 | 確保每 = 使用者登錄專案都需要。<br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <dt>**msiReinstallModeMachineData**</dt> </dl>                     | 確保每 = 電腦登錄專案都需要。<br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <dt>**msiReinstallModeShortcut**</dt> </dl>                                 | 驗證快速鍵。<br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <dt>**msiReinstallModePackage**</dt> </dl>                                     | 使用重新緩存來源來安裝套件。<br/>                        |



 

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

[**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
</dt> <dt>

[安裝和設定功能](installer-function-reference.md)
</dt> </dl>

 

 




