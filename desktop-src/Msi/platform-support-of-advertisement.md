---
description: Windows Installer 支援廣告應用程式和功能。
ms.assetid: 9e5158bc-4877-49d1-9bb9-4dd17abb444d
title: 廣告的平臺支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48016241998473a5bb5ae8ecff05a14fd702f8be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106975605"
---
# <a name="platform-support-of-advertisement"></a>廣告的平臺支援

Windows Installer 支援廣告應用程式和功能。

下列公告功能可在 Windows Server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003、Windows XP 及 Windows 2000 上取得。

-   快速鍵及其圖示。

-   [ProgId 資料表](progid-table.md)中指定的延伸模組及其圖示。

-   在 ProgId 索引鍵下註冊的 Shell 和命令動詞。

-   CLSID 內容和 InProcHandler。

-   透過 OLE 的隨選安裝僅可透過 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以程式設計方式透過 CoCreateInstance (C/c + +) ，而 CreateObject 函式 **(Visual Basic)** 或 **GetObject 函數 (Visual Basic)**。

> [!Note]
> 只有在安裝公告的元件時，才會寫入 AppId 和 Typelib 資訊。
> 
> 若要支援副檔名，必須將應用程式發佈至使用群組原則的系統管理員 Active Directory。

## <a name="remarks"></a>備註

產品的安裝可能不需要重新開機，但是在重新開機電腦之前，任何通告的快捷方式都無法運作。 後續安裝的已公告快捷方式不需要重新開機即可運作。

為了確保通告的快捷方式正確運作，套件作者應該在安裝結束時排程強制重新開機。

若要避免系統不必要的重新開機，請將重新開機排程為只有在未安裝任何版本的 Windows Installer 時才執行。

條件陳述式可以檢查 [**ShellAdvtSupport**](shelladvtsupport.md) 屬性和 [**Version9X**](version9x.md) 屬性。 如需排程條件式強制重新開機的詳細資訊，請參閱 [系統重新開機](system-reboots.md) 和 [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md)。

 

 
