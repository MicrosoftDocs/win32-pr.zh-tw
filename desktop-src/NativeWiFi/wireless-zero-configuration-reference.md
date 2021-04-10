---
description: 包含 Windows XP 和 Windows Server 2003 上的無線零設定服務之程式設計介面的相關資訊。
ms.assetid: cd9e8fc0-0a65-4654-95aa-201751183521
title: 無線零設定參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebe202e16aa38fef617f382559f124772d50a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192640"
---
# <a name="wireless-zero-configuration-reference"></a>無線零設定參考

\[Windows Vista 和 Windows Server 2008 不再支援無線零設定程式設計介面。 相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。 如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]

本節包含 Windows XP 和 Windows Server 2003 上的無線零設定服務之程式設計介面的相關資訊。 主題包括：

-   [無線零設定函數](wireless-zero-configuration-functions.md)
-   [無線零設定結構](wireless-zero-configuration-structures.md)

無線零設定是 Windows XP 和 Windows Server 2003 上的 Windows 服務，可用來設定和管理無線介面卡上的無線網路連線。 無線零設定的服務名稱是 WZCSVC。 在 Windows XP 上，WZCSVC 服務的顯示名稱為「無線零設定」。 在 Windows Server 2003 上，WZCSVC 服務的顯示名稱為「無線設定」。

無線零設定服務通常是在開機時啟動。 只有在無線零設定服務啟動時，才能使用無線零設定服務的程式設計介面。 如果未啟動無線零設定服務，無線零設定函數將會傳回錯誤。

若要啟用無線零設定服務，讓它自動啟動，請移至 [ **開始** ] 按鈕。 選取 [ **設定** ] 選項，然後選取 [ **主控台**]。 如果您使用的是 Windows XP view，請選取 [ **效能及維護** ] 類別，然後選取 [系統 **管理工具**]。 如果您使用的是傳統視圖，請選取 [系統 **管理工具**]。 按一下左窗格中的 [ **服務** ] 圖示。 按一下右窗格中的 [無線零設定] 圖示，並將 [dropbox] 的 [ **啟動類型** ] 變更為 [ **自動**]。 此設定會將服務設定為在開機時自動啟動。 然後按一下 [ **開始** ] 按鈕，啟動無線零無線零設定服務，然後按一下 [ **確定]** 按鈕。

您也可以從命令提示字元啟動和停止無線零設定。 若要啟動無線零設定，請執行下列命令：

**net start wzcsvc**

若要停止無線零設定，請執行下列命令：

**net stop wzcsvc**

 

 



