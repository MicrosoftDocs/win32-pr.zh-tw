---
description: 設定 DISABLEADVTSHORTCUTS 屬性時，會停用產生支援隨選安裝和公告的快捷方式。 設定這個屬性會指定這些快速鍵應該改由一般快速鍵取代。
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: DISABLEADVTSHORTCUTS 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fd8465620abab56ebfe18f68254bf6d29b6e752a7550157231a0b1abe95ecd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745558"
---
# <a name="disableadvtshortcuts-property"></a>DISABLEADVTSHORTCUTS 屬性

設定 **DISABLEADVTSHORTCUTS** 屬性時，會停用產生支援 [隨選安裝](installation-on-demand.md) 和 [公告](advertisement.md)的快捷方式。 設定這個屬性會指定這些快速鍵應該改由一般快速鍵取代。

## <a name="default-value"></a>預設值

依預設，會啟用隨選安裝的快捷方式產生。

## <a name="remarks"></a>備註

支援廣告的快速鍵具有功能的名稱，而不是在 \[ \# \] [快捷方式資料表](shortcut-table.md)的目標資料行中輸入的 filekey 格式檔案路徑。 如果已設定此屬性，且已安裝此功能，安裝程式會產生一般功能的快捷方式。

系統管理員通常會使用這個屬性，讓使用者在不支援廣告的環境之間漫遊。 這個屬性可由轉換、系統管理資料流程或 [屬性工作表](property-table.md)中的設定來設定。 如果是使用命令列或呼叫 [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)來設定，則必須在每次後續安裝期間再次重設。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




