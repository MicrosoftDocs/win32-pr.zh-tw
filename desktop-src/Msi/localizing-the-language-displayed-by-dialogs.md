---
description: Windows Installer 服務會在所有對話方塊中使用目前使用者的語言，直到開啟 Windows Installer 封裝為止。
ms.assetid: c9902990-7a26-48fd-96ac-4d5a749e34be
title: 將對話方塊所顯示的語言當地語系化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042b2b7f9ac256ebad265b75a8756fc422403e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997159"
---
# <a name="localizing-the-language-displayed-by-dialogs"></a><span data-ttu-id="430d0-103">將對話方塊所顯示的語言當地語系化</span><span class="sxs-lookup"><span data-stu-id="430d0-103">Localizing the Language Displayed by Dialogs</span></span>

<span data-ttu-id="430d0-104">Windows Installer 服務會在所有對話方塊中使用目前使用者的語言，直到開啟 Windows Installer 封裝為止。</span><span class="sxs-lookup"><span data-stu-id="430d0-104">The Windows Installer service uses the current user's language in all dialogs until a Windows Installer package is opened.</span></span> <span data-ttu-id="430d0-105">Windows Installer 使用 **GetUserDefaultUILanguage** 來決定這一點。</span><span class="sxs-lookup"><span data-stu-id="430d0-105">The Windows Installer determines this by using **GetUserDefaultUILanguage**.</span></span> <span data-ttu-id="430d0-106">開啟 Windows Installer 套件時，安裝程式會使用 [ [**範本摘要**](template-summary.md) ] 屬性所指定的封裝語言來顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="430d0-106">When a Windows Installer package is opened, the installer displays dialogs using the package's language as specified by the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="430d0-107">如需當地語系化 Windows Installer 套件語言的詳細資訊，另請參閱 [當地語系化範例](a-localization-example.md)。</span><span class="sxs-lookup"><span data-stu-id="430d0-107">For more information about localizing the language of a Windows Installer package, see also [A Localization Example](a-localization-example.md).</span></span>

 

 



