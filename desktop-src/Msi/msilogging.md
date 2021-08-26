---
description: MsiLogging 屬性會設定 Windows Installer 封裝的預設記錄模式。
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: MsiLogging 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e166a52e970cdb3e0be5ffae6611a8ea9a299232d55f36a45ba470b3717cafae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042778"
---
# <a name="msilogging-property"></a>MsiLogging 屬性

**MsiLogging** 屬性會設定 Windows Installer 封裝的預設記錄模式。 如果這個選擇性屬性存在於 [屬性工作表](property-table.md)中，安裝程式會產生名為 MSI 的記錄檔 \* 。日誌。 記錄檔的完整路徑是由 [**MsiLogFileLocation**](msilogfilelocation.md) 屬性的值提供。

## <a name="value"></a>值

這個屬性的值應該是下列字元的字串，指定預設的記錄模式。



| 值                                                                        | 意義                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>我</dt> </dl> | 狀態訊息。<br/>                                                    |
| <dl> <dt>w</dt> </dl> | 非嚴重警告。<br/>                                                  |
| <dl> <dt>pci-e</dt> </dl> | 所有錯誤訊息。<br/>                                                 |
| <dl> <dt>的</dt> </dl> | 啟動動作。<br/>                                                |
| <dl> <dt>r</dt> </dl> | 動作特定記錄。<br/>                                            |
| <dl> <dt>u</dt> </dl> | 使用者要求。<br/>                                                      |
| <dl> <dt>c</dt> </dl> | 初始 UI 參數。<br/>                                              |
| <dl> <dt>m</dt> </dl> | 記憶體不足或嚴重的離開資訊。<br/>                            |
| <dl> <dt>o</dt> </dl> | 磁碟空間不足的訊息。<br/>                                         |
| <dl> <dt>p</dt> </dl> | 終端機屬性。<br/>                                                |
| <dl> <dt>v</dt> </dl> | 詳細資訊輸出。<br/>                                                     |
| <dl> <dt>x</dt> </dl> | 額外的調試資訊。 僅適用于 Windows Server 2003。<br/> |
| <dl> <dt>!</dt> </dl> | 將每一行排清到記錄檔。<br/>                                         |



 

## <a name="remarks"></a>備註

從 Windows Installer 4.0 開始，可以使用此屬性。

您無法 \* 在 **MsiLogging** 屬性的值中使用/l 選項的 "+" 和 "" 值。

您可以使用原則、命令列選項或以程式設計方式來設定記錄模式。 這會覆寫預設的記錄模式。 如需可用於設定記錄模式之所有方法的詳細資訊，請參閱[Windows Installer 記錄](windows-installer-logging.md)] 區段中的[一般記錄](normal-logging.md)。

如果 [屬性工作表](property-table.md)中有 **MsiLogging** 屬性，則可以使用 [資料庫轉換](database-transforms.md)來變更這個屬性的值，藉以修改封裝的預設記錄模式。 無法使用 (.msp 檔的 [修補套件](patch-packages.md) 來變更預設記錄模式。 ) 

如果已在 [屬性工作表](property-table.md)中設定 **MsiLogging** 屬性，則可以藉由設定 [DisableLoggingFromPackage](disableloggingfrompackage.md)原則和 [記錄](logging.md)原則來指定電腦上所有使用者的預設記錄模式。 同時設定 DisableLoggingFromPackage 原則和記錄原則，將會覆寫所有封裝的 **MsiLogging** 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式4.5。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




