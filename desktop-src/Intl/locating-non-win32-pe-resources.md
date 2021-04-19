---
description: 尋找非 Win32 PE 資源
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: 尋找非 Win32 PE 資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079288cd6200eb64289f474636cbc8dc046c1e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978831"
---
# <a name="locating-non-win32-pe-resources"></a><span data-ttu-id="2b92b-103">尋找非 Win32 PE 資源</span><span class="sxs-lookup"><span data-stu-id="2b92b-103">Locating Non-Win32 PE Resources</span></span>

<span data-ttu-id="2b92b-104">若要尋找非 Win32 PE 資源，您的應用程式應該先呼叫 [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) 函式，以找出要從中載入資源的特定語言資源檔。</span><span class="sxs-lookup"><span data-stu-id="2b92b-104">To locate non-Win32 PE resources, your application should first call the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function to locate the language-specific resource file from which to load resources.</span></span> <span data-ttu-id="2b92b-105">如果應用程式是遵循系統語言設定，則必須使用針對 DwFlags 指定的 \_ mui \_ 語言 \| 名稱 mui \_ 使用者慣用 UI 語言來呼叫函式，並為 \_ \_ \_ *pwszLanguage* 指定 **Null** 。 </span><span class="sxs-lookup"><span data-stu-id="2b92b-105">If the application is following system language settings, it must call the function with MUI\_LANGUAGE\_NAME \| MUI\_USER\_PREFERRED\_UI\_LANGUAGES specified for *dwFlags* and **NULL** specified for *pwszLanguage*.</span></span> <span data-ttu-id="2b92b-106">如果應用程式是依照應用程式特定的語言設定，則會使用 **GetFileMUIPath** ，藉由在 *pwszLanguage* 參數中指定語言來判斷特定語言的檔案是否存在。</span><span class="sxs-lookup"><span data-stu-id="2b92b-106">If the application is following application-specific language settings, it uses **GetFileMUIPath** to determine if a language-specific file exists by specifying the language in the *pwszLanguage* parameter.</span></span>

<span data-ttu-id="2b92b-107">呼叫 [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)之後，應用程式必須定義自訂功能以載入資源模組，並從中載入特定資源。</span><span class="sxs-lookup"><span data-stu-id="2b92b-107">After the call to [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), the application must define custom functionality to load the resource module and load specific resources from it.</span></span> <span data-ttu-id="2b92b-108">例如，如果您使用 .txt 或 .xml 資源檔，應用程式必須使用 TXT 或 XML 剖析器來載入檔案，然後針對每個必要的資源剖析檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="2b92b-108">For example, if you are using a .txt or .xml resource file, the application must use a TXT or XML parser to load the file and then parse the contents of the file for each required resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b92b-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b92b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b92b-110">使用多語系消費者介面</span><span class="sxs-lookup"><span data-stu-id="2b92b-110">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="2b92b-111">**GetFileMUIPath**</span><span class="sxs-lookup"><span data-stu-id="2b92b-111">**GetFileMUIPath**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



