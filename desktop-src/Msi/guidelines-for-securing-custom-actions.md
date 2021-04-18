---
description: 若要協助維護軟體安裝的安全，請在撰寫 Windows Installer 自訂動作時遵守這些指導方針。
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: 保護自訂動作的指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119c045833b165222756702244cf65bb2225a8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193493"
---
# <a name="guidelines-for-securing-custom-actions"></a><span data-ttu-id="ecb8e-103">保護自訂動作的指導方針</span><span class="sxs-lookup"><span data-stu-id="ecb8e-103">Guidelines for Securing Custom Actions</span></span>

<span data-ttu-id="ecb8e-104">在使用自訂動作撰寫 Windows Installer 套件時遵循下列指導方針，可協助您在安裝期間維護安全的環境：</span><span class="sxs-lookup"><span data-stu-id="ecb8e-104">Adherence to the following guidelines when authoring a Windows Installer package with custom actions helps maintain a secure environment during installation:</span></span>

-   <span data-ttu-id="ecb8e-105">保護您自訂動作所撰寫的任何其他檔案。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-105">Secure any additional files written by your custom action.</span></span>
-   <span data-ttu-id="ecb8e-106">檢查緩衝區長度和自訂動作讀取的所有資料的有效性。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-106">Check buffer lengths and validity of all data read by your custom action.</span></span> <span data-ttu-id="ecb8e-107">這包括可提供資料給您自訂動作的屬性，特別是使用使用者所提供之公用屬性的屬性。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-107">This includes properties that may supply data to your custom action, particularly those that use public properties provided by a user.</span></span>
-   <span data-ttu-id="ecb8e-108">請勿依賴您的安裝套件要執行之所有平臺上的系統不信任的外部 Dll。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-108">Do not rely on external DLLs that are not trusted by the system on all platforms on which your installation package is intended to run.</span></span>
-   <span data-ttu-id="ecb8e-109">請仔細考慮是否要使用使用較 [*高*](e-gly.md) 許可權或模擬的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-109">Carefully consider whether to use custom actions that use [*elevated*](e-gly.md) privileges or impersonation.</span></span> <span data-ttu-id="ecb8e-110">自訂動作（例如「在安裝完成後開啟 URL」、「安裝完成後啟動軟體」或「在安裝完成後啟動讀我檔案」）通常不需要更高的許可權才能運作。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-110">Custom actions such as “open a URL after installation is completed,” “launch the software after installation is complete,” or “launch ReadMe after installation is complete” would not usually require elevated privileges to function.</span></span> <span data-ttu-id="ecb8e-111">如果您的自訂動作必須以較 *高* 的許可權執行，請確定自訂動作程式碼可預防緩衝區溢位，並不慎載入 unsafe 程式碼。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-111">If your custom action must run with *elevated* privileges, be sure that the custom action code guards against buffer overruns and inadvertent loading of unsafe code.</span></span> <span data-ttu-id="ecb8e-112">請注意，在安裝的執行時間期間，安裝程式會將資訊以較 *高* 的許可權傳遞給處理常式，並執行腳本。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-112">Note that during the execution phase of the installation, the installer passes information to a process with *elevated* privileges and runs the script.</span></span> <span data-ttu-id="ecb8e-113">在執行階段期間執行的任何自訂動作，都可能以較 *高* 的許可權執行。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-113">Any custom actions that run during the execution phase may run with *elevated* privileges.</span></span>
-   <span data-ttu-id="ecb8e-114">收集使用者在 UI 順序期間提供的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-114">Gather all information provided by the user during the UI sequence.</span></span> <span data-ttu-id="ecb8e-115">請勿提示使用者提供任何無法使用公用屬性設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-115">Do not prompt the user for any information that can't be set using a public property.</span></span>
-   <span data-ttu-id="ecb8e-116">如果您的腳本自訂動作會展開屬性，請預防自訂動作受到保護，以避免腳本插入的可能性。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-116">If your script custom action expands properties, take precautions that the custom action is secured against the possibility of script injection.</span></span> <span data-ttu-id="ecb8e-117">腳本可能會以純文字的方式登入。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-117">Script may be logged in clear text.</span></span>

<span data-ttu-id="ecb8e-118">另請參閱 [自訂動作安全性](custom-action-security.md)。</span><span class="sxs-lookup"><span data-stu-id="ecb8e-118">See also [Custom Action Security](custom-action-security.md).</span></span>

 

 



