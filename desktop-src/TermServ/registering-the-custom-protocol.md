---
title: 註冊通訊協定管理員
description: 您至少必須為通訊協定管理員建立一個登錄值專案，遠端桌面服務服務才能將它具現化。
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0193440414c1b95b741b6e1f0257d8d1aa3e00b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372010"
---
# <a name="registering-the-protocol-manager"></a><span data-ttu-id="1cfe0-103">註冊通訊協定管理員</span><span class="sxs-lookup"><span data-stu-id="1cfe0-103">Registering the Protocol Manager</span></span>

<span data-ttu-id="1cfe0-104">您至少必須為通訊協定管理員建立一個登錄值專案，遠端桌面服務服務才能將它具現化。</span><span class="sxs-lookup"><span data-stu-id="1cfe0-104">You must create at least one registry value entry for your protocol manager so that the Remote Desktop Services service can instantiate it.</span></span>

## <a name="registry-location"></a><span data-ttu-id="1cfe0-105">登錄位置</span><span class="sxs-lookup"><span data-stu-id="1cfe0-105">Registry Location</span></span>

<span data-ttu-id="1cfe0-106">針對您的通訊協定所使用的每個接聽程式 ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) ，在下列位置建立登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="1cfe0-106">Create a registry key in the following location for each listener ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) that your protocol uses.</span></span> <span data-ttu-id="1cfe0-107">在此範例中，新的接聽程式金鑰稱為 *MyListener1* 和 *MyListener2*。</span><span class="sxs-lookup"><span data-stu-id="1cfe0-107">In this example, the new listener keys are called *MyListener1* and *MyListener2*.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Terminal Server
               WinStations
                  RDP-Tcp
                  MyListener1
                  MyListener2
```

<span data-ttu-id="1cfe0-108">您可以在此位置中查看預設的 **rdp-tcp 接聽程式** 金鑰底下的值專案，以供參考。</span><span class="sxs-lookup"><span data-stu-id="1cfe0-108">For reference, you can view the value entries under the default **RDP-Tcp** listener key in this location.</span></span>

## <a name="registry-value-entries"></a><span data-ttu-id="1cfe0-109">登錄值專案</span><span class="sxs-lookup"><span data-stu-id="1cfe0-109">Registry Value Entries</span></span>

<span data-ttu-id="1cfe0-110">通訊協定的接聽程式金鑰必須有一個稱為 **LoadableProtocol \_ Object** 的值專案</span><span class="sxs-lookup"><span data-stu-id="1cfe0-110">The listener key for the protocol must have a value entry called **LoadableProtocol\_Object**</span></span><dl> <dt>

<span data-ttu-id="1cfe0-111">資料類型</span><span class="sxs-lookup"><span data-stu-id="1cfe0-111">Data type</span></span>
</dt> <dd><span data-ttu-id="1cfe0-112">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1cfe0-112">REG_SZ</span></span></dd> <span data-ttu-id="1cfe0-113"></dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> 介面。 ) 遠端桌面服務服務會在找到登錄中的接聽程式之後，使用此 CLSID 將此接聽程式的通訊協定管理員具現化。</span><span class="sxs-lookup"><span data-stu-id="1cfe0-113"></dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> interface.) The Remote Desktop Services service uses this CLSID to instantiate the protocol manager for this listener after it finds the listener in the registry.</span></span>

<span data-ttu-id="1cfe0-114">如果您的通訊協定提供者使用一個以上的接聽程式，遠端桌面服務服務只會建立一個通訊協定管理員實例，並使用它來針對每個接聽程式呼叫 [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) 一次。</span><span class="sxs-lookup"><span data-stu-id="1cfe0-114">If your protocol provider uses more than one listener, the Remote Desktop Services service only creates one instance of the protocol manager, and uses it to call [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) once for each listener.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cfe0-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="1cfe0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cfe0-116">建立遠端桌面通訊協定提供者</span><span class="sxs-lookup"><span data-stu-id="1cfe0-116">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dt>

[<span data-ttu-id="1cfe0-117">方法呼叫順序</span><span class="sxs-lookup"><span data-stu-id="1cfe0-117">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> </dl>

 

 




