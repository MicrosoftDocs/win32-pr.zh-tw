---
description: 當使用者第一次登入電腦時，系統會自動為每位使用者建立本機使用者設定檔。 系統會自動在本機電腦上的使用者設定檔中維護每個使用者工作環境的設定。
title: 本機使用者設定檔
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0e6c060e-025e-4d00-9b92-4f3b7bf66dda
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 713adc7db522ff473de42a3ecaa2a1a0671f95ee5f4039f0039a196304c7aa4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220153"
---
# <a name="local-user-profiles"></a>本機使用者設定檔

Windows 安全性需要電腦上每個使用者帳戶的使用者設定檔。 當使用者第一次登入電腦時，系統會自動為每位使用者建立 *本機使用者設定檔* 。 系統會自動在本機電腦上的使用者設定檔中維護每個使用者工作環境的設定。

WindowsVista 和更新版本：使用者設定檔是透過 [**使用者帳戶**] 控制台專案進行管理。

Windows 2000 和 Windows XP：若要複製或刪除使用者設定檔，請從主控台中選取 [**系統**]，然後選取 [ **Advanced** ] 索引標籤，然後在 [**使用者設定檔**] 區域中選取 [**設定**] 按鈕。

當使用者使用 [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) 函數登入時，不會自動載入使用者的設定檔。 若要以程式設計方式載入使用者設定檔，請使用 [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) 函數。 若要卸載 **LoadUserProfile** 所載入的使用者設定檔，請呼叫 [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) 函數。

 

 
