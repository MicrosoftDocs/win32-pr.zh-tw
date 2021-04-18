---
description: 您的應用程式可能需要提示使用者輸入使用者名稱和密碼資訊，以避免儲存系統管理員密碼或確認權杖具有適當的許可權。
ms.assetid: 966de0cc-63de-4430-843f-668de2dfe0a6
title: 要求使用者提供認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adb315837d86a9f1dda4075b8d89db33f0dd22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978082"
---
# <a name="asking-the-user-for-credentials"></a>要求使用者提供認證

您的應用程式可能需要提示使用者輸入使用者名稱和密碼資訊，以避免儲存系統管理員密碼或確認權杖具有適當的許可權。

不過，只要提示認證，就可以訓練使用者將這些對話方塊提供給出現在螢幕上的任何隨機、無法辨識的對話方塊。 建議您執行下列程式，以減少定型效果。

**若要正確取得使用者認證**

1.  使用您的應用程式中很清楚的訊息來通知使用者，他們將會看到要求其使用者名稱和密碼的對話方塊。 您也可以在呼叫 [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa)時使用 [**CREDUI \_ 資訊**](/windows/desktop/api/wincred/ns-wincred-credui_infoa)結構，以傳達識別資料或訊息。
2.  呼叫 [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa)。 請注意，為使用者名稱和密碼資訊指定的最大字元數包含終止的 null 字元。
3.  呼叫 [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) 和 [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) ，以確認您已取得適當的認證。

下列範例示範如何呼叫 [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) 來要求使用者輸入使用者名稱和密碼。 它一開始會填入 CREDUI \_ 資訊結構，其中包含要使用哪些提示的相關資訊。 接下來，程式碼會以零填滿兩個緩衝區。 這樣做的目的是為了確保不會將任何資訊傳遞給可能會向使用者顯示舊使用者名稱或密碼的函式。 呼叫 **CredUIPromptForCredentials** 會顯示對話方塊。 基於安全性理由，此範例會使用 CREDUI \_ 旗 \_ 標 \_ 不 \_ 保存旗標，以防止作業系統儲存密碼，因為它可能會被公開。 如果沒有任何錯誤， **CredUIPromptForCredentials** 會填入 PszName 和 pszPwd 變數，並傳回零。 當應用程式完成使用認證時，它應該在緩衝區中放置零，以防止意外顯示資訊。


```C++
CREDUI_INFO cui;
TCHAR pszName[CREDUI_MAX_USERNAME_LENGTH+1];
TCHAR pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1];
BOOL fSave;
DWORD dwErr;
 
cui.cbSize = sizeof(CREDUI_INFO);
cui.hwndParent = NULL;
//  Ensure that MessageText and CaptionText identify what credentials
//  to use and which application requires them.
cui.pszMessageText = TEXT("Enter administrator account information");
cui.pszCaptionText = TEXT("CredUITest");
cui.hbmBanner = NULL;
fSave = FALSE;
SecureZeroMemory(pszName, sizeof(pszName));
SecureZeroMemory(pszPwd, sizeof(pszPwd));
dwErr = CredUIPromptForCredentials( 
    &cui,                         // CREDUI_INFO structure
    TEXT("TheServer"),            // Target for credentials
                                  //   (usually a server)
    NULL,                         // Reserved
    0,                            // Reason
    pszName,                      // User name
    CREDUI_MAX_USERNAME_LENGTH+1, // Max number of char for user name
    pszPwd,                       // Password
    CREDUI_MAX_PASSWORD_LENGTH+1, // Max number of char for password
    &fSave,                       // State of save check box
    CREDUI_FLAGS_GENERIC_CREDENTIALS |  // flags
    CREDUI_FLAGS_ALWAYS_SHOW_UI |
    CREDUI_FLAGS_DO_NOT_PERSIST);  

if(!dwErr)
{
    //  Put code that uses the credentials here.
 
    //  When you have finished using the credentials,
    //  erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[**CREDUI \_ UINFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
