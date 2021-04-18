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
# <a name="asking-the-user-for-credentials"></a><span data-ttu-id="ffead-103">要求使用者提供認證</span><span class="sxs-lookup"><span data-stu-id="ffead-103">Asking the User for Credentials</span></span>

<span data-ttu-id="ffead-104">您的應用程式可能需要提示使用者輸入使用者名稱和密碼資訊，以避免儲存系統管理員密碼或確認權杖具有適當的許可權。</span><span class="sxs-lookup"><span data-stu-id="ffead-104">Your application may need to prompt the user for user name and password information to avoid storing an administrator password or to verify that the token holds the appropriate privileges.</span></span>

<span data-ttu-id="ffead-105">不過，只要提示認證，就可以訓練使用者將這些對話方塊提供給出現在螢幕上的任何隨機、無法辨識的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ffead-105">However, simply prompting for credentials may train users to supply those to any random, unidentified dialog box that appears on the screen.</span></span> <span data-ttu-id="ffead-106">建議您執行下列程式，以減少定型效果。</span><span class="sxs-lookup"><span data-stu-id="ffead-106">The following procedure is recommended to reduce that training effect.</span></span>

<span data-ttu-id="ffead-107">**若要正確取得使用者認證**</span><span class="sxs-lookup"><span data-stu-id="ffead-107">**To properly acquire user credentials**</span></span>

1.  <span data-ttu-id="ffead-108">使用您的應用程式中很清楚的訊息來通知使用者，他們將會看到要求其使用者名稱和密碼的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ffead-108">Inform the user, by using a message that is clearly part of your application, that they will see a dialog box that requests their user name and password.</span></span> <span data-ttu-id="ffead-109">您也可以在呼叫 [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa)時使用 [**CREDUI \_ 資訊**](/windows/desktop/api/wincred/ns-wincred-credui_infoa)結構，以傳達識別資料或訊息。</span><span class="sxs-lookup"><span data-stu-id="ffead-109">You can also use the [**CREDUI\_INFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) structure on the call to [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to convey identifying data or a message.</span></span>
2.  <span data-ttu-id="ffead-110">呼叫 [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa)。</span><span class="sxs-lookup"><span data-stu-id="ffead-110">Call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).</span></span> <span data-ttu-id="ffead-111">請注意，為使用者名稱和密碼資訊指定的最大字元數包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="ffead-111">Note that the maximum number of characters specified for user name and password information includes the terminating null character.</span></span>
3.  <span data-ttu-id="ffead-112">呼叫 [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) 和 [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) ，以確認您已取得適當的認證。</span><span class="sxs-lookup"><span data-stu-id="ffead-112">Call [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) and [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) to verify that you obtained appropriate credentials.</span></span>

<span data-ttu-id="ffead-113">下列範例示範如何呼叫 [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) 來要求使用者輸入使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="ffead-113">The following example shows how to call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to ask the user for a user name and password.</span></span> <span data-ttu-id="ffead-114">它一開始會填入 CREDUI \_ 資訊結構，其中包含要使用哪些提示的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ffead-114">It begins by filling in a CREDUI\_INFO structure with information about what prompts to use.</span></span> <span data-ttu-id="ffead-115">接下來，程式碼會以零填滿兩個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ffead-115">Next, the code fills two buffers with zeros.</span></span> <span data-ttu-id="ffead-116">這樣做的目的是為了確保不會將任何資訊傳遞給可能會向使用者顯示舊使用者名稱或密碼的函式。</span><span class="sxs-lookup"><span data-stu-id="ffead-116">This is done to ensure that no information gets passed to the function that might reveal an old user name or password to the user.</span></span> <span data-ttu-id="ffead-117">呼叫 **CredUIPromptForCredentials** 會顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ffead-117">The call to **CredUIPromptForCredentials** brings up the dialog box.</span></span> <span data-ttu-id="ffead-118">基於安全性理由，此範例會使用 CREDUI \_ 旗 \_ 標 \_ 不 \_ 保存旗標，以防止作業系統儲存密碼，因為它可能會被公開。</span><span class="sxs-lookup"><span data-stu-id="ffead-118">For security reasons, this example uses the CREDUI\_FLAGS\_DO\_NOT\_PERSIST flag to prevent the operating system from storing the password because it might then be exposed.</span></span> <span data-ttu-id="ffead-119">如果沒有任何錯誤， **CredUIPromptForCredentials** 會填入 PszName 和 pszPwd 變數，並傳回零。</span><span class="sxs-lookup"><span data-stu-id="ffead-119">If there are no errors, **CredUIPromptForCredentials** fills in the pszName and pszPwd variables and returns zero.</span></span> <span data-ttu-id="ffead-120">當應用程式完成使用認證時，它應該在緩衝區中放置零，以防止意外顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="ffead-120">When the application has finished using the credentials, it should put zeros in the buffers to prevent the information from being accidentally revealed.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ffead-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="ffead-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffead-122">**CredUICmdLinePromptForCredentials**</span><span class="sxs-lookup"><span data-stu-id="ffead-122">**CredUICmdLinePromptForCredentials**</span></span>](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[<span data-ttu-id="ffead-123">**CREDUI \_ UINFO**</span><span class="sxs-lookup"><span data-stu-id="ffead-123">**CREDUI\_UINFO**</span></span>](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
