---
title: 提供媒體燒錄裝置的使用者權限
description: 根據預設，Windows Vista 和 Windows Server 2008 都會將讀取/寫入存取權授與直接登入電腦 (中繼使用者) 中的系統管理員和使用者。
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c5827b960405855ba34880e39750b39d4f934e395167479b7cae7912721af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758557"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a>提供媒體燒錄裝置的使用者權限

根據預設，Windows Vista 和 Windows Server 2008 都會將讀取/寫入存取權授與直接登入電腦 (中繼使用者) 中的系統管理員和使用者。 不過，在 Windows XP 和 Windows Server 2003 中，系統管理員必須將這些裝置的讀取/寫入權限授與其他使用者群組。

系統管理員可以為 power 使用者和互動式使用者調整特定裝置的相關許可權。

若要在 Windows XP 中找到適當的群組許可權面板，請按一下 [**開始**]，再按一下 [**執行**]，輸入 **gpedit.msc**，然後按一下 **[確定]**。 在群組原則介面中，依序展開 [**電腦** 設定]、[ **Windows 設定**]、[**安全性] 設定**、[**本機原則**]，然後按兩下 [**安全性選項**]。

![顯示 [群組原則] 視窗的螢幕擷取畫面，其中已從 [原則] 窗格中選取原則。](images/gpolpanel.jpg)

在此面板中，系統管理員必須指定兩個裝置選項的設定，以提供必要的群組許可權：

-   將「裝置：限制僅限本機登入使用者的 CD-ROM 存取」設為 **啟用**
-   將「裝置：允許格式化及退出卸載式媒體」設定給系統 **管理員和 Power Users**。 您也可以將此選項設定為 [系統管理員] 和 [**互動式使用者**]，以模擬 Windows Vista 許可權。

當 Windows XP 或 Windows Server 2003 中沒有特定 UI 可供使用 [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)或 [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)時，可以使用這些 api 來授與自訂使用者群組裝置許可權。 例如，對 **SetSecurityInfo** 的呼叫會將許可權授與使用者群組。 此 API 的許可權變更是暫時性的，不會在重新開機時持續保存。 不過，呼叫 [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) 將會執行登錄中的許可權變更，而這些變更會在重新開機時保存。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 IMAPI.EXE](using-imapi.md)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 