---
description: Nondeferred 呼叫動態連結程式庫或腳本的自訂動作，可能會存取執行中的安裝，以查詢或修改目前安裝會話的屬性。
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: 從自訂動作內部存取目前的安裝程式會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a870247f70742d408c0f5d1d0e67f20cef65d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944051"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a><span data-ttu-id="178b4-103">從自訂動作內部存取目前的安裝程式會話</span><span class="sxs-lookup"><span data-stu-id="178b4-103">Accessing the Current Installer Session from Inside a Custom Action</span></span>

<span data-ttu-id="178b4-104">Nondeferred 呼叫 [動態連結程式庫](dynamic-link-libraries.md) 或 [腳本](scripts.md) 的自訂動作，可能會存取執行中的安裝，以查詢或修改目前安裝會話的屬性。</span><span class="sxs-lookup"><span data-stu-id="178b4-104">Nondeferred custom actions that call [dynamic-link libraries](dynamic-link-libraries.md) or [scripts](scripts.md) may access a running installation to query or modify the attributes of the current installation session.</span></span> <span data-ttu-id="178b4-105">每個進程只能有一個 **會話** 物件，而且自訂動作腳本不能嘗試建立另一個會話。</span><span class="sxs-lookup"><span data-stu-id="178b4-105">Only one **Session** object can exist for each process, and custom action scripts must not attempt to create another session.</span></span>

<span data-ttu-id="178b4-106">自訂動作只能加入、修改或移除資料庫中的暫存資料列、資料行或資料表。</span><span class="sxs-lookup"><span data-stu-id="178b4-106">Custom actions can only add, modify, or remove temporary rows, columns, or tables from a database.</span></span> <span data-ttu-id="178b4-107">自訂動作無法修改資料庫中的持續性資料，例如，儲存在磁片上之資料庫的資料。</span><span class="sxs-lookup"><span data-stu-id="178b4-107">Custom actions cannot modify persistent data in a database, for example, data that is a part of the database stored on disk.</span></span>

[<span data-ttu-id="178b4-108">動態連結程式庫</span><span class="sxs-lookup"><span data-stu-id="178b4-108">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)

<span data-ttu-id="178b4-109">若要存取執行中的安裝，呼叫動態連結程式庫 (DLL) 的自訂動作會傳遞給目前會話的型別 MSIHANDLE 控制碼，作為 [CustomAction 資料表](customaction-table.md)的目標資料行中所指定之 DLL 進入點的唯一引數。</span><span class="sxs-lookup"><span data-stu-id="178b4-109">To access a running installation, custom actions that call dynamic-link libraries (DLL) are passed a handle of the type MSIHANDLE for the current session as the only argument to the DLL entry point named in the Target column of the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="178b4-110">因為安裝程式提供此控制碼，所以自訂動作不應該關閉它，例如，若要從安裝程式接收控制碼 *hInstall* ，自訂動作函式的宣告方式如下。</span><span class="sxs-lookup"><span data-stu-id="178b4-110">Because the installer provides this handle, the custom action should not close it, for example, to receive the handle *hInstall* from the installer, the custom action function is declared as follows.</span></span>


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="178b4-111">若要取得目前資料庫的唯讀存取權，請呼叫 [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)來取得資料庫控制碼。</span><span class="sxs-lookup"><span data-stu-id="178b4-111">For read-only access to the current database obtain the database handle by calling [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase).</span></span> <span data-ttu-id="178b4-112">如需詳細資訊，請參閱 [取得資料庫控制碼](obtaining-a-database-handle.md)。</span><span class="sxs-lookup"><span data-stu-id="178b4-112">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

[<span data-ttu-id="178b4-113">指令碼</span><span class="sxs-lookup"><span data-stu-id="178b4-113">Scripts</span></span>](scripts.md)

<span data-ttu-id="178b4-114">以 VBScript 或 JScript 撰寫的自訂動作可以使用 [**Session 物件**](session-object.md)存取目前的安裝會話。</span><span class="sxs-lookup"><span data-stu-id="178b4-114">Custom actions written in VBScript or JScript can access the current installation session by using the [**Session Object**](session-object.md).</span></span> <span data-ttu-id="178b4-115">安裝程式會建立名為「會話」的 **會話** 物件，該物件會參考目前的安裝。</span><span class="sxs-lookup"><span data-stu-id="178b4-115">The installer creates a **Session** object named "Session" that references the current installation.</span></span> <span data-ttu-id="178b4-116">若為目前資料庫的唯讀存取權，請使用 **Session** 物件的 [**database**](session-database.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="178b4-116">For read-only access to the current database use the [**Database**](session-database.md) property of the **Session** object.</span></span>

<span data-ttu-id="178b4-117">因為腳本是從 [**會話**](session-object.md) 物件的內容中執行，所以並不一定需要完整限定屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="178b4-117">Because a script is run from the context of the [**Session**](session-object.md) object, it is not always necessary to fully qualify properties and methods.</span></span> <span data-ttu-id="178b4-118">在下列範例中，使用 VBScript 時，我的參考可以取代 **會話** 物件，例如，下列三行是相等的。</span><span class="sxs-lookup"><span data-stu-id="178b4-118">In the following example, when using VBScript, the Me reference can replace the **Session** object, for example, the following three lines are equivalent.</span></span>


```VB
Session.SetInstallLevel 1
```




```VB
Me.SetInstallLevel 1
```




```VB
SetInstallLevel 1
```



[<span data-ttu-id="178b4-119">可執行檔</span><span class="sxs-lookup"><span data-stu-id="178b4-119">Executable Files</span></span>](executable-files.md)

<span data-ttu-id="178b4-120">您無法從呼叫以命令列啟動之可執行檔的自訂動作（例如， [自訂動作類型 2](custom-action-type-2.md) 和 [自訂動作類型 18](custom-action-type-18.md)）存取目前的安裝程式會話。</span><span class="sxs-lookup"><span data-stu-id="178b4-120">You cannot access the current installer session from custom actions that call executable files launched with a command-line, for example, [Custom Action Type 2](custom-action-type-2.md) and [Custom Action Type 18](custom-action-type-18.md).</span></span>

[<span data-ttu-id="178b4-121">延後執行自訂動作</span><span class="sxs-lookup"><span data-stu-id="178b4-121">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)

<span data-ttu-id="178b4-122">您無法從順延強制自訂動作存取目前的安裝程式會話或所有屬性資料。</span><span class="sxs-lookup"><span data-stu-id="178b4-122">You cannot access the current installer session or all property data from a deferred execution custom action.</span></span> <span data-ttu-id="178b4-123">如需詳細資訊，請參閱 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="178b4-123">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="178b4-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="178b4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="178b4-125">從自訂動作內部存取資料庫或會話</span><span class="sxs-lookup"><span data-stu-id="178b4-125">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



