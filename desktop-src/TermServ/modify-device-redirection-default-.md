---
title: 修改裝置重新導向預設值
description: 因為遠端桌面閘道伺服器在將用戶端連線傳遞到遠端桌面工作階段主機伺服器之前，嘗試強制執行安全的裝置重新導向原則，所以在某些情況下，您可能需要停用此預設值。
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b74515f6bf79b42c129ec7c113729b9871d4e4bfb0101f845f91dcac0d49237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138166"
---
# <a name="modify-device-redirection-default"></a>修改裝置重新導向預設值

因為遠端桌面閘道伺服器在將用戶端連線傳遞到遠端桌面工作階段主機伺服器之前，嘗試強制執行安全的裝置重新導向原則，所以在某些情況下，您可能需要停用此預設值。

在 Windows Server 2008 R2 和更新版本上，遠端桌面閘道伺服器預設會嘗試強制執行安全的裝置重新導向原則，然後才將用戶端連線傳遞到遠端桌面工作階段主機伺服器。 不過，某些伺服器並不支援這項功能。 例如，不支援對 Hyper-v 主控台會話的連線，而且可能需要停用預設值以支援同盟驗證。 在這些情況下，您可以藉由建立下列登錄機碼來停用這項功能，以允許連線通過。

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 終端機伺服器閘道 \\ preRDPDisableRegKey**

當此機碼存在時，遠端桌面閘道將不會強制執行裝置重新導向。

 

 




