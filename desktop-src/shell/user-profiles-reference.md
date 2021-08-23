---
description: 下列 API 元素會與使用者設定檔搭配使用。
title: 使用者設定檔參考
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 86871866-bb90-4287-9640-0a6cd136a800
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4b064eefae4916576cb8ccc6b3dfe058ea4e2e34f960315b74d384194f61ec99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967828"
---
# <a name="user-profiles-reference"></a>使用者設定檔參考

下列 API 元素會與使用者設定檔搭配使用。

## <a name="functions"></a>函式



| 函式                                                                   | 描述                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | 抓取指定使用者的環境變數。                                                   |
| [**CreateProfile**](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | 建立新的使用者設定檔。  (Windows Vista （含）以後版本。 )                                                    |
| [**DeleteProfile**](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | 從指定的電腦刪除使用者設定檔和所有使用者相關的設定。                           |
| [**DestroyEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | 釋放 [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) 函數所建立的環境變數。 |
| [**ExpandEnvironmentStringsForUser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | 使用針對指定使用者所建立的環境區塊來展開來源字串。                  |
| [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | 抓取所有使用者設定檔之根目錄的路徑。                                                      |
| [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | 抓取預設使用者設定檔之根目錄的路徑。                                                   |
| [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | 抓取儲存所有使用者設定檔之根目錄的路徑。                                  |
| [**GetProfileType**](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | 抓取為目前使用者載入的配置檔案類型。                                                    |
| [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | 抓取指定使用者設定檔之根目錄的路徑。                                     |
| [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | 載入指定的使用者設定檔。                                                                           |
| [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | 卸載 [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) 函數所載入的使用者設定檔。          |



 

不支援 [**CreateUserProfileEx**](createuserprofileex.md) 函數。

## <a name="structures"></a>結構



| 結構                          | 描述                                |
|------------------------------------|--------------------------------------------|
| [**PROFILEINFO.TXT**](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | 包含使用者設定檔的相關資訊。 |



 

 

 



