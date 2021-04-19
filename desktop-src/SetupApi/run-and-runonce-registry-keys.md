---
description: Run 和 RunOnce 登錄機碼會導致每次使用者登入時都會執行程式。
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: 執行和 RunOnce 登錄機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89cf51ad3c7e2096aeffbbd6ed98c02a202f2ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994545"
---
# <a name="run-and-runonce-registry-keys"></a><span data-ttu-id="0d23c-103">執行和 RunOnce 登錄機碼</span><span class="sxs-lookup"><span data-stu-id="0d23c-103">Run and RunOnce Registry Keys</span></span>

<span data-ttu-id="0d23c-104">Run 和 RunOnce 登錄機碼會導致每次使用者登入時都會執行程式。</span><span class="sxs-lookup"><span data-stu-id="0d23c-104">Run and RunOnce registry keys cause programs to run each time that a user logs on.</span></span> <span data-ttu-id="0d23c-105">索引鍵的資料值是不超過260個字元的命令列。</span><span class="sxs-lookup"><span data-stu-id="0d23c-105">The data value for a key is a command line no longer than 260 characters.</span></span> <span data-ttu-id="0d23c-106">藉由新增表單 *描述* - *字串* = *命令列* 的專案來註冊要執行的程式。</span><span class="sxs-lookup"><span data-stu-id="0d23c-106">Register programs to run by adding entries of the form *description*-*string*=*commandline*.</span></span> <span data-ttu-id="0d23c-107">您可以在機碼下撰寫多個專案。</span><span class="sxs-lookup"><span data-stu-id="0d23c-107">You can write multiple entries under a key.</span></span> <span data-ttu-id="0d23c-108">如果有一個以上的程式在任何特定的金鑰下註冊，這些程式執行的順序就會不定。</span><span class="sxs-lookup"><span data-stu-id="0d23c-108">If more than one program is registered under any particular key, the order in which those programs run is indeterminate.</span></span>

<span data-ttu-id="0d23c-109">Windows 登錄包含下列四個執行和 RunOnce 索引鍵：</span><span class="sxs-lookup"><span data-stu-id="0d23c-109">The Windows registry includes the following four Run and RunOnce keys:</span></span>

-   <span data-ttu-id="0d23c-110">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ 執行**</span><span class="sxs-lookup"><span data-stu-id="0d23c-110">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Run**</span></span>
-   <span data-ttu-id="0d23c-111">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ 執行**</span><span class="sxs-lookup"><span data-stu-id="0d23c-111">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Run**</span></span>
-   <span data-ttu-id="0d23c-112">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**</span><span class="sxs-lookup"><span data-stu-id="0d23c-112">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce**</span></span>
-   <span data-ttu-id="0d23c-113">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**</span><span class="sxs-lookup"><span data-stu-id="0d23c-113">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce**</span></span>

<span data-ttu-id="0d23c-114">根據預設，在執行命令列之前，會刪除 RunOnce 索引鍵的值。</span><span class="sxs-lookup"><span data-stu-id="0d23c-114">By default, the value of a RunOnce key is deleted before the command line is run.</span></span> <span data-ttu-id="0d23c-115">您可以在 RunOnce 值名稱前面加上驚嘆號 (！ ) 來延遲刪除值，直到命令執行為止。</span><span class="sxs-lookup"><span data-stu-id="0d23c-115">You can prefix a RunOnce value name with an exclamation point (!) to defer deletion of the value until after the command runs.</span></span> <span data-ttu-id="0d23c-116">如果沒有驚嘆號前置詞，則當您下次啟動電腦時，將不會要求關聯的程式執行。</span><span class="sxs-lookup"><span data-stu-id="0d23c-116">Without the exclamation point prefix, if the RunOnce operation fails the associated program will not be asked to run the next time you start the computer.</span></span>

<span data-ttu-id="0d23c-117">根據預設，當電腦以安全模式啟動時，會忽略這些機碼。</span><span class="sxs-lookup"><span data-stu-id="0d23c-117">By default, these keys are ignored when the computer is started in Safe Mode.</span></span> <span data-ttu-id="0d23c-118">RunOnce 索引鍵的值名稱前面可以加上星號 (\*) 來強制程式在安全模式中執行。</span><span class="sxs-lookup"><span data-stu-id="0d23c-118">The value name of RunOnce keys can be prefixed with an asterisk (\*) to force the program to run even in Safe mode.</span></span>

<span data-ttu-id="0d23c-119">從這些機碼執行的程式不應該在執行期間寫入金鑰，因為這會干擾在機碼下註冊的其他程式的執行。</span><span class="sxs-lookup"><span data-stu-id="0d23c-119">A program run from any of these keys should not write to the key during its execution because this will interfere with the execution of other programs registered under the key.</span></span> <span data-ttu-id="0d23c-120">應用程式應該只針對暫時性狀況使用 RunOnce 索引鍵，例如完成應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="0d23c-120">Applications should use the RunOnce key only for transient conditions, such as to complete application setup.</span></span> <span data-ttu-id="0d23c-121">應用程式不能持續在 RunOnce 下重建專案，因為這會干擾 Windows 安裝程式。</span><span class="sxs-lookup"><span data-stu-id="0d23c-121">An application must not continually recreate entries under RunOnce because this will interfere with Windows Setup.</span></span>
