---
title: ADSI 的腳本開始使用
description: 腳本適用于想要建立常用工作之批次腳本的系統管理員。
ms.assetid: ae479d6b-75cf-4659-8a91-c2cbdcf56091
ms.tgt_platform: multiple
keywords:
- ADSI ADSI 的腳本開始使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a85a9ea110ca80f45c3a0f0f1917e8d25c08ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931839"
---
# <a name="getting-started-with-scripting-for-adsi"></a><span data-ttu-id="977cb-104">ADSI 的腳本開始使用</span><span class="sxs-lookup"><span data-stu-id="977cb-104">Getting Started with Scripting for ADSI</span></span>

<span data-ttu-id="977cb-105">腳本適用于想要建立常用工作之批次腳本的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="977cb-105">Scripting is useful for system administrators who want to create batch scripts for frequently used tasks.</span></span>

<span data-ttu-id="977cb-106">若要使用 ADSI 開始撰寫腳本，您必須有執行 Windows 的電腦，或登入包含目錄中電腦帳戶資料的網域。</span><span class="sxs-lookup"><span data-stu-id="977cb-106">To start scripting with ADSI, you must have a computer that runs Windows or be logged on to a domain that contains data for computer accounts in the directory.</span></span>

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a><span data-ttu-id="977cb-107">簡單的腳本範例：尋找電腦帳戶的名稱和位置</span><span class="sxs-lookup"><span data-stu-id="977cb-107">A Simple Scripting Sample: Finding Names and Locations of Computer Accounts</span></span>

<span data-ttu-id="977cb-108">使用文字編輯器建立新的文字檔。</span><span class="sxs-lookup"><span data-stu-id="977cb-108">Create a new text file using a text editor.</span></span> <span data-ttu-id="977cb-109">下列程式碼範例顯示如何尋找電腦帳戶的名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="977cb-109">The following code example shows how to find names and locations of computer accounts.</span></span>


```VB
'---------------------------------------------------------------
' Returns the name and location for all the computer accounts in 
' Active Directory.
'--------------------------------------------------------------- 
Const ADS_SCOPE_SUBTREE = 2
Set objConnection = CreateObject("ADODB.Connection")
Set objCommand =   CreateObject("ADODB.Command")
objConnection.Provider = "ADsDSOObject"
objConnection.Open "Active Directory Provider"
Set objCommand.ActiveConnection = objConnection
objCommand.CommandText = "Select Name, Location from 'LDAP://DC=fabrikam,DC=com' " & "where objectClass='computer'"  
objCommand.Properties("Page Size") = 1000
objCommand.Properties("Timeout") = 30 
objCommand.Properties("Searchscope") = ADS_SCOPE_SUBTREE 
objCommand.Properties("Cache Results") = False 
Set objRecordSet = objCommand.Execute
objRecordSet.MoveFirst
Do Until objRecordSet.EOF
    Wscript.Echo "Computer Name: " & objRecordSet.Fields("Name").Value
    Wscript.Echo "Location: " & objRecordSet.Fields("Location").Value
    objRecordSet.MoveNext
Loop
```



<span data-ttu-id="977cb-110">將檔案儲存為 First.vbs。</span><span class="sxs-lookup"><span data-stu-id="977cb-110">Save the file as First.vbs.</span></span> <span data-ttu-id="977cb-111">修改開頭為 "Objcommand.properties" 的行，以變更您的網域路徑。</span><span class="sxs-lookup"><span data-stu-id="977cb-111">Modify the line that begins with "objCommand.CommandText" to change the path to your domain.</span></span> <span data-ttu-id="977cb-112">在命令提示字元中，輸入命令列的 **cscript First.vbs** 或 Windows 腳本的 First.vbs。</span><span class="sxs-lookup"><span data-stu-id="977cb-112">At the command prompt, type **cscript First.vbs** for a command line or First.vbs for Windows scripting.</span></span> <span data-ttu-id="977cb-113">結果應該會在命令提示字元中傳回。</span><span class="sxs-lookup"><span data-stu-id="977cb-113">The results should be returned in the command prompt.</span></span>

<span data-ttu-id="977cb-114">如需有關編寫 ADSI 腳本的詳細資訊，請參閱 [Active Directory 服務介面腳本](adsi-scripting-tutorial.md)。</span><span class="sxs-lookup"><span data-stu-id="977cb-114">For more information about scripting for ADSI, see [Active Directory Service Interfaces Scripting](adsi-scripting-tutorial.md).</span></span>

 

 




