---
description: 如果電腦是在網路上執行 Windows 2000 Server 或更新版本，則使用者可以將其設定檔儲存在伺服器上。 這些設定檔稱為漫遊使用者設定檔。
title: 漫遊使用者設定檔
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8af06fdf-be99-4295-8f11-7d7f68e66956
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e3b95374b06c4efc665b231b4c7e1f1d81861dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973341"
---
# <a name="roaming-user-profiles"></a>漫遊使用者設定檔

如果電腦是在網路上執行 Windows 2000 Server 或更新版本，則使用者可以將其設定檔儲存在伺服器上。 這些設定檔稱為 *漫遊使用者設定檔*。

漫遊使用者設定檔有下列優點：

-   自動資源可用性。 當使用者登入網路上的任何電腦時，會自動使用使用者的唯一設定檔。 使用者不需要在網路上使用的每部電腦上建立設定檔。
-   簡化的電腦更換與備份。 當使用者的電腦必須被取代時，就可以輕鬆地予以取代，因為所有使用者的設定檔資訊都是在網路上分開維護，而不受個別電腦的影響。 當使用者第一次登入新電腦時，會將使用者設定檔的伺服器複本複製到新電腦。

當使用者使用 [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) 函數登入時，不會自動載入使用者的設定檔。 若要以程式設計方式載入漫遊使用者設定檔，請使用 [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) 函數。 若要卸載 **LoadUserProfile** 所載入的漫遊使用者設定檔，請呼叫 [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) 函數。

 

 
