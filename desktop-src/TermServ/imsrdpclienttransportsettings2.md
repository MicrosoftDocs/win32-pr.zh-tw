---
title: IMsRdpClientTransportSettings2 介面
description: 管理遠端桌面閘道 (RD 閘道) server 的用戶端傳輸設定。 |IMsRdpClientTransportSettings2 介面
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings2 介面遠端桌面服務
- IMsRdpClientTransportSettings2 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f2f4887c6a4f55f3b9c97c389e9afd702d2ffab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106975620"
---
# <a name="imsrdpclienttransportsettings2-interface"></a>IMsRdpClientTransportSettings2 介面

管理遠端桌面閘道 (RD 閘道) server 的用戶端傳輸設定。

## <a name="members"></a>成員

**IMsRdpClientTransportSettings2** 介面繼承自 [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)。 **IMsRdpClientTransportSettings2** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientTransportSettings2** 介面具有這些屬性。



| 屬性                                                                                                    | 存取類型           | Description                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [**GatewayCredSharing**](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | 讀取/寫入<br/> | 指出是否已啟用 RD 閘道的單一登入功能。<br/>                |
| [**GatewayDomain**](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | 讀取/寫入<br/> | 使用者為了連接到 RD 閘道伺服器所提供的功能變數名稱。<br/>              |
| [**GatewayEncryptedOtpCookie**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | 讀取/寫入<br/> | 加密的 OTP cookie。<br/>                                                              |
| [**GatewayEncryptedOtpCookieSize**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | 讀取/寫入<br/> | 加密 OTP cookie 的大小（以位元組為單位）。<br/>                                       |
| [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | 唯寫<br/> | 使用者為了連接到 RD 閘道伺服器所提供的密碼。<br/>                 |
| [**GatewayPreAuthRequirement**](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | 讀取/寫入<br/> | 指出是否已啟用 RD 閘道一次性密碼 (OTP) 功能。<br/>           |
| [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | 讀取/寫入<br/> | 預先驗證服務器的網路位址。<br/>                                      |
| [**GatewaySupportUrl**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | 讀取/寫入<br/> | 提供 RD 閘道 server 技術支援的網站網址。<br/> |
| [**GatewayUsername**](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | 讀取/寫入<br/> | 使用者為了連接到 RD 閘道伺服器所提供的使用者名稱。<br/>                |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista SP1<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                    |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 定義為 67341688-D606-4c73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





