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
# <a name="registering-the-protocol-manager"></a>註冊通訊協定管理員

您至少必須為通訊協定管理員建立一個登錄值專案，遠端桌面服務服務才能將它具現化。

## <a name="registry-location"></a>登錄位置

針對您的通訊協定所使用的每個接聽程式 ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) ，在下列位置建立登錄機碼。 在此範例中，新的接聽程式金鑰稱為 *MyListener1* 和 *MyListener2*。

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

您可以在此位置中查看預設的 **rdp-tcp 接聽程式** 金鑰底下的值專案，以供參考。

## <a name="registry-value-entries"></a>登錄值專案

通訊協定的接聽程式金鑰必須有一個稱為 **LoadableProtocol \_ Object** 的值專案<dl> <dt>

資料類型
</dt> <dd>REG_SZ</dd> </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> 介面。 ) 遠端桌面服務服務會在找到登錄中的接聽程式之後，使用此 CLSID 將此接聽程式的通訊協定管理員具現化。

如果您的通訊協定提供者使用一個以上的接聽程式，遠端桌面服務服務只會建立一個通訊協定管理員實例，並使用它來針對每個接聽程式呼叫 [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) 一次。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立遠端桌面通訊協定提供者](creating-a-custom-remote-protocol.md)
</dt> <dt>

[方法呼叫順序](method-call-sequence.md)
</dt> </dl>

 

 




