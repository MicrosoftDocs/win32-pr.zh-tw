---
description: 本主題列出用於快捷方式 (內容) 功能表和快捷方式功能表處理常式的主要程式設計項目。 快速鍵功能表處理常式（也稱為內容功能表處理常式或動詞處理常式）是檔案類型處理常式的類型。
ms.assetid: efd96a52-6455-40bc-9c21-65f89728e771
title: 快速鍵功能表參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb1552c8f2f383b08984e9142e464b6831a3c8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191182"
---
# <a name="shortcut-menu-reference"></a>快速鍵功能表參考

本主題列出用於快捷方式 (內容) 功能表和快捷方式功能表處理常式的主要程式設計項目。 快速鍵功能表處理常式（也稱為內容功能表處理常式或動詞處理常式）是檔案類型處理常式的類型。

## <a name="about-shortcut-menu-implemetation"></a>關於快捷方式功能表實作

強烈建議您使用其中一個靜態動詞方法來執行快捷方式功能表。 請參閱下列指示：

-   若要使用靜態動詞方法來執行快捷方式功能表，請參閱 [建立快捷方式功能表處理常式](context-menu-handlers.md)的「使用靜態動詞自訂快捷方式功能表」一節。
-   若要在 Windows 7 及更新版本中取得靜態動詞命令的動態行為，請參閱 [建立快捷方式功能表處理常式](context-menu-handlers.md)中的「取得靜態動詞的動態行為」。
-   如需靜態動詞命令的執行，以及要避免哪些動態動詞的詳細資訊，請參閱 [為您的快捷方式功能表選擇靜態或動態動詞](shortcut-choose-method.md)。
-   如果您必須註冊檔案類型的動態動詞命令以擴充檔案類型的快捷方式功能表，請依照 [使用動態動詞自訂快捷方式功能表](shortcut-menu-using-dynamic-verbs.md)中提供的指示進行。

### <a name="interfaces"></a>介面



| 主題                                        | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)         | 公開方法，以建立或合併與 Shell 物件相關聯的快捷方式功能表。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ICoNtextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)       | 公開方法，以建立或合併與 Shell 物件相關聯的快捷方式 (內容) 功能表。 藉由新增方法來擴充 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) ，以允許用戶端物件處理與主控描繪功能表項目相關聯的訊息。<br/>                                                                                                                                                                                                                                                    |
| [**ICoNtextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3)       | 公開方法，以建立或合併與 Shell 物件相關聯的快捷方式功能表。 允許用戶端物件處理與主控描繪功能表項目相關聯的訊息，並接受來自該訊息處理的傳回值來擴充 [**ICoNtextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) 。<br/>                                                                                                                                                                                                                         |
| [**ICoNtextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)     | 公開啟用內容功能表回呼的方法。 例如，在需要提高許可權的 **menuItem** 中加入盾牌圖示。<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**ICoNtextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) | 由使用 [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview)建立的預設資料夾視圖所執行。 [**ICoNtextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite)的執行支援 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)、 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)和 [**trackpopupmenu 讓**](/windows/win32/api/winuser/nf-winuser-trackpopupmenu)，以及該函式所需的任何訊息轉送。 **ICoNtextMenuSite** 通常也會更新狀態列。<br/> |



 

### <a name="functions"></a>函式



| 主題                                                            | 目錄                                                                                                                                |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)        | 建立所選檔案資料夾物件群組的內容功能表。<br/>                                                          |
| [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)                       | 定義回呼函式的原型，此函式會從 Shell 的預設內容功能表執行接收訊息。<br/> |
| [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) | 建立物件，這個物件表示 Shell 的預設內容功能表執行。<br/>                                           |



 

### <a name="structures"></a>結構



| 主題                                                  | 目錄                                                                                                                                                                                                   |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)     | 包含 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 用來叫用快捷方式功能表命令所需的資訊。<br/>                                                             |
| [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) | 包含快捷方式功能表命令的延伸資訊。 此結構是 [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) 的延伸版本，可允許使用 Unicode 值。<br/> |
| [**DEFCONTEXTMENU**](/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu)               | 包含 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)所使用的內容功能表資訊。<br/>                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快捷方式 (內容) 功能表和快捷方式功能表處理常式](context-menu.md)
</dt> <dt>

[為快捷方式功能表選擇靜態或動態動詞](shortcut-choose-method.md)
</dt> <dt>

[動詞和檔案關聯](fa-verbs.md)
</dt> <dt>

[快速鍵功能表處理常式和多重選取動詞的最佳作法](verbs-best-practices.md)
</dt> <dt>

[建立快捷方式功能表處理常式](context-menu-handlers.md)
</dt> <dt>

[使用動態動詞自訂快捷方式功能表](shortcut-menu-using-dynamic-verbs.md)
</dt> </dl>

 

 
