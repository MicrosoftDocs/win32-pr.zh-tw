---
title: ServiceParameters
description: 指定要傳遞至物件的命令列參數，這些參數會透過 LocalService 登錄值傳遞給已安裝供 COM 使用的物件。
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- ServiceParameters 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300960"
---
# <a name="serviceparameters"></a><span data-ttu-id="0d2ac-104">ServiceParameters</span><span class="sxs-lookup"><span data-stu-id="0d2ac-104">ServiceParameters</span></span>

<span data-ttu-id="0d2ac-105">指定要傳遞至物件的命令列參數，這些參數會透過 [**LocalService**](localservice.md) 登錄值傳遞給已安裝供 COM 使用的物件。</span><span class="sxs-lookup"><span data-stu-id="0d2ac-105">Specifies the command-line parameters to be passed to an object installed for use by COM through the [**LocalService**](localservice.md) registry value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0d2ac-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="0d2ac-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a><span data-ttu-id="0d2ac-107">備註</span><span class="sxs-lookup"><span data-stu-id="0d2ac-107">Remarks</span></span>

<span data-ttu-id="0d2ac-108">這是 **REG \_ SZ** 值。</span><span class="sxs-lookup"><span data-stu-id="0d2ac-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="0d2ac-109">在啟動時，此字串會以命令列引數的形式傳遞給服務。</span><span class="sxs-lookup"><span data-stu-id="0d2ac-109">This string is passed to the service as a command-line argument as it is being launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d2ac-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="0d2ac-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d2ac-111">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="0d2ac-111">**LocalService**</span></span>](localservice.md)
</dt> <dt>

[<span data-ttu-id="0d2ac-112">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="0d2ac-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 




