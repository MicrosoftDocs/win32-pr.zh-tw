---
title: 會話常數
description: WSManSessionFlags 列舉中的會話常數 \_ \_ 會針對連線到遠端電腦的 WSMan. CreateSession 或 IWSMan CreateSession 呼叫指定驗證和其他資訊。
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8417289a218203dbdaee288ff03096d894f4bd4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966380"
---
# <a name="session-constants"></a><span data-ttu-id="cb5a5-103">會話常數</span><span class="sxs-lookup"><span data-stu-id="cb5a5-103">Session Constants</span></span>

<span data-ttu-id="cb5a5-104">**\_ \_ WSManSessionFlags** 列舉中的會話常數會指定 [**CreateSession**](wsman-createsession.md)或 [**IWSMan：： CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)呼叫的驗證和其他資訊，以連接到遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="cb5a5-104">The session constants in the **\_\_WSManSessionFlags** enumeration specify authentication and other information for [**WSMan.CreateSession**](wsman-createsession.md) or [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span> <span data-ttu-id="cb5a5-105">這些常數也與 **Winrm** 命令列工具參數密切相關。</span><span class="sxs-lookup"><span data-stu-id="cb5a5-105">These constants are also closely related to **Winrm** command-line tool switches.</span></span>

## <a name="using-session-constants"></a><span data-ttu-id="cb5a5-106">使用會話常數</span><span class="sxs-lookup"><span data-stu-id="cb5a5-106">Using Session Constants</span></span>

<span data-ttu-id="cb5a5-107">您可以透過兩種不同的方式，設定 [**CreateSession**](wsman-createsession.md) 呼叫的會話旗標。</span><span class="sxs-lookup"><span data-stu-id="cb5a5-107">You can set the Session flags for the call to [**WSMan.CreateSession**](wsman-createsession.md) in two different ways.</span></span> <span data-ttu-id="cb5a5-108">其中一個是較短且更簡單的。</span><span class="sxs-lookup"><span data-stu-id="cb5a5-108">One is shorter and simpler.</span></span> <span data-ttu-id="cb5a5-109">如下列範例所示，較長的方法是找出您想要使用的旗標值，並在腳本中使用該值建立常數。</span><span class="sxs-lookup"><span data-stu-id="cb5a5-109">The longer way, as is shown in the following example, is to locate the value of the flag you want to use and create a constant in your script with that value.</span></span> <span data-ttu-id="cb5a5-110">然後，常數會用來設定 *iFlags* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="cb5a5-110">Then the constant is used to set the value of the *iFlags* parameter.</span></span>

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

<span data-ttu-id="cb5a5-111">如下列範例所示，建議的方式是使用與旗標相關聯的 [**WSMan**](wsman.md) 物件方法。</span><span class="sxs-lookup"><span data-stu-id="cb5a5-111">The recommended way, as shown in the following example, is to use the [**WSMan**](wsman.md) object method associated with the flag.</span></span>

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span data-ttu-id="cb5a5-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**驗證常數**](authentication-constants.md)</span><span class="sxs-lookup"><span data-stu-id="cb5a5-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Authentication Constants**](authentication-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="cb5a5-113">指定驗證方法，以及如何處理憑證伺服器。</span><span class="sxs-lookup"><span data-stu-id="cb5a5-113">Specify the authentication method and how to handle certificate servers.</span></span>

</dd> <dt>

<span data-ttu-id="cb5a5-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**其他會話常數**](other-session-constants.md)</span><span class="sxs-lookup"><span data-stu-id="cb5a5-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Other Session Constants**](other-session-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="cb5a5-115">指定編碼、加密和服務主體名稱埠。</span><span class="sxs-lookup"><span data-stu-id="cb5a5-115">Specify the encoding, encryption, and service principal name port.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="cb5a5-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="cb5a5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb5a5-117">WinRM 常數和列舉</span><span class="sxs-lookup"><span data-stu-id="cb5a5-117">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="cb5a5-118">**WSMan. CreateSession**</span><span class="sxs-lookup"><span data-stu-id="cb5a5-118">**WSMan.CreateSession**</span></span>](wsman-createsession.md)
</dt> <dt>

[<span data-ttu-id="cb5a5-119">遠端連線的驗證</span><span class="sxs-lookup"><span data-stu-id="cb5a5-119">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> </dl>

 

 




