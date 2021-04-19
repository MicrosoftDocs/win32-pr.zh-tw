---
description: 具有特殊許可權的作業需要安全性許可權，例如腳本 API 常數中的 SeLoadDriverPrivilege (wbemPrivilegeLoadDriver) ，也就是載入設備磁碟機的帳戶必須啟用的許可權。
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: 執行具有特殊許可權的作業
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37abba9d774025825611e311f08414b50e660f65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977259"
---
# <a name="executing-privileged-operations"></a><span data-ttu-id="7b085-103">執行具有特殊許可權的作業</span><span class="sxs-lookup"><span data-stu-id="7b085-103">Executing Privileged Operations</span></span>

<span data-ttu-id="7b085-104">具有特殊許可權的作業需要安全性許可權，例如 [腳本 API 常數](scripting-api-constants.md)中的 **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver**) ，也就是載入設備磁碟機的帳戶必須啟用的許可權。</span><span class="sxs-lookup"><span data-stu-id="7b085-104">Privileged operations require security privileges such as **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** in the [Scripting API Constants](scripting-api-constants.md)), a privilege that must be enabled for an account that is loading a device driver.</span></span> <span data-ttu-id="7b085-105">您無法透過 WMI 將許可權新增至系統管理員或使用者，您只能啟用帳戶已經擁有的許可權。</span><span class="sxs-lookup"><span data-stu-id="7b085-105">You cannot add privileges to an administrator or user through WMI, you can only enable privileges that the account already has.</span></span> <span data-ttu-id="7b085-106">如需許可權清單，請參閱 [**許可權 \_ 常數**](privilege-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="7b085-106">For a list of privileges, see [**Privilege\_Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="7b085-107">根據預設，電腦上的本機使用者可以讀取 [*WMI 存放庫*](gloss-w.md)中的靜態資料、寫入提供者提供的實例，以及執行提供者方法，除非提供者強制執行其專屬的特殊安全性需求。</span><span class="sxs-lookup"><span data-stu-id="7b085-107">By default, a local user on a computer can read static data from the [*WMI repository*](gloss-w.md), write to instances supplied by providers, and execute provider methods, unless the provider enforces special security requirements of its own.</span></span> <span data-ttu-id="7b085-108">只有系統管理員可以連線 [到遠端電腦](connecting-to-wmi-on-a-remote-computer.md)、變更安全描述項，或變更靜態 wmi 儲存機制資料，例如 wmi 類別定義。</span><span class="sxs-lookup"><span data-stu-id="7b085-108">Only administrators can [connect to a remote computer](connecting-to-wmi-on-a-remote-computer.md), change security descriptors, or change static WMI repository data, such as a WMI class definition.</span></span> <span data-ttu-id="7b085-109">遠端連線會啟用擁有權限。</span><span class="sxs-lookup"><span data-stu-id="7b085-109">All privileges are enabled for a remote connection.</span></span> <span data-ttu-id="7b085-110">如需詳細資訊，請參閱 [保護遠端 WMI 連接](securing-a-remote-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="7b085-110">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="7b085-111">C + + 的許可權常數不同于自動化語言（例如 Visual Basic）所使用的常數。</span><span class="sxs-lookup"><span data-stu-id="7b085-111">The privilege constants for C++ differ from those that are used by automation languages such as Visual Basic.</span></span> <span data-ttu-id="7b085-112">腳本必須使用常數的值，而不是名稱。</span><span class="sxs-lookup"><span data-stu-id="7b085-112">Scripts must use the value of the constant rather than the name.</span></span> <span data-ttu-id="7b085-113">如需詳細資訊，請參閱使用 [c + + 執行特殊許可權作業](executing-privileged-operations-using-c-.md) 或 [使用 VBScript 執行特殊許可權作業](executing-privileged-operations-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="7b085-113">For more information, see [Executing Privileged Operations Using C++](executing-privileged-operations-using-c-.md) or [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="7b085-114">使用 WMI 時，拒絕存取錯誤的常見原因是缺少作業的已啟用許可權，例如取得 [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))的所有實例。</span><span class="sxs-lookup"><span data-stu-id="7b085-114">A common cause of access denied errors when using WMI is the lack of an enabled privilege for operations, such as getting all instances of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)).</span></span> <span data-ttu-id="7b085-115">若未啟用 **SeSecurity** 許可權，就無法存取安全性記錄檔檔。</span><span class="sxs-lookup"><span data-stu-id="7b085-115">Without enabling the **SeSecurity** privilege, you cannot access the Security log file.</span></span>

<span data-ttu-id="7b085-116">下列 VBScript 程式碼範例示範如何在標記字串中設定 **SeSecurity** 許可權。</span><span class="sxs-lookup"><span data-stu-id="7b085-116">The following VBScript code example shows how to set the **SeSecurity** privilege in the moniker string.</span></span> <span data-ttu-id="7b085-117">在用於標記中時，以括弧括住的許可權名稱會卸載初始的「Se」。</span><span class="sxs-lookup"><span data-stu-id="7b085-117">When used in the moniker, the privilege name in parentheses drops the initial "Se".</span></span> <span data-ttu-id="7b085-118">如需詳細資訊，請參閱 [建立標記字串](constructing-a-moniker-string.md)。</span><span class="sxs-lookup"><span data-stu-id="7b085-118">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate,(Security)}!\\" _
    & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery _
    ("Select * from Win32_NTEventLogFile " _
    & "Where LogFileName='Security'")
For Each LogFile in colFiles
Wscript.Echo LogFile.NumberOfRecords
Next
```



## <a name="related-topics"></a><span data-ttu-id="7b085-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b085-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b085-120">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="7b085-120">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 
