---
title: 無法撥號的原因
description: 下表列出表示無法連接介面之原因的常數值。
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b99d36ba895394a417130ab3ae45d1a47c7ed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023826"
---
# <a name="unreachability-reasons"></a>無法撥號的原因

下表列出表示無法連接介面之原因的常數值。



| 值                                       | 意義                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| MPR \_ 介面系統 \_ 管理員 \_ 已停用             | 系統管理員已停用介面。                                                  |
| MPR \_ 介面 \_ 連接 \_ 失敗         | 先前的連接嘗試失敗。 查看 **dwLastError** 成員中的錯誤碼。 |
| MPR \_ 介面 \_ 撥出時 \_ 數 \_ 限制 | 目前不允許撥號。                                                   |
| MPR \_ 介面 \_ \_ 資源不足 \_          | 沒有任何埠或裝置可供使用。                                                     |
| MPR \_ 介面 \_ 服務已 \_ 暫停             | 暫停服務。                                                                         |
| MPR \_ 介面 \_ 無 \_ 媒體 \_ 意義            | 網路纜線與網路介面卡中斷連線。                                       |
| MPR \_ 介面 \_ 無 \_ 裝置                  | 網路卡已從電腦移除。                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**MPR \_ 介面 \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[**MPR \_ 介面 \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[**MIB \_ IFROW**](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[**MIB \_ IFSTATUS**](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 